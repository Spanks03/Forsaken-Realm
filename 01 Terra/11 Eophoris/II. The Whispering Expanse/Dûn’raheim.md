---
tags:
  - Location
  - Settlement
location:
  - The Whispering Expanse
mapmarker: Settlement
bannerArt: "[[PlaceholderSettlement.png]]"
art: 99 Images/Dûn’raheim (1).jpg
aliases:
  - Dûn’raheim
settlementType:
terrain:
  - Mountains
  - Subterranean
defence:
currentLocation: []
Population: 0.5
MilitaryMight: 12
Infrastructure: 6
PublicHealth: 12
EducationMagic: 12
EconomicStability: 8
Diplomacy: 6
Traits:
  - Veteran Army
  - Cultural Magnet
  - Iron Discipline
---
> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
>> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
>> **Aliases** | `INPUT[list:aliases]` |
>> **Type** | `INPUT[SettlementType][inlineListSuggester:settlementType]` |
>> **Terrain** | `INPUT[Terrain][inlineListSuggester:terrain]` |
>> **Location** | `INPUT[Location][inlineListSuggester:location]` |
>
>> [!metadata|metadataoption]- Demographics
>> #### Demographics
>>  |
>>---|---|
>> **Rulers** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"98 Templates"), useLinks(partial)):rulers]` |
>> **Leaders** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"98 Templates"), useLinks(partial)):leaders]` |
>> **Nation** | `INPUT[Nation][inlineListSuggester(optionQuery(Nation AND !"98 Templates"), useLinks(partial)):nation]` |
>> **Government** |  `INPUT[textArea:governmentType]` |
>> **Population** | `INPUT[Population][inlineSelect:Population]` |
>> **Alignment with Empire** | `INPUT[AlignmentEmpire][inlineListSuggester:alignmentEmpire]` |
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
>> **Traits** | `INPUT[SettlementTraits][inlineListSuggester:Traits]`

![[PlaceholderSettlement.png|banner]]

> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> 
> # Info
> | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Terrain** | `VIEW[{terrain}][text]` |
> | **Location** | `VIEW[{location}][link]` |
> 
> # Demographics
> | |
> |---|---|
> | **Rulers** | `VIEW[{ruler}][link]` |
> | **Leaders** | `VIEW[{leader}][link]` |
> | **Nation** | `VIEW[{nation}][Link]` |
> | **Government** | `VIEW[{governmentType}][text]` |
> | **Alignment with Empire** | `VIEW[{alignmentEmpire}][text]` |
> 
> # [[Travel Calculator]] 
> | |
> |---|---|
> | **TBD** | `VIEW[round(0 / (({Travel Calculator#MilesPerHour}*{Travel Calculator#HoursPerDay})*{Travel Calculator#SpeedMultiplier}),1)]` Day(s) |

> [!quote]- Scene Introduction
> A script to read from when the party arrives to the area for the first time to set the scene.

> *<font color="#7f7f7f">Summarize the settlement by describing its size, purpose, and defining features, along with what makes it stand out from others.</font>*

```dataviewjs
// ========================================
// 🏙️ D&D Settlement Stat Block Generator — Block 1 (Summary + Core Stats)
// ========================================

// Pull only from this note
const settlements = [dv.current()];

// --- Helpers ---
function mod(score) { return Math.floor((score - 10) / 2); }
function avg(...nums) { return nums.reduce((a,b) => a+b, 0) / nums.length; }
function formatMod(m) { return (m>=0 ? "+" : "") + m; }

// --- Trait Bonuses ---
const traitBonuses = {
  "Fortified Walls": { INF: +2, DefenseAC: +2 },
  "Trade Hub": { ECO: +2, DIP: +1 },
  "Grand Academy": { EDU: +3, innovation: +2 },
  "Veteran Army": { MIL: +3, morale: +1 },
  "Cultural Magnet": { DIP: +2, growth: +1 },
  "Sacred Wells": { PH: +2, recovery: +1 },
  "Arcane Nexus": { EDU: +2, ECO: +1 },
  "Merchant Princes": { ECO: +3, DIP: +1 },
  "City of Artisans": { INF: +1, ECO: +2 },
  "Divine Favor": { PH: +1, DIP: +1, morale: +2 },
  "Mercenary Contract": { MIL: +2, ECO: +1 },
  "Hidden Vaults": { ECO: +1, DefenseAC: +1 },
  "Iron Discipline": { MIL: +2, morale: +2 },
  "Revolutionary Spirit": { DIP: +1, MIL: +1, growth: +2 },
  "Harbor of Storms": { ECO: +1, MIL: +1, INF: +1 }
};

// --- Size tiers ---
const tiers = [
  { max: 0.25, name: "Thorp", score: 0, range: "20-80 People" },
  { max: 0.5, name: "Hamlet", score: 1, range: "81-400 People"  },
  { max: 0.75, name: "Village", score: 2, range: "401-1,000 People"  },
  { max: 1, name: "Small Town", score: 2.5, range: "1,001-3,000 People"  },
  { max: 1.5, name: "Large Town", score: 3, range: "3,001-6,000 People"  },
  { max: 2, name: "Small City", score: 3.5, range: "6,001-25,000 People"  },
  { max: 3, name: "Large City", score: 4, range: "25,001-100,000 People"  },
  { max: 4, name: "Metropolis", score: 5, range: "100,001+ People"  }
];
function getTier(pop) { for (let t of tiers) if (pop <= t.max) return t; return {name:"Unknown", score:6}; }

// --- Main ---
for (let p of settlements) {
  const pop = Number(p.Population ?? 1);
  const tier = getTier(pop);

  // Base stats
  let MIL = Number(p.MilitaryMight ?? 10);
  let INF = Number(p.Infrastructure ?? 10);
  let PH  = Number(p.PublicHealth ?? 10);
  let EDU = Number(p.EducationMagic ?? 10);
  let ECO = Number(p.EconomicStability ?? 10);
  let DIP = Number(p.Diplomacy ?? 10);

  // Trait application
  const traits = p.Traits ? (Array.isArray(p.Traits) ? p.Traits : [p.Traits]) : [];
  const bonusNotes = [];
  let derivedBonuses = { DefenseAC: 0, RecoveryRate: 0, AttackBonus: 0, DamagePerVolley: 0, BattleRating: 0 };

  for (const trait of traits) {
    const b = traitBonuses[trait];
    if(!b) continue;

    if(b.MIL) MIL += b.MIL;
    if(b.INF) INF += b.INF;
    if(b.PH)  PH  += b.PH;
    if(b.EDU) EDU += b.EDU;
    if(b.ECO) ECO += b.ECO;
    if(b.DIP) DIP += b.DIP;

    if(b.DefenseAC) derivedBonuses.DefenseAC += b.DefenseAC;
    if(b.RecoveryRate) derivedBonuses.RecoveryRate += b.RecoveryRate;
    if(b.AttackBonus) derivedBonuses.AttackBonus += b.AttackBonus;
    if(b.DamagePerVolley) derivedBonuses.DamagePerVolley += b.DamagePerVolley;
    if(b.BattleRating) derivedBonuses.BattleRating += b.BattleRating;

    bonusNotes.push(`${trait}: ${Object.entries(b).map(([k,v])=>`${k}+${v}`).join(", ")}`);
  }

  // Recompute modifiers
  const MIL_MOD = mod(MIL);
  const INF_MOD = mod(INF);
  const PH_MOD  = mod(PH);
  const EDU_MOD = mod(EDU);
  const ECO_MOD = mod(ECO);
  const DIP_MOD = mod(DIP);

  // Derived stats
  const BattleRating = MIL + Math.log2(10*pop) + derivedBonuses.BattleRating;
  const DefenseAC = 10 + INF_MOD + Math.floor(MIL_MOD/2) + Math.floor(tier.score/2) + derivedBonuses.DefenseAC;
  const PopulationEndurance = Math.round((PH + INF)*10*pop);
  const AttackBonus = MIL_MOD + Math.floor(EDU_MOD/3) + Math.log2(pop*10) + derivedBonuses.AttackBonus;
  const DamagePerVolley = Math.round((MIL*(1+ECO/10))*(pop/1.5)) + derivedBonuses.DamagePerVolley;
  const InfluenceRadius = Math.round(((DIP + ECO + EDU)/3) * Math.sqrt(pop));
  const RecoveryRate = Math.round(((PH + ECO + INF/2)/4)*pop) + derivedBonuses.RecoveryRate;
  const SettlementPower = Math.min(30, Math.max(1, Math.round((BattleRating + DefenseAC + AttackBonus + (PopulationEndurance/10))/5)));

  // Saving Throws
  const famineSave      = formatMod(PH_MOD);
  const siegeSave       = formatMod(mod(avg(INF, MIL)));
  const growthCheck     = formatMod(mod(avg(DIP, ECO)));
  const innovationCheck = formatMod(mod(avg(EDU, ECO)));
  const recoveryCheck   = formatMod(mod(avg(PH, ECO)));
  const moraleSave      = formatMod(mod(avg(DIP, MIL)));

  // --- OUTPUT ---
  dv.el("hr");
  dv.paragraph(`# **Dûn’raheim (${tier.name})**  
*Settlement, Neutral*  
**Armor Class** ${DefenseAC}  
**Hit Points** ${PopulationEndurance}  (Population: *${tier.range}*)
**Speed** Influence radius ${InfluenceRadius} miles  
**Recovery Rate** ${RecoveryRate}  
**Challenge Rating (CR)** ${SettlementPower}

**Attack Bonus** ${formatMod(Math.round(AttackBonus))}  
**Damage per Volley** ${DamagePerVolley}`);

  // Core Stats Table
  dv.el("div", `
  <table style="width: 900px; margin: 10px auto; border-collapse: collapse; text-align: center; font-size: 16px;">
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
  </table>`);

  // Save Stats for Block 2
  window.settlementTier = tier.name;
  window.settlementStats = {
    MIL, INF, PH, EDU, ECO, DIP,
    MIL_MOD, INF_MOD, PH_MOD, EDU_MOD, ECO_MOD, DIP_MOD,
    DefenseAC, PopulationEndurance, AttackBonus, DamagePerVolley,
    InfluenceRadius, RecoveryRate, SettlementPower,
    traits, bonusNotes, pop
  };
}

```
> [!tip|map] Settlement Map
> ```leaflet
> id: Dûn’raheim
> image: [[Dûn’raheim (1).jpg]]
> lock: true
> recenter: true
> noScrollZoom: false
> ### Use this [LINK](https://docs.google.com/spreadsheets/d/1jKQxktYSUFcCJhEkAAPr1wMVBTqUdpEfA5XveUXI17I/edit?usp=sharing) to work out your map's bounds.
> ### bounds: [[0,0], [3072,4096]] (Remove the ### and these parentheses with the content within from this line to enable the bounds)
> height: 500px
> width: 58%
> lat: 1536
> long: 2048
> minZoom: 2.4
> maxZoom: 6.0
> defaultZoom: 1
> zoomDelta: 0.2
> unit: miles
> scale: 1
> darkMode: false
> ```

```dataviewjs
// ========================================
// 🏙️ D&D Settlement Stat Block Generator — Block 2 (Saves, Traits, Actions + Bonus Notes)
// ========================================

const p = dv.current();

function mod(score) { return Math.floor((score - 10) / 2); }
function avg(...nums) { return nums.reduce((a,b)=>a+b,0)/nums.length; }
function formatMod(m) { return (m>=0 ? "+" : "") + m; }

// --- TRAIT BONUSES (must match Block 1) ---
const traitBonuses = {
  "Fortified Walls": { INF: +2, DefenseAC: +2 },
  "Trade Hub": { ECO: +2, DIP: +1 },
  "Grand Academy": { EDU: +3, innovation: +2 },
  "Veteran Army": { MIL: +3, morale: +1 },
  "Cultural Magnet": { DIP: +2, growth: +1 },
  "Sacred Wells": { PH: +2, recovery: +1 },
  "Arcane Nexus": { EDU: +2, ECO: +1 },
  "Merchant Princes": { ECO: +3, DIP: +1 },
  "City of Artisans": { INF: +1, ECO: +2 },
  "Divine Favor": { PH: +1, DIP: +1, morale: +2 },
  "Mercenary Contract": { MIL: +2, ECO: +1 },
  "Hidden Vaults": { ECO: +1, DefenseAC: +1 },
  "Iron Discipline": { MIL: +2, morale: +2 },
  "Revolutionary Spirit": { DIP: +1, MIL: +1, growth: +2 },
  "Harbor of Storms": { ECO: +1, MIL: +1, INF: +1 }
};

// --- Base scores (read from frontmatter/fields) ---
let MIL = Number(p.MilitaryMight ?? p.MIL ?? 10);
let INF = Number(p.Infrastructure ?? p.INF ?? 10);
let PH  = Number(p.PublicHealth ?? p.PH ?? 10);
let EDU = Number(p.EducationMagic ?? p.EDU ?? 10);
let ECO = Number(p.EconomicStability ?? p.ECO ?? 10);
let DIP = Number(p.Diplomacy ?? p.DIP ?? 10);
const pop = Number(p.Population ?? 1);

// --- Prepare trait list & apply bonuses to the base scores ---
const traits = p.Traits ? (Array.isArray(p.Traits) ? p.Traits : [p.Traits]) : [];
const bonusNotes = [];
let derivedBonuses = { DefenseAC: 0, RecoveryRate: 0, AttackBonus: 0, DamagePerVolley: 0, BattleRating: 0 };

for (const trait of traits) {
  const b = traitBonuses[trait];
  if (!b) continue;

  // apply ability bonuses if present
  if (b.MIL) MIL += b.MIL;
  if (b.INF) INF += b.INF;
  if (b.PH)  PH  += b.PH;
  if (b.EDU) EDU += b.EDU;
  if (b.ECO) ECO += b.ECO;
  if (b.DIP) DIP += b.DIP;

  // collect derived stat bonuses to apply later
  if (b.DefenseAC) derivedBonuses.DefenseAC += b.DefenseAC;
  if (b.RecoveryRate) derivedBonuses.RecoveryRate += b.RecoveryRate;
  if (b.AttackBonus) derivedBonuses.AttackBonus += b.AttackBonus;
  if (b.DamagePerVolley) derivedBonuses.DamagePerVolley += b.DamagePerVolley;
  if (b.BattleRating) derivedBonuses.BattleRating += b.BattleRating;

  // human-readable note
  bonusNotes.push(`${trait}: ${Object.entries(b).map(([k,v])=>`${k}+${v}`).join(", ")}`);
}

// --- Recompute modifiers after applying trait ability bonuses ---
const MIL_MOD = mod(MIL);
const INF_MOD = mod(INF);
const PH_MOD  = mod(PH);
const EDU_MOD = mod(EDU);
const ECO_MOD = mod(ECO);
const DIP_MOD = mod(DIP);

// --- Derived values (now include derivedBonuses where appropriate) ---
let DefenseAC = 10 + INF_MOD + Math.floor(MIL_MOD / 2) + (derivedBonuses.DefenseAC || 0);
let PopulationEndurance = Math.round((PH + INF) * 10 * pop);
let AttackBonus = MIL_MOD + Math.floor(EDU_MOD / 3) + (derivedBonuses.AttackBonus || 0) + (p.Population ? Math.log2(Number(p.Population) * 10) : 0);
let DamagePerVolley = Math.round((MIL * (1 + ECO / 10)) * (pop / 1.5)) + (derivedBonuses.DamagePerVolley || 0);
let InfluenceRadius = Math.round(((DIP + ECO + EDU) / 3) * Math.sqrt(pop));
let RecoveryRate = Math.round(((PH + ECO + INF / 2) / 4) * pop) + (derivedBonuses.RecoveryRate || 0);
let BattleRating = MIL + Math.log2(10 * pop) + (derivedBonuses.BattleRating || 0);

// --- Saving Throws & Checks (use updated MODs) ---
const famineSave      = formatMod(PH_MOD);
const siegeSave       = formatMod(mod(avg(INF, MIL)));
const growthCheck     = formatMod(mod(avg(DIP, ECO)));
const innovationCheck = formatMod(mod(avg(EDU, ECO)));
const recoveryCheck   = formatMod(mod(avg(PH, ECO)));
const moraleSave      = formatMod(mod(avg(DIP, MIL)));

// --- Render saving throw table ---
dv.el("div", `
  <table style="
    width: 900px;
    margin: 20px auto;
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

// --- Traits + BonusNotes display ---
const traitsText = traits.length > 0 ? traits.join(", ") : "None";

dv.el("blockquote", `***Traits***  
**Active Traits:** ${traitsText}${bonusNotes.length ? `  
_(Bonuses: ${bonusNotes.join("; ")})_` : ""}`);

// --- Actions (use updated derived values/mods) ---
dv.el("blockquote", `***Actions (Conflict Resolution)***  
- **Open Battle.** Roll *1d20 ${formatMod(Math.round(AttackBonus))}* vs. target **Defense Rating**. Success deals ~${DamagePerVolley} (per volley).  
- **Siege Warfare.** Roll *1d20 ${formatMod(MIL_MOD)}* vs. **Resistance to Siege DC**.  
- **Diplomatic Maneuver.** Roll *1d20 ${formatMod(DIP_MOD)}* vs. **Expanding Influence DC**.  
- **Research Race.** Roll *1d20 ${formatMod(EDU_MOD)}* vs. **Innovation DC**.  
- **Recovery Effort.** Roll *1d20 ${formatMod(PH_MOD)}* vs. **Event Difficulty DC**.`);

```
## Overview

### Description:

> *<font color="#7f7f7f">What is the settlement's environment, architecture, culture, and overall atmosphere? Describe its look and feel, what it's known for, who lives there, and how it fits into the surrounding region.</font>*

### Society & Culture:

> *<font color="#7f7f7f">What is daily life like in the settlement? How do its people think, behave, and interact? Describe customs, traditions, beliefs, social structure, and any notable values or taboos.</font>*
> 
## Database

![[Database - Settlement Note.base]]

## Commerce

> [!grid|col-2]
> <font color="#9bbb59">**Imported Goods:**</font> `VIEW[{import}][text]`
>
> <font color="#c0504d">**Exported Goods:**</font> `VIEW[{export}][text]`

### Trade Agreements:

- [[Template - Settlement]]
   - <font color="#9bbb59">Example Import</font> - Why do they import this from here?
- [[Template - Settlement]]
   - <font color="#c0504d">Example Export</font> - Why do they export to here?

## Present

### Current Events:

> *<font color="#7f7f7f">- Example Quest</font>*
> *<font color="#7f7f7f">    - Summary of a quest the player can get involved in.</font>*
> *<font color="#7f7f7f">- Example Event</font>*
> *<font color="#7f7f7f">    - Summary of an event that's going on in this settlement which may not relate to a specific quest or may relate to multiple.</font>*

## Past

### History:

> *<font color="#7f7f7f">What key events have shaped this settlement over time? Consider ancient civilizations, major wars, migrations, natural disasters, or political shifts. How has its past influenced the cultures, borders, and conflicts that exist today?</font>*

### Secrets, Rumours & Legends:

> *<font color="#7f7f7f">What hidden truths or mysteries lie across the settlement? These could include lost kingdoms, ancient technologies, forbidden magic, hidden societies, or concealed geopolitical agendas. Who knows about them and what would it mean if they were revealed?</font>*

## Notes

