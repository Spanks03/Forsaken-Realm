---
Population: 0.25
MilitaryMight: 30
Infrastructure: 16
PublicHealth: 30
EducationMagic: 1
EconomicStability: 1
Diplomacy: 1
Traits:
  - Arcane Nexus
  - Divine Favor
---
> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- Settlement Data
>> #### Settlement Size
>>  |
>> ---|---|
>> **Population** | `INPUT[Population][inlineSelect:Population]` |
>
>>[!metadata|metadataoption]- Settlement Ability Scores
>>#### Ability Scores Calculation
>>  |
>> ---|---|
>> **Military Might** | `INPUT[MilitaryMight][inlineSelect:MilitaryMight]` |
>> **Infrastructure** | `INPUT[Infrastructure][inlineSelect:Infrastructure]`|
>> **Public Health** |`INPUT[PublicHealth][inlineSelect:PublicHealth]`|
>> **Education/Magic** |`INPUT[EducationMagic][inlineSelect:EducationMagic]`|
>> **Economic Stability** |`INPUT[EconomicStability][inlineSelect:EconomicStability]`|
>> **Diplomacy** |`INPUT[Diplomacy][inlineSelect:Diplomacy]`|
>
>>[!metadata|metadataoption]- Settlement Traits
>>#### Traits
>>  |
>> ---|---|
>> **Settlement Traits** | `INPUT[SettlementTraits][inlineListSuggester:Traits]`

```dataviewjs
// ========================================
// 🏙️ D&D Settlement Stat Block Generator (Per-Note Version)
// ========================================

// Only pull data from *this* note
const settlements = [dv.current()];

// --- HELPERS ---
function mod(score) { return Math.floor((score - 10) / 2); }
function avg(...nums) { return nums.reduce((a,b) => a+b, 0) / nums.length; }
function formatMod(m) { return (m>=0 ? "+" : "") + m; }

// --- Trait Derived Bonus Accumulators ---
let famine = 0;
let seige = 0;
let innovation = 0;
let growth = 0;
let morale = 0;
let recovery = 0;

// --- TRAIT BONUSES ---
const traitBonuses = {
  "Fortified Walls": { INF: +2, DefenseAC: +2 },  
  "Trade Hub": { ECO: +2, DIP: +1 },  
  "Grand Academy": { EDU: +3, innovationCheck: +2 },  
  "Veteran Army": { MIL: +3, moraleSave: +1 },  
  "Cultural Magnet": { DIP: +2, growthCheck: +1 },  
  "Sacred Wells": { PH: +2, recoveryCheck: +1 },  
  "Arcane Nexus": { EDU: +2, ECO: +1 },  
  "Merchant Princes": { ECO: +3, DIP: +1 },  
  "City of Artisans": { INF: +1, ECO: +2 },  
  "Divine Favor": { PH: +1, DIP: +1, moraleSave: +2 },  
  "Mercenary Contract": { MIL: +2, ECO: +1 },  
  "Hidden Vaults": { ECO: +1, DefenseAC: +1 },  
  "Iron Discipline": { MIL: +2, moraleSave: +2 },  
  "Revolutionary Spirit": { DIP: +1, MIL: +1, growthCheck: +2 },  
  "Harbor of Storms": { ECO: +1, MIL: +1, INF: +1 },  
  "Circle of Venterri": { DIP: +3, EDU: +1, innovationCheck: +1 }
};

// --- SIZE TIERS ---
const tiers = [
  { max: 0.25, name: "Thorp", score: 0 },
  { max: 0.5, name: "Hamlet", score: 1 },
  { max: 0.75, name: "Village", score: 2 },
  { max: 1, name: "Small Town", score: 2.5 },
  { max: 1.5, name: "Large Town", score: 3 },
  { max: 2, name: "Small City", score: 3.5 },
  { max: 3, name: "Large City", score: 4 },
  { max: 4, name: "Metropolis", score: 5 }
];
function getTier(pop) { for (let t of tiers) if (pop<=t.max) return t; return {name:"Unknown", score:6}; }

// --- MAIN LOOP ---
for (let p of settlements) {
  const pop = Number(p.Population);
  const tier = getTier(pop);

  // --- Base Scores ---
  let MIL = Number(p.MilitaryMight);
  let INF = Number(p.Infrastructure);
  let PH  = Number(p.PublicHealth);
  let EDU = Number(p.EducationMagic);
  let ECO = Number(p.EconomicStability);
  let DIP = Number(p.Diplomacy);

  // --- Trait List ---
  const traits = p.Traits ? (Array.isArray(p.Traits) ? p.Traits : [p.Traits]) : [];

  // --- Derived Bonus Accumulators ---  
  let innovationBonus = 0;  
  let growthBonus = 0;  
  let moraleBonus = 0;  
  let recoveryBonus = 0;  
  let defenseBonus = 0;
  
  // --- Derived Modifiers (from base abilities) ---
  let MIL_MOD = mod(MIL);
  let INF_MOD = mod(INF);
  let PH_MOD  = mod(PH);
  let EDU_MOD = mod(EDU);
  let ECO_MOD = mod(ECO);
  let DIP_MOD = mod(DIP);

  // --- Derived Calculations (BASE) ---
  let BattleRating = MIL + Math.log2(10*pop);
  let DefenseAC = 10 + INF_MOD + Math.floor(MIL_MOD/2) + Math.floor(tier.score/2);
  let PopulationEndurance = Math.round((PH+INF)*10*pop);
  let AttackBonus = MIL_MOD + Math.floor(EDU_MOD/3) + Math.log2(pop*10);
  let DamagePerVolley = Math.round((MIL*(1+ECO/10))*(pop/1.5));
  let InfluenceRadius = Math.round(((DIP+ECO+EDU)/3) * Math.sqrt(pop));
  let RecoveryRate = Math.round(((PH + ECO + INF/2)/4)*pop);

  // --- Apply Trait Bonuses ---
  let bonusNotes = [];
  for (const trait of traits) {
    const b = traitBonuses[trait];
    if (!b) continue;

    if (b.MIL) { MIL += b.MIL; MIL_MOD = mod(MIL); }
    if (b.INF) { INF += b.INF; INF_MOD = mod(INF); }
    if (b.PH)  { PH += b.PH; PH_MOD = mod(PH); }
    if (b.EDU) { EDU += b.EDU; EDU_MOD = mod(EDU); }
    if (b.ECO) { ECO += b.ECO; ECO_MOD = mod(ECO); }
    if (b.DIP) { DIP += b.DIP; DIP_MOD = mod(DIP); }

    if (b.DefenseAC) DefenseAC += b.DefenseAC;
    if (b.RecoveryRate) RecoveryRate += b.RecoveryRate;
    if (b.AttackBonus) AttackBonus += b.AttackBonus;
    if (b.DamagePerVolley) DamagePerVolley += b.DamagePerVolley;
    if (b.BattleRating) BattleRating += b.BattleRating;
	if (b.innovationCheck) innovationBonus += b.innovationCheck;  
	if (b.growthCheck) growthBonus += b.growthCheck;  
	if (b.moraleSave) moraleBonus += b.moraleSave;  
	if (b.recoveryCheck) recoveryBonus += b.recoveryCheck;

    bonusNotes.push(`${trait}: ${Object.entries(b).map(([k,v])=>`${k}+${v}`).join(", ")}`);
  }

  // --- Settlement Power CR 1–30 ---
  const SettlementPower = Math.min(30, Math.max(1, Math.round((BattleRating + DefenseAC + AttackBonus + (PopulationEndurance/10))/5)));

  // --- Saving Throws & Checks ---
  const famineSave      = formatMod(PH_MOD);
  const siegeSave       = formatMod(mod(avg(INF, MIL)));
  const growthCheck = formatMod(mod(avg(DIP, ECO)) + growthBonus);  
  const innovationCheck = formatMod(mod(avg(EDU, ECO)) + innovationBonus);  
  const recoveryCheck = formatMod(mod(avg(PH, ECO)) + recoveryBonus);  
  const moraleSave = formatMod(mod(avg(DIP, MIL)) + moraleBonus);
  
  

  // === OUTPUT ===
  dv.el("hr");
  dv.paragraph(`# **${p.file.name} (${tier.name})**  
*Settlement, Neutral*  
**Armor Class** ${DefenseAC} (walls and defenses)  
**Hit Points** ${PopulationEndurance} (Population Endurance)  
**Speed** Influence radius ${InfluenceRadius} miles  
**Recovery Rate** ${RecoveryRate}
**Challenge Rating (CR)** ${SettlementPower}

**Attack Bonus** ${formatMod(Math.round(AttackBonus))}  
**Damage per Volley** ${DamagePerVolley}  
`);

  // Core Stats Table
  dv.el("div", `
  <table style="
    width: 900px;
    margin: 10px auto;
    border-collapse: collapse;
    text-align: center;
    font-size: 16px;">
    <thead>
      <tr>
        <th>MILITARY (MIL)</th>
        <th>INFRASTRUCTURE (INF)</th>
        <th>HEALTH (PH)</th>
        <th>EDUCATION (EDU)</th>
        <th>ECONOMY (ECO)</th>
        <th>DIPLOMACY (DIP)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><b>${formatMod(MIL_MOD)}</b> <br>(${MIL})</td>
        <td><b>${formatMod(INF_MOD)}</b> <br>(${INF})</td>
        <td><b>${formatMod(PH_MOD)}</b> <br>(${PH})</td>
        <td><b>${formatMod(EDU_MOD)}</b> <br>(${EDU})</td>
        <td><b>${formatMod(ECO_MOD)}</b> <br>(${ECO})</td>
        <td><b>${formatMod(DIP_MOD)}</b> <br>(${DIP})</td>
      </tr>
    </tbody>
  </table>
  `);

  // Saving Throws Table
  dv.el("div", `
  <table style="
    width: 900px;
    margin: 10px auto;
    border-collapse: collapse;
    text-align: center;
    font-size: 15px;">
    <thead>
      <tr><th>Type</th><th>Modifier</th><th>Example Use</th></tr>
    </thead>
    <tbody>
      <tr><td>Famine / Plague Save (PH)</td><td>${famineSave}</td><td>Resist disease or famine events</td></tr>
      <tr><td>Siege Save (INF & MIL)</td><td>${siegeSave}</td><td>Endure or repel sieges</td></tr>
      <tr><td>Growth / Expansion Check (DIP & ECO)</td><td>${growthCheck}</td><td>Attract settlers or allies</td></tr>
      <tr><td>Innovation / Research Check (EDU & ECO)</td><td>${innovationCheck}</td><td>Advance tech or magic</td></tr>
      <tr><td>Recovery Check (PH & ECO)</td><td>${recoveryCheck}</td><td>Rebuild after wars/disasters</td></tr>
      <tr><td>Morale Save (DIP & MIL)</td><td>${moraleSave}</td><td>Resist panic or unrest</td></tr>
    </tbody>
  </table>
  `);

  // Traits + Actions
  const traitsText = traits.length > 0 ? traits.join(", ") : "None";
  dv.el("blockquote", `***Traits***  
**Active Traits:** ${traitsText}${bonusNotes.length ? `  
_(Bonuses: ${bonusNotes.join("; ")})_` : ""}`);

  dv.el("blockquote", `***Actions (Conflict Resolution)***  
- **Open Battle.** Roll *1d20 ${formatMod(Math.round(AttackBonus))}* vs. target **Defense Rating**.  
- **Siege Warfare.** Roll *1d20 ${formatMod(MIL_MOD)}* vs. **Resistance to Siege DC**.  
- **Diplomatic Maneuver.** Roll *1d20 ${formatMod(DIP_MOD)}* vs. **Expanding Influence DC**.  
- **Research Race.** Roll *1d20 ${formatMod(EDU_MOD)}* vs. **Innovation DC**.  
- **Recovery Effort.** Roll *1d20 ${formatMod(PH_MOD)}* vs. **Event Difficulty DC**.`);
}

```