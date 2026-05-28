---
tags:
  - Location
  - Settlement
location:
  - The Whispering Expanse
mapmarker: Settlement
bannerArt: "[[PlaceholderSettlement.png]]"
art: 99 Images/Oar's Break Images/OB.png
aliases:
  - Oar's Break
settlementType:
  - Large Town
terrain:
  - Rivers
defence:
currentLocation: []
dominion: []
rulers: []
leaders: []
organizations: []
governmentType: []
population:
imports:
exports:
heritage:
  - Rivers
Population: 1.5
MilitaryMight: 4
Infrastructure: 10
PublicHealth: 12
EducationMagic: 8
EconomicStability: 12
Diplomacy: 6
Traits:
  - Hidden Vaults
  - Trade Hub
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
>> **Location** | `INPUT[Location][inlineListSuggester(optionQuery(Location AND !"98 Templates"), useLinks(partial)):location]` |
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

> [!quote]- Scene Introduction
> A script to read from when the party arrives to the area for the first time to set the scene.

> *<font color="#7f7f7f">Summarize the settlement by describing its size, purpose, and defining features, along with what makes it stand out from others.</font>*

![[OB Streetview.png|banner]]

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
  dv.paragraph(`# **${p.file.name} (${tier.name})**  
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

## Map

> [!tip|map] Settlement Map
>```leaflet  
>id: OarBreakMap ### Must be unique with no spaces  
>image: 
>  - [[Oar's Break.jpg]]
>  - [[Oar's Break (Night).jpg]]
>bounds: [[0,0], [2304, 3072]] ### Size of the map in px Height_y, Width_x. Ignore 0,0  
>height: 500px ### Size of the leaflet embed in px on your screen  
>width: 50% ### Size of the leaflet embed in your note  
>lat: 1152 ### To center the map, make this half of the map height.  
>long: 1536 ### To center the map, make this half of the map width.  
>minZoom: -2.2 ### Controls how far away from the map you can zoom out. Hover over the target icon to see the current level.  
>maxZoom: 1 ### Controls how far towards the map you can zoom in. Hover over the target icon to see the current level.  
>defaultZoom: -2.2 ### Sets the default zoom level when the map loads. Hover over the target icon to see the current level.  
>zoomDelta: 0.2 ### Adjust how much the zoom changes when you zoom in or out.  
>unit: ft ### The value displayed when measuring so you know what type of unit is being measure.  
>scale: 0.10714285714285714 ### Real units/px (resolution) of your map  
>recenter: true  
>darkmode: false ### marker
>```

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

**Oar’s Break** is a quiet jewel nestled within a man-made loop of the Whispering Stretch, hidden away in the winding arteries of the Whispering Expanse. Though modest in size, it serves as a treasured waypoint for seasoned river travelers—those who know where to veer off the current and into calmer waters. The loop itself is a clever feat of early engineering, creating a natural harbor that shelters boats from the powerful main flow of the river. Wooden docks rise from stone-reinforced banks, and the hum of town life—barter, hammering, laughter—spills gently across the surface of the water.

### Description:

The town itself is a patchwork of worn timber and sunbaked brick, with low buildings huddled close to the riverside and a few cobbled paths winding their way inward. Narrow roads bend around modest homes, small shops, and the weathered inn that gives the town its name. Despite its simple appearance, Oar’s Break is far from provincial. The streets are often filled with travelers of many kinds—fishermen, wandering traders, ferrymen, and even adventurers between contracts—making it a place of quiet stories and unspoken trust. Though the town lacks the infrastructure to support large fleets or full-scale trade, its people offer rest, repair, and honesty in equal measure.

On the outskirts, hidden in the shadow of leaning pines and tall grasses, stands a crescent-shaped shrine to **Lunala**, the Keeper of Night and Darkness. Lanterns flicker gently along its path even in daylight, and the temple's presence casts a quiet reverence over the surrounding woods. In contrast, the larger, sunlit **Temple of Sol** lies a day's journey away in the riverside city of **Spanreach**, giving Oar’s Break a uniquely nocturnal spiritual leaning. Governance is split between **Mayor Elira Voss**, a sharp-eyed woman with a merchant’s pragmatism, and **Constable Dor Pike**, a broad-shouldered veteran whose silence speaks louder than orders. Together, they keep the peace—not with iron laws, but with familiarity and patience. The people of Oar’s Break know each other, and they know the river, and that's more than enough.

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

1. [[Briarwind Farm]] - A sprawling field of wheat and vegetables with lazy chickens. Halder rarely speaks unless you’re buying or helping.
2. [[Greystone Manor]] - A well-maintained stone estate with a small garden. Mayor Voss is calm, practical, and runs the town with quiet confidence.
3. [[Oldstone Mill]] - The creaking wheel turns slow but steady. Marnick grinds grain with stories of how everything was better “last season.”
4. [[Constables Dorn Pike]]' Roost
5. [[Hollowstep Estate]] - Overgrown vines and shuttered windows hide whispers of a life once lived. Locals say the adventurer who owned it never returned from the deep woods.
6. [[Driftmark Dock Office]] - A riverside guild with crates stacked high. Wilma manages local river trade - logging/managing incoming and outgoing boats.
7. [[The Braided Ram Inn]] - Warm fire, braided tapestries, and Lette’s famous stew. The beds are clean and the gossip free-flowing.
8. [[Lorn & Fila Varyn]]'s House
9. [[Grandmother Kesh]]'s House
10. [[Jarin Feld]]'s House
11. [[Yura & Cal Tembin]]'s House
12. [[Brel & Doma Ashglen]]'s House
13. [[Gellen the Mute]]'s House
14. [[Ironroot Forge]] - The clang of hammer never ceases. Brenna’s strength is matched only by her craftsmanship.
15. [[The Tradehouse]] - Organized chaos of goods, scrolls, and traders. Sarvin is more politician than merchant.
16. [[Townspire Hall]] - A narrow tower of records and bureaucracy. Olwin remembers every letter ever sent.
17. [[The Hollow Hearth Tavern]] - A lively tavern with a cracked hearthstone and off-key singing. Tuck serves drinks and dodges questions.
18. [[Produce Stall]] - Fresh vegetables and sly smiles. Lysa knows everyone's secrets but never tells.
19. [[Vaultclerk Office]] - Iron doors, clean books, and a quiet sneeze echoing through the ledgers. Penra is paranoid, but effective.
20. [[Willowmane Stables]] - Horses, mules, and occasional goats. Orven is better with animals than people.
21. [[Niloressa]]'s House
22. [[Tallow's General Goods]] - A cluttered store with everything almost in stock. Mirk forgets prices and makes up deals on the spot.
23. [[Trinket Stalls]] - Handmade toys, carved trinkets, and embroidered satchels. She hums lullabies as she works.
24. [[Smoked Meats]] - He wears an apron blackened by years of smoke. Everything he sells smells like fire and pepper.
25. [[Cleaver's Chop]] - Sharp knives, sharp tongue. She’s clean, precise, and never wastes meat.
26. [[Stonekeep Depot]] - Dusty crates and heavy crates. Joss is wiry, sarcastic, and always covered in ore dust.
27. [[Tavrin & Moss]]' House
28. [[Town Lot Storage Barn]] - Unlocked during daylight. Holds lumber, mining gear, spare carts, and old festival banners.
29. [[Quillgate Hall]] - Strict, patient, and surprisingly good with maps. Children fear her bell.
30. [[Farra Redleaf]] Farmstead
31. [[Notch & String]] - His arrows fly true, and his jokes miss always. Keeps a pet hawk named Shriek.
32. [[Chillcellar Stores]] - Cool and well-ventilated. No rats. Usually.
33. [[The Frothing Barrel]] - Honey ale, sour rye, and thick stews. Wyla drinks more than she sells.
34. [[Dusty Tomes]] - Nemeris knows every spine by scent and finger. Occasionally speaks in riddles.
35. [[Hammer & Peg]] - Careful, proud, and obsessed with beams being “just so.” Has opinions on every house in town.
36. [[The Pikewatch Barracks]] - Discipline, drills, and a half-decent sparring ring. She’ll train anyone who shows up sober.
37. [[Thread & Tannin]] - Rough hands, softer heart. Daria crafts leather armor and dyed wool, often humming to herself.
38. [[The Verdant Jar]] - Vials of color, herbs hanging to dry. Renwin is calm, often speaks with plants, and sometimes they answer.
39. [[Whisperwillow Clinic]] - A gentle, aging healer who once served in a war. Uses poultices, prayer, and a firm bedside manner.
40. [[Talla & Hen]]'s House
41. [[Berun Kross]]'s House
42. [[Timber Hollow]] - Smells of pine and damp sawdust.
43. [[Temple of Lunala]] - A temple of quiet shadows and silver candles. Nyra offers gentle guidance and moon-blessed charms.

