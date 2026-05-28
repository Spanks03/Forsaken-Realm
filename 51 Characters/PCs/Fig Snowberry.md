---
tags:
  - Character
  - Player
art: 99 Images/Fig.png
playedBy: Andrew
aliases:
  - Fig
ancestry: Halfling
heritage: Hillfolk Halfling
gender: N/A
pronouns:
languages:
  - Common
  - Halfling
  - Common Sign Language
occupation:
  - Cook
organizations: []
religions: []
condition:
  - Healthy
currentLocation: []
whichParty: []
fc-date:
  year: "[-*]"
birthday: -28
year:
age: 5
alignment: Neutral Good
flaws: Naive to a fault. Trust anyone the speaks kindly. Has not seen too much bad thinks.
ideals: Everyone deserves warm food in the bellies and kind words. Everyone is good if given the chance. The world is nice.
fears: "Fire, blood, and others in pain "
str: 6
dex: 10
con: 16
int: 18
wis: 10
cha: 12
ac: 15
hp_max: 31
hp_current: 31
mana_max: 20
mana_current: 20
spell_save_dc: 18
spell_attack_mod: 8
initiative_mod: 0
speed: 25
prof_bonus: 3
coins:
  cp: 17
  sp: 19
  ep: 0
  gp: 20
  pp: 0
save_proficiencies:
  - int
  - con
skill_proficiencies:
  - Medicine
  - Arcana
armor_proficiencies:
weapon_proficiencies:
  - Daggers
  - Darts
  - Slings
  - Quarterstaffs
  - Light Crossbows
tool_proficiencies:
  - Cook's Utensils
  - Monster Harvesting Tools
carryCapacity: 90
pushDragLift: 180
inventory:
  equipment:
    - name: Cast-iron Pan
      qty: 1
      weight: 10
      category: Utility
      rarity: Uncommon
    - name: Mama's Cookin' Spoon
      qty: 1
      weight: 1
      category: Utility
      rarity: Rare
    - name: Component/ Ingredient Pouch
      qty: 1
      weight: 2
      category: Utility
      rarity: Common
    - name: Chain Shirt
      qty: 1
      weight: 20
      category: Armor
      rarity: Common
    - name: Blue Blanket Cloak
      qty: 1
      weight: 0.5
      category: Comfort
      rarity: Rare
  backpack:
    - name: Cooking Knife
      qty: 5
      weight: 1
      category: Weapon
      rarity: Uncommon
    - name: Ration
      qty: 10
      weight: 2
      category: Consumable
      rarity: Common
    - name: Mess Kit
      qty: 1
      weight: 1
      category: Utility
    - name: Waterskin
      qty: 1
      weight: 1
      category: Utility
    - name: Tinderbox
      qty: 1
      weight: 1
      category: Utility
    - name: Rope (50ft)
      qty: 1
      weight: 1
      category: Utility
    - name: Blink Dog Stuffed Animal
      qty: 1
      weight: 0.5
      category: Comfort
      rarity: Uncommon
    - name: Yo-yo
      qty: 1
      weight: 0.3
      category: Comfort
  components:
    - name: a piece of iron
      qty: 3
      weight: 0.1
      category: Spell Material
      rarity: Common
    - name: a bit or phosphorus
      qty: 1
      weight: 0.1
      category: Spell Material
      rarity: UnCommon
    - name: Rose Petals
      qty: 5
      weight: 0.1
      category: Spell Material
      rarity: UnCommon
spells:
  - name: Bread
    level: Cantrip
    school: Transmutation
    casting_time: 1 action
    range: Touch
    duration: Instantaneous
    components:
      verbal: true
      somatic: false
    concentration: false
    notes: When holding an object, you may transform it into bread.
  - name: Dancing Lights
    level: Cantrip
    school: Illusion
    casting_time: 1 action
    range: 120 ft
    duration: 1 minute
    components:
      verbal: true
      somatic: true
      material:
        - item: a bit of phosphorus
          consumed: false
          quantity_needed: 1
    concentration: true
    notes: create up to 4 torch-sized lights. 10ft radius of dim light. Bonus action to move lights 60ft.
  - name: Mage Hand
    level: Cantrip
    school: Conjuration
    casting_time: 1 action
    range: 30 ft
    duration: 1 minute
    components:
      verbal: true
      somatic: false
    concentration: false
    notes: (1 min) Spectal hand that can carry 10lbs
  - name: Moment to Think
    level: Cantrip
    school: Transmutation
    casting_time: 1 bonus action
    range: Self
    duration: Instantaneous
    components:
      verbal: true
      somatic: false
    concentration: false
    notes: When you cast this spell, you briefly stop time for everyone but yourself. You can take one additional action and move around in your space while no time passes for other creatures. That action can be used only to take the Search or Use an Object action, or to make an Intelligence check to remember information about something. Furthermore, you can’t affect or damage any creature or object, other than objects you are wearing or carrying. If an object leaves your hand, it also becomes frozen in time.
  - name: Resilient Friendship
    level: Cantrip
    school: Enchantment
    casting_time: 1 action
    range: 5 ft
    duration: Instantaneous
    components:
      verbal: true
      somatic: false
    concentration: false
    notes: You magically assist a creature within range, granting it the benefits of the Help action. If the target you helped successfully accomplishes the task by the start of your next turn, you gain 1d4 temporary hit points, which last for 1 hour. <br> <br> The number of temporary hit points you gain increases when you reach 5th level (1d6), 11th level (1d8), and 17th level (1d10).
  - name: Silvery Barbs
    level: 1st
    school: Enchantment
    casting_time: 1 reaction
    range: 60 ft
    duration: Instantaneous
    components:
      verbal: true
      somatic: false
    concentration: false
    notes: You magically distract the triggering creature and turn its momentary uncertainty into encouragement for another creature. The triggering creature must reroll the d20 and use the lower roll. <br> <br> You can then choose a different creature you can see within range (you can choose yourself). The chosen creature has advantage on the next attack roll, ability check, or saving throw it makes within 1 minute. A creature can be empowered by only one use of this spell at a time.
  - name: Sleep
    level: 1st
    school: Enchantment
    casting_time: 1 action
    range: 60 ft
    duration: Instantaneous
    components:
      verbal: true
      somatic: true
      material:
        - item: Rose petals
          consumed: false
          quantity_needed: 3
    concentration: true
    notes: Each creature of your choice in a 5-foot-radius Sphere centered on a point within range must succeed on a Wisdom saving throw or have the Incapacitatedcondition until the end of its next turn, at which point it must repeat the save. If the target fails the second save, the target has the Unconscious condition for the duration. The spell ends on a target if it takes damage or someone within 5 feet of it takes an action to shake it out of the spell’s effect.
  - name: Healing Word
    level: 1st
    school: Abjuration
    casting_time: 1 bonus action
    range: 60 ft
    duration: Instantaneous
    components:
      verbal: true
      somatic: false
    concentration: false
    notes: A creature of your choice that you can see within range regains Hit Points equal to 2d4 plus your spellcasting ability modifier. <br> <br> The healing increases by 2d4 for each spell slot level above 1.
  - name: Delay
    level: 1st
    school: Transmutation
    casting_time: 1 action
    range: 60 ft
    duration: Instantaneous
    components:
      verbal: true
      somatic: true
      material:
        - item: Octagonal sign
          consumed: false
          quantity_needed: 1
    concentration: false
    notes: You briefly slow time for a creature of your choice that you can see within range. The target must succeed on a Wisdom saving throw or be moved to last place in the initiative order from the beginning of the next round onwards.
  - name: Bless
    level: 1st
    school: Enchantment
    casting_time: 1 action
    range: 30 ft
    duration: 1 minute
    components:
      verbal: true
      somatic: true
      material:
        - item: a Holy Symbol worth 5gp
          consumed: false
          quantity_needed: 1
    concentration: true
    notes: You bless up to three creatures of your choice within range. Whenever a target makes an attack roll or a saving throw before the spell ends, the target can roll a d4 and add the number rolled to the attack roll or saving throw. <br> <br> When you cast this spell using a spell slot of 2nd level or higher, you can target one additional creature for each slot level above 1st.
  - name: Heat Metal
    level: 2nd
    school: Transmutation
    casting_time: 1 action
    range: 60 ft
    duration: Instantaneous
    components:
      verbal: true
      somatic: true
      material:
        - item: a piece of iron
          consumed: false
          quantity_needed: 1
    concentration: true
    notes: Choose a manufactured metal object, such as a metal weapon or a suit of heavy or medium metal armor, that you can see within range. You cause the object to glow red-hot. Any creature in physical contact with the object takes 2d8 fire damage when you cast the spell. Until the spell ends, you can use a bonus action on each of your subsequent turns to cause this damage again. <br> <br> If a creature is holding or wearing the object and takes the damage from it, the creature must succeed on a Constitution saving throw or drop the object if it can. If it doesn’t drop the object, it has disadvantage on attack rolls and ability checks until the start of your next turn. When you cast this spell using a spell slot of 3rd level or higher, the damage increases by 1d8 for each slot level above 2nd.
  - name: Healing Spirit
    level: 2nd
    school: Conjuration
    casting_time: 1 bonus action
    range: 60 ft
    duration: 1 minute
    components:
      verbal: true
      somatic: true
    concentration: true
    notes: You call forth a nature spirit to soothe the wounded. The intangible spirit appears in a space that is a 5-foot cube you can see within range. The spirit looks like a transparent beast or fey (your choice). <br> <br> Until the spell ends, whenever you or a creature you can see moves into the spirit’s space for the first time on a turn or starts its turn there, you can cause the spirit to restore 1d6 hit points to that creature (no action required). The spirit can’t heal constructs or undead. The spirit can heal a number of times equal to 1 + your spellcasting ability modifier (minimum of twice). After healing that number of times, the spirit disappears. <br> <br> As a bonus action on your turn, you can move the spirit up to 30 feet to a space you can see. <br> <br> When you cast this spell using a spell slot of 3rd level or higher, the healing increases by 1d6 for each slot level above 2nd.
  - name: Revivify
    level: 3rd
    school: Necromancy
    casting_time: 1 action
    range: Touch
    duration: Instantaneous
    components:
      verbal: true
      somatic: true
      material:
        - item: a diamond worth 300gp
          consumed: true
          quantity_needed: 1
    concentration: false
    notes: You touch a creature that has died within the last minute. That creature returns to life with 1 hit point. This spell can't return to life a creature that has died of old age, nor can it restore any missing body parts.
  - name: Beacon of Hope
    level: 3rd
    school: Abjuration
    casting_time: 1 action
    range: 30 ft
    duration: 1 minute
    components:
      verbal: true
      somatic: true
    concentration: true
    notes: This spell bestows hope and vitality. Choose any number of creatures within range. For the duration, each target has advantage on Wisdom saving throws and death saving throws, and regains the maximum number of hit points possible from any healing.
  - name: Swap
    level: 3rd
    school: Void
    casting_time: 1 action (ritual)
    range: 60 ft (ritual 1000 ft)
    duration: Instantaneous
    components:
      verbal: true
      somatic: true
    concentration: false
    notes: As long as you know the location of the target, you can swap spaces with it. Can be no more than one size smaller or larger. <br> <br> When you cast this spell using a spell slot of 4th level or higher, the range increases by 15ft for each level above 3rd.
  - name: Spirit Guardians
    level: 3rd
    school: Conjuration
    casting_time: 1 action
    range: Self (15ft radius)
    duration: 10 minutes
    components:
      verbal: true
      somatic: true
      material:
        - item: a Holy Symbol worth 5gp
          consumed: false
          quantity_needed: 1
    concentration: true
    notes: Protective spirits flit around you in a 15-foot Emanation for the duration. If you are good or neutral, their spectral form appears angelic or fey (your choice). When you cast this spell, you can designate creatures to be unaffected by it. Any other creature’s Speed is halved in the Emanation. You may choose your effect. <br> <br> 1. Whenever the Emanation enters a creature’s space and whenever a creature enters the Emanation or ends its turn there, the creature must make a Wisdom saving throw. On a failed save, the creature takes 3d8 Radiant damage (if you are good or neutral) or 3d8 Necrotic damage (if you are evil). On a successful save, the creature takes half as much damage. A creature makes this save only once per turn. <br> <br> 2. Up to three choosen friendly creatures are protected and Armor Class increases by 3 for the duration that they are in the area. <br> <br> The damage increases by 1d8 or AC increases by 2 for each spell slot level above 3.
abilities:
  - name: Unarmed Attack
    description: Hit. +0 Damage. 0
    type: Actions
  - name: Mama's Cookin' Spoon
    description: +1 to attack roll and damage (deals additional extra 1d6). When an attack is made with this spoon, the target must make a Constitution saving throw (DC 13). On a failure, the target becomes Hungry. a Hungry target gets -1 on Wisdom and Constitution saving throws. You  have +1 to your spell attacks and +1 to your spell DC. You have the Chef feat.
    type: Other
  - name: Chef Feat (Cook Treat)
    description: With one hour of work or when you finish a long rest, you can cook a number of treats equal to your proficiency bonus. These special treats last 8 hours after being made. A creature can use a bonus action to eat one of those treats to gain temporary hit points equal to your proficiency bonus.
    type: Other
    uses_max: 3
    reset: Long
  - name: Chef Feat (Special Food)
    description: As part of a short rest, you can cook special food, provided you have ingredients and cook’s utensils on hand. You can prepare enough of this food for a number of creatures equal to 4 + your proficiency bonus. At the end of the short rest, any creature who eats the food and spends one or more Hit Dice to regain hit points regains an extra 1d8 hit points.
    type: Other
    uses_max: 7
    reset: Short
racial_abilities:
  - name: Brave
    description: You have Advantage on saving throws you make to avoid or end the Frightened condition.
  - name: Halfling Nimbleness
    description: You can move through the space of any creature that is a size larger than you, but you can’t stop in the same space.
  - name: Luck
    description: When you roll a 1 on the d20 of a D20 Test, you can reroll the die, and you must use the new roll.
  - name: Naturally Stealthy
    description: You can take the Hide action even when you are obscured only by a creature that is at least one size larger than you.
  - name: Chef (Background)
    description: For any roll relating to finding food or ingredients add 2d6 to your roll and for any food you make add 1d4 Hit Points to the creature who consumed the dish. <br> <br> In your pursuit of a veteran palate you have tasted foods both fair and foul, and thus have grown resistant to them. You have advantage on any Constitution saving throw involving consumption of materials or liquids including potions and poisons.
class_abilities:
  - name: Spellcasting
    description: Mana Pool. Rather than using spell slots, UnForsaken draw upon a mana pool — a reservoir of pure magical energy that fuels your spellcasting. The UnForsaken table shows how many mana points you have at each level. This pool determines the total magical energy available to you for casting spells. <br> <br> >Spell Level Costs. The mana cost to cast a spell is equal to its level. For example, a 1st-level spell costs 1 mana point, while a 5th-level spell costs 5 mana points. <br> >Overchanneling.** You can only cast a spell if you have enough mana to meet its level cost. You cannot “partially” cast spells or go into negative mana. <br> >Long Rest Recovery.** You regain up to 75 Mana points. If your max mana pool is less than 75, then it is repleshed to full. <br> >Short Rest Recovery.** You regain Mana points equal to your proficiency bonus.
  - name: Weave Manipulation
    description: As a bonus action, choose one of the following effects. You can use this feature a number of times equal to your proficiency bonus, and you regain all uses when you finish a long rest. <br> <br> Arcane Compression. Choose a spell you know of 3rd level or lower. For the next minute, reduce its mana cost by 1 (minimum 1). This reduction applies every time you cast that specific spell during the duration. <br> <br> Spell Stretch. Choose a spell you know of 2nd level or lower. When you cast it, you may spend 1 additional mana point to enhance its potency. <br> >Increase its range by double. <br> >Extend its duration by 1 minute (if its duration is 1 minute or longer). <br> >Apply advantage on a saving throw DC against the spell. <br> >Deal maximum damage/healing with one die of your choice. <br> <br> Mana Transer. As an action, you can transfer up to 3 mana points from your pool to a willing creature within 5 feet. That creature immediately regains expended spell slots whose combined level does not exceed the amount of mana transferred.
    uses_max: 3
    reset: Long
  - name: Residual Pain
    description: When a creature succeeds on a saving throw against one of your spells and the spell would normally deal no damage on a success, the creature instead takes half damage. If the spell already deals half damage on a successful save, that damage cannot be reduced or negated in any way.
class:
  - UnForsaken
---


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
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>> ---|---|
>> **Played By** |  `INPUT[textArea:playedBy]` |
>> **Pronounced** |  `INPUT[textArea:pronounced]` |
>> **Aliases** | `INPUT[list:aliases]` |
>> **Ancestry** | `INPUT[Ancestry][suggester:ancestry]` |
>> **Heritage** | `INPUT[Heritage][suggester:heritage]` |
> **Creature Type** | `INPUT[textArea:ancestry]` |
> **Creature Sub-Type** | `INPUT[textArea:heritage]` |
>> **Gender** | `INPUT[Gender][suggester:gender]` |
>> **Age** | `INPUT[number:age]` |
>> **Alignment** | `INPUT[Alignment][suggester:alignment]` |
>
>> [!metadata|metadataoption]- PC Info
>> #### PC Info
>>  |
>>---|---|
>> **Languages** | `INPUT[Languages][inlineListSuggester:languages]` |
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"98 Templates"), useLinks(partial)):organizations]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"98 Templates"), useLinks(partial)):religions]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"98 Templates"), useLinks(partial)):ownedLocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"98 Templates"), useLinks(partial)):currentLocation]` |
>> **Condition** | `INPUT[Condition][inlineListSuggester:condition]` |
>
>> [!metadata|metadataoption]- Skill Info
>> **Class** | `INPUT[list:class]` |
>> #### Ability Scores
>>  |
>> ---|---|
>> **Strength** | `INPUT[number:str]` |
>> **Dexterity** |  `INPUT[number:dex]` |
>> **Constitution** |  `INPUT[number:con]` |
>> **Intelligence** |  `INPUT[number:int]` |
>> **Wisdom** |  `INPUT[number:wis]` |
>> **Charisma** |  `INPUT[number:cha]` |
>> #### Basic Stats
>>  |
>> ---|---|
>> **Speed** |  `INPUT[number:speed]` |
>> **Initiative** |  `INPUT[number:initiative_mod]` |
>> **Proficiency Bonus** |  `INPUT[number:prof_bonus]` |
>> **Armor Class** |  `INPUT[number:ac]` |
>> #### Proficiencies
>>  |
>> ---|---|
>> **Ability Proficiencies** | `INPUT[AbilityProf][inlineListSuggester:save_proficiencies]` |
>> **Skill Proficiencies** | `INPUT[SkillProf][inlineListSuggester:skill_proficiencies]`  |
>> **Armor Proficiencies** | `INPUT[list:armor_proficiencies]` |
>> **Weapon Proficiencies** | `INPUT[list:weapon_proficiencies]` |
>> **Tool Proficiencies** | `INPUT[list:tool_proficiencies]` |
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"98 Templates")):whichParty]` |
>> **Party 1 Relation** | `INPUT[party1Relation][inlineListSuggester:party1Relation]` |
>
>> [!metadata|metadataoption]- Editable Data
>> #### Editable Data
>>  |
>> ---|---|
>> **Current Hit Points** | `INPUT[number:hp_current]` |
>> **Max Hit Points** | `INPUT[number:hp_max]` |
>> **Current Mana** | `INPUT[number:mana_current]` |
>> **Max Mana** | `INPUT[number:mana_max]` |
>> **Current Platinum Coins** | `INPUT[number:coins.pp]` |
>> **Current Gold Coins** | `INPUT[number:coins.gp]` |
>> **Current Electrum Coins** | `INPUT[number:coins.ep]` |
>> **Current Silver Coins** | `INPUT[number:coins.sp]` |
>> **Current Copper Coins** | `INPUT[number:coins.cp]` |


> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> 
> ###### **Played By:** <font color="#ffc000">`VIEW[{playedBy}][text]`</font>
> 
> # Bio
> | | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Ancestry** | `VIEW[{ancestry}][link]` |
> | **Heritage** | `VIEW[{heritage}][link]` |
> | **Gender** | `VIEW[{gender}]` |
> | **Age** | `VIEW[{age}]` yrs |
> 
> # Details
> | | |
> |---|---|
> | **Class** | `VIEW[{class}][text]` |
> | **Languages** | `VIEW[{languages}][link]` |
> | **Occupations** | `VIEW[{occupation}][text]` |
> | **Organizations** | `VIEW[{organizations}][link]` |
> | **Religions** | `VIEW[{religions}][link]` |
> | **Condition** | `VIEW[{condition}]` |
> | **Current Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`
**`VIEW[{heritage}][link]`** | **`VIEW[{class}][text]`** | Level: **5** 

**Physical Appearance:** A small halfling adventurer with soft, androgynous features and an innocent expression. They have thick wavy stark white hair that falls all the way to their ankles, with small round ears poking through. Their skin is so fair that it may or may not glow, and their large brilliantly blue eyes and dimples give them a youthful, kind look, easily mistaken for a human child. Their proportions are slightly exaggerated for a halfling — short and sturdy with large bare feet. They wear an oversized chainmail shirt that hangs to their knees and flops over their hands, and a blue patched cloak with tasseled blanket edges fastened by an old ornate pin. In one hand, they hold a well- used full-sized human wooden spoon like a weapon, and in the other, a cast-iron pan attached to a leather strap handle like a shield.


```dataviewjs
// ABILITY SCORE RENDERER for Obsidian (DataviewJS)
// Put below your YAML frontmatter. Requires Dataview plugin enabled.

// Utility: calculate modifier from score
const calcMod = score => {
  if (score === undefined || score === null || isNaN(score)) return null;
  return Math.floor((Number(score) - 10) / 2);
};

// Safe access to frontmatter
const f = dv.current()?.file?.frontmatter || {};

// Build data array for iteration
const abilities = [
  { key: "str", label: "STR" },
  { key: "dex", label: "DEX" },
  { key: "con", label: "CON" },
  { key: "int", label: "INT" },
  { key: "wis", label: "WIS" },
  { key: "cha", label: "CHA" }
].map(a => {
  const score = f[a.key];
  const mod = (score !== undefined && !isNaN(score)) ? calcMod(score) : null;
  return { label: a.label, score: score ?? "", mod: mod };
});

// Helper to format modifier string
const formatMod = m => {
  if (m === null || m === "") return "";
  return (m >= 0 ? `+${m}` : `${m}`);
};

// HTML for the block
let html = `
<div class="char-abilities" style="display: grid; grid-template-columns: repeat(6, 1fr); gap: 10px; align-items: center; max-width: 780px; margin: 6px auto;">
`;

// each ability becomes a small card with circle + text
for (const ab of abilities) {
  html += `
  <div class="ability-card" style="text-align:center; font-family: inherit;">
    <div class="ability-circle" style="
        width:68px;
        height:68px;
        line-height:68px;
        border-radius:50%;
        border:2px solid var(--background-modifier-border);
        display:inline-block;
        vertical-align:middle;
        font-weight:700;
        font-size:20px;
    ">${ab.score}</div>
    <div style="margin-top:6px; font-size:12px;">
      <div style="font-weight:700;">${ab.label}</div>
      <div style="color:var(--muted-text);">${formatMod(ab.mod)}</div>
    </div>
  </div>
  `;
}

html += `</div>`;


// render
dv.el("div", html);

// Add interactivity for HP buttons
const hpDisplay = document.getElementById("hp-display");
document.getElementById("hp-minus")?.addEventListener("click", () => {
  if (hpCurrent > 0) hpCurrent--;
  hpDisplay.innerText = `${hpCurrent} / ${hpMax}`;
});
document.getElementById("hp-plus")?.addEventListener("click", () => {
  if (hpCurrent < hpMax) hpCurrent++;
  hpDisplay.innerText = `${hpCurrent} / ${hpMax}`;
});

```

```dataviewjs
// D&D Character Combat Stats Display (Obsidian DataviewJS)

// Grab frontmatter
const f = dv.current()?.file?.frontmatter || {};

// Helper to show "undefined" fields cleanly
const safe = v => (v !== undefined && v !== null) ? v : "--";

// Build HTML
let html = `
<div class="char-vitals" style="
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
  gap: 12px;
  max-width: 780px;
  margin: 14px auto;
  text-align: center;
  font-family: inherit;
">
`;

// Define boxes
const stats = [
  { label: "Armor Class", value: f.ac, symbol: "🛡️" },
  { label: "Hit Points", value: `${safe(f.hp_current)} / ${safe(f.hp_max)}`, symbol: "❤️" },
  { label: "Mana", value: `${safe(f.mana_current)} / ${safe(f.mana_max)}`, symbol: "⚗️" },
  { label: "Initiative", value: (f.initiative_mod >= 0 ? `+${f.initiative_mod}` : f.initiative_mod), symbol: "⚡" },
  { label: "Speed", value: `${safe(f.speed)} ft.`, symbol: "👣" },
  { label: "Proficiency", value: `+${safe(f.prof_bonus)}`, symbol: "🎯" },
];

// Render
for (const stat of stats) {
  html += `
  <div class="vital-box" style="
    flex: 1 1 120px;
    border: 2px solid var(--background-modifier-border);
    border-radius: 12px;
    padding: 8px 0;
    background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.02));
    box-shadow: var(--shadow-small);
  ">
    <div style="font-size: 22px;">${stat.symbol}</div>
    <div style="font-size: 20px; font-weight: 700;">${safe(stat.value)}</div>
    <div style="font-size: 12px; color: var(--muted-text);">${stat.label}</div>
  </div>`;
}

html += `</div>`;

dv.el("div", html);


```

## Skills
````col
```dataviewjs
// === Passive Senses Block ===
// Calculates passive perception, investigation, and insight
// Uses skill proficiency + ability modifiers

// Helper functions
const calcMod = score => Math.floor((score - 10) / 2);
const fmt = n => (n >= 0 ? `+${n}` : `${n}`);
const safe = v => (v !== undefined && v !== null ? v : "--");

// Access frontmatter
const f = dv.current()?.file?.frontmatter || {};
const prof = f.prof_bonus ?? 0;
const skills = f.skill_proficiencies ?? [];

// Ability modifiers
const mods = {
  wis: calcMod(f.wis ?? 10),
  int: calcMod(f.int ?? 10)
};

// Compute passives
const senses = [
  { name: "Passive Perception", ability: "wis", skill: "perception" },
  { name: "Passive Investigation", ability: "int", skill: "investigation" },
  { name: "Passive Insight", ability: "wis", skill: "insight" }
].map(s => {
  const base = 10 + mods[s.ability];
  const bonus = skills.includes(s.skill) ? prof : 0;
  const total = base + bonus;
  return { ...s, total, proficient: skills.includes(s.skill) };
});

// HTML layout
let html = `
<div class="char-senses" style="
  max-width: 450px;
  margin: 10px auto;
  border: 2px solid var(--background-modifier-border);
  border-radius: 12px;
  padding: 10px 16px;
  background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.02));
  box-shadow: var(--shadow-small);
">
  <h3 style="text-align:center; margin-top:0;">Senses</h3>
  <table style="width:100%; border-collapse: collapse; font-size:14px;">
    <thead>
      <tr style="background: var(--background-secondary); text-align:left;">
        <th style="padding:4px;">Prof</th>
        <th style="padding:4px;">Sense</th>
        <th style="padding:4px; text-align:right;">Score</th>
      </tr>
    </thead>
    <tbody>
`;

for (const s of senses) {
  html += `
  <tr style="border-top:1px solid var(--background-modifier-border);">
    <td style="text-align:center; padding:4px;">${s.proficient ? "✔️" : "❌"}</td>
    <td style="padding:4px;">${s.name}</td>
    <td style="text-align:right; padding:4px;"><b>${s.total}</b></td>
 </tr>`;
}

html += `
    </tbody>
  </table>
  <div style="max-width:780px;margin:8px auto 0; display:flex; justify-content:center; gap:12px; font-size:13px;">
    <div><strong>Additional Senses:</strong> None</div>
  </div>
</div>
`;

dv.el("div", html);

```

```dataviewjs
// === Saving Throws Block ===
// Calculates modifiers + proficiency and displays a clean table

// Helper functions
const calcMod = score => Math.floor((score - 10) / 2);
const fmtMod = n => (n >= 0 ? `+${n}` : `${n}`);
const safe = v => (v !== undefined && v !== null ? v : "--");

// Access frontmatter
const f = dv.current()?.file?.frontmatter || {};
const prof = f.prof_bonus ?? 0;
const profs = f.save_proficiencies ?? [];

// Define ability set
const abilities = [
  { key: "str", label: "Strength" },
  { key: "dex", label: "Dexterity" },
  { key: "con", label: "Constitution" },
  { key: "int", label: "Intelligence" },
  { key: "wis", label: "Wisdom" },
  { key: "cha", label: "Charisma" }
];

// Build HTML
let html = `
<div class="saving-throws" style="
  max-width: 450px;
  margin: 20px auto;
  border: 2px solid var(--background-modifier-border);
  border-radius: 12px;
  padding: 10px 16px;
  background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.02));
  box-shadow: var(--shadow-small);
">
  <h3 style="text-align:center; margin-top:0;">Saving Throws</h3>
  <table style="width:100%; border-collapse: collapse; font-size: 14px;">
    <thead>
      <tr style="background: var(--background-secondary); text-align:left;">
        <th style="padding: 4px;">Prof</th>
        <th style="padding: 4px;">Ability</th>
        <th style="padding: 4px; text-align:right;">Modifier</th>
      </tr>
    </thead>
    <tbody>
`;

for (const ab of abilities) {
  const score = f[ab.key];
  const mod = calcMod(score ?? 10);
  const isProf = profs.includes(ab.key);
  const total = mod + (isProf ? prof : 0);

  html += `
  <tr style="border-top: 1px solid var(--background-modifier-border);">
    <td style="padding: 3px 4px; text-align:center;">${isProf ? "✔️" : "❌"}</td>
    <td style="padding: 3px 4px;">${ab.label}</td>
    <td style="padding: 3px 4px; text-align:right;"><b>${fmtMod(total)}</b></td>
  </tr>
  `;
}

html += `
    </tbody>
  </table>
    <div style="max-width:780px;margin:8px auto 0; display:flex; justify-content:center; gap:12px; font-size:13px;">
    <div><strong>Advantage:</strong> to avoid or end the Frightened condition</div>
    <div><strong>Advantage:</strong> on CON involving consumption of potions & poisons</div>
    <div><strong>Disdvantage:</strong> on STR and DEX when non proficient armor worn</div>
  </div>
</div>
`;

dv.el("div", html);
```

```dataviewjs
// === Proficiencies & Training Box ===
// Displays armor, weapon, tool, and language proficiencies from frontmatter

const f = dv.current()?.file?.frontmatter || {};

// Helper function for clean rendering
const list = arr => {
 if (!arr || arr.length === 0) return "<i>None</i>";
 if (typeof arr === "string") return arr;
 return arr.join(", ");
};

// HTML layout
let html = `
<div class="char-proficiencies" style="
 max-width: 450px;
  margin: 20px auto;
 border: 2px solid var(--background-modifier-border);
 border-radius: 12px;
  padding: 10px 16px;
  background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.02));
  box-shadow: var(--shadow-small);
">
  <h3 style="text-align:center; margin-top:0;">Proficiencies & Training</h3>

  <div style="margin-bottom:8px;">
    <b>Armor:</b> ${list(f.armor_proficiencies)}
  </div>
  <div style="margin-bottom:8px;">
    <b>Weapons:</b> ${list(f.weapon_proficiencies)}
  </div>
  <div style="margin-bottom:8px;">
    <b>Tools:</b> ${list(f.tool_proficiencies)}
  </div>
  <div>
    <b>Languages:</b> ${list(f.languages)}
  </div>
</div>
`;

dv.el("div", html);

```
````

```dataviewjs
//----------------------------------------------------------
// Skill Display - grouped by type
//----------------------------------------------------------
const f = dv.current().file.frontmatter;

// Helper: get ability mod
const mod = (score) => Math.floor(((score ?? 10) - 10) / 2);

// Helper: check proficiency
const hasProf = (name) => (f.skill_proficiencies || []).map(s => s.toLowerCase()).includes(name.toLowerCase());

// Helper: format modifier
const fmt = (n) => (n >= 0 ? "+" + n : n);

// Helper: calculate total
const total = (ability, proficient) => fmt(mod(f[ability]) + (proficient ? (f.prof_bonus ?? 0) : 0));

// Skill groups
const skillGroups = {
  "Physical": [
    { name: "Athletics", ability: "STR", key: "str" },
    { name: "Acrobatics", ability: "DEX", key: "dex" },
    { name: "Sleight of Hand", ability: "DEX", key: "dex" },
    { name: "Stealth", ability: "DEX", key: "dex" },
  ],
  "Knowledge": [
    { name: "Arcana", ability: "INT", key: "int" },
    { name: "History", ability: "INT", key: "int" },
    { name: "Investigation", ability: "INT", key: "int" },
    { name: "Nature", ability: "INT", key: "int" },
    { name: "Religion", ability: "INT", key: "int" },
  ],
  "Social": [
    { name: "Deception", ability: "CHA", key: "cha" },
    { name: "Intimidation", ability: "CHA", key: "cha" },
    { name: "Performance", ability: "CHA", key: "cha" },
    { name: "Persuasion", ability: "CHA", key: "cha" },
  ],
  "Perceptive": [
    { name: "Animal Handling", ability: "WIS", key: "wis" },
    { name: "Insight", ability: "WIS", key: "wis" },
    { name: "Medicine", ability: "WIS", key: "wis" },
    { name: "Perception", ability: "WIS", key: "wis" },
    { name: "Survival", ability: "WIS", key: "wis" },
  ],
};

// HTML layout
let html = `
<div style="
  display:grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap:12px;
  margin-top: 10px;
">
`;

for (const [group, skills] of Object.entries(skillGroups)) {
  html += `
  <div style="
    border:1px solid var(--background-modifier-border);
    border-radius:10px;
    padding:8px 10px;
    background:rgba(255,255,255,0.02);
  ">
    <h4 style="text-align:center; margin:4px 0;">${group}</h4>
    <table style="width:100%; border-collapse:collapse; font-size:14px;">
  `;

  for (const s of skills) {
    const proficient = hasProf(s.name);
    html += `
      <tr>
        <td style="width:22px; text-align:center;">${proficient ? "🟢" : "⚪"}</td>
        <td>${s.name} (${s.ability})</td>
        <td style="text-align:right;">${total(s.key, proficient)}</td>
      </tr>
    `;
  }

  html += `</table>`;

  // 🧠 Custom section-specific notes
  if (group === "Physical") {
    html += `
    <div style="max-width:780px;margin:8px auto 0; display:flex; justify-content:center; gap:12px; font-size:13px; opacity:0.8;">
      <div><strong>Disadvantage:</strong> when not proficient with armor worn (Chain Shirt)</div>
    </div>
    `;
  }

  html += `</div>`;
}

html += `</div>`;
dv.el("div", html);

```

## Actions
```dataviewjs
// === D&D Character Abilities Display (Three Columns Styled + Collapsible Cards + Global Rest Buttons) ===

// --- Frontmatter ---
const f = dv.current()?.file?.frontmatter || {};
const abilities = f.abilities || [];
const racialAbilities = f.racial_abilities || [];
const classAbilities = f.class_abilities || [];

// --- LocalStorage Helpers ---
const saveState = (key, val) =>
  localStorage.setItem(`dnd_${dv.current().file.path}_${key}`, JSON.stringify(val));
const loadState = (key, fallback) => {
  const val = localStorage.getItem(`dnd_${dv.current().file.path}_${key}`);
  return val ? JSON.parse(val) : fallback;
};

// --- Collapsible Card Builder with Styled Borders ---
function buildCard(action) {
  const stateKey = `${action.name.replace(/\s+/g, "_")}_uses`;
  const saved = loadState(stateKey, Array(action.uses_max || 0).fill(false));

  const card = document.createElement("div");
  card.className = "ability-card";
  card.style.border = "2px solid var(--background-modifier-border)";
  card.style.borderRadius = "12px";
  card.style.boxShadow = "0 3px 8px rgba(0,0,0,0.25)";
  card.style.overflow = "hidden";
  card.style.transition = "all 0.3s ease";
  card.style.backgroundColor = "var(--background-secondary)";
  card.style.minWidth = "220px";
  card.style.flex = "1 1 220px";

  // Header (always visible)
  const header = document.createElement("div");
  header.style.padding = "10px";
  header.style.cursor = "pointer";
  header.style.fontWeight = "700";
  header.style.textAlign = "center";
  header.style.backgroundColor = "var(--background-primary-alt)";
  header.style.borderBottom = "1px solid var(--background-modifier-border)";
  header.innerText = action.name;

  header.addEventListener("mouseover", () => {
    header.style.backgroundColor = "var(--background-modifier-hover)";
  });
  header.addEventListener("mouseout", () => {
    header.style.backgroundColor = "var(--background-primary-alt)";
  });

  card.appendChild(header);

  // Content (hidden until expanded)
  const content = document.createElement("div");
  content.style.maxHeight = "0";
  content.style.overflow = "hidden";
  content.style.transition = "max-height 0.3s ease, padding 0.3s ease";
  content.style.padding = "0 10px";

  if (action.description) {
    const descDiv = document.createElement("div");
    descDiv.innerHTML = action.description;
    descDiv.style.fontSize = "13px";
    descDiv.style.color = "var(--muted-text)";
    descDiv.style.textAlign = "center";
    descDiv.style.marginTop = "6px";
    content.appendChild(descDiv);
  }

  // Charge boxes
  if (action.uses_max && action.uses_max > 0) {
    const boxDiv = document.createElement("div");
    boxDiv.style.display = "flex";
    boxDiv.style.justifyContent = "center";
    boxDiv.style.gap = "6px";
    boxDiv.style.margin = "8px 0";
    saved.forEach((used, i) => {
      const box = document.createElement("div");
      box.style.width = "22px";
      box.style.height = "22px";
      box.style.borderRadius = "5px";
      box.style.cursor = "pointer";
      box.style.border = "2px solid var(--background-modifier-border)";
      box.style.background = used ? "rgba(255,0,0,0.5)" : "rgba(0,255,0,0.15)";
      box.dataset.index = i;
      box.dataset.key = stateKey;
      box.addEventListener("click", e => {
        e.stopPropagation();
        const idx = +e.target.dataset.index;
        const key = e.target.dataset.key;
        const cur = loadState(key, []);
        cur[idx] = !cur[idx];
        saveState(key, cur);
        e.target.style.background = cur[idx]
          ? "rgba(255,0,0,0.5)"
          : "rgba(0,255,0,0.15)";
      });
      boxDiv.appendChild(box);
    });
    content.appendChild(boxDiv);

    const footer = document.createElement("div");
    footer.style.fontSize = "12px";
    footer.style.color = "var(--muted-text)";
    footer.style.textAlign = "center";
    footer.style.marginBottom = "8px";
    footer.innerText = `${action.uses_max} uses · resets on ${action.reset?.toLowerCase() || "long"} rest`;
    content.appendChild(footer);
  }

  card.appendChild(content);

  // Toggle collapse
  let expanded = false;
  header.addEventListener("click", () => {
    expanded = !expanded;
    content.style.maxHeight = expanded ? content.scrollHeight + 30 + "px" : "0";
    content.style.padding = expanded ? "8px 10px" : "0 10px";
  });

  return card;
}

// --- Group Actions by Type ---
const grouped = {};
abilities.forEach(ab => {
  if (!grouped[ab.type]) grouped[ab.type] = [];
  grouped[ab.type].push(ab);
});

// --- Main Container ---
const main = dv.el("div", "", { cls: "three-col-abilities" });
main.style.display = "flex";
main.style.flexWrap = "wrap";
main.style.gap = "20px";
main.style.justifyContent = "space-between";
main.style.maxWidth = "1600px";
main.style.margin = "20px auto";

// --- Build Column ---
function buildColumn(titleText, data, isGrouped = false) {
  const col = document.createElement("div");
  col.style.flex = "1 1 30%";
  col.style.display = "flex";
  col.style.flexDirection = "column";
  col.style.gap = "12px";

  const title = document.createElement("h2");
  title.innerText = titleText;
  title.style.margin = "0 0 6px 0";
  title.style.textAlign = "center";
  col.appendChild(title);

  if (isGrouped) {
    const order = ["Actions", "Bonus Actions", "Reactions", "Other"];
    order.forEach(type => {
      const list = data[type] || [];
      if (!list.length) return;

      const typeHeader = document.createElement("h3");
      typeHeader.innerText = type;
      typeHeader.style.textAlign = "center";
      typeHeader.style.marginBottom = "6px";
      col.appendChild(typeHeader);

      const flexWrap = document.createElement("div");
      flexWrap.style.display = "flex";
      flexWrap.style.flexWrap = "wrap";
      flexWrap.style.gap = "10px";
      list.forEach(item => flexWrap.appendChild(buildCard(item)));
      col.appendChild(flexWrap);
    });
  } else {
    const flexWrap = document.createElement("div");
    flexWrap.style.display = "flex";
    flexWrap.style.flexWrap = "wrap";
    flexWrap.style.gap = "10px";
    if (data.length) data.forEach(item => flexWrap.appendChild(buildCard(item)));
    else {
      const none = document.createElement("p");
      none.style.color = "var(--text-faint)";
      none.innerText = "None listed.";
      flexWrap.appendChild(none);
    }
    col.appendChild(flexWrap);
  }

  main.appendChild(col);
}

// --- Build Columns ---
buildColumn("🗡️ Actions & Combat Options", grouped, true);
buildColumn("🧬 Racial Abilities", racialAbilities);
buildColumn("📜 Class Abilities", classAbilities);

dv.container.appendChild(main);

// --- Global Rest Buttons ---
const restDiv = dv.el("div", "", {cls:"rest-buttons"});
restDiv.style.display = "flex";
restDiv.style.justifyContent = "center";
restDiv.style.gap = "12px";
restDiv.style.margin = "16px auto";

const shortBtn = document.createElement("button");
shortBtn.innerText = "Short Rest";
shortBtn.style.padding = "6px 12px";
shortBtn.style.fontWeight = "600";
shortBtn.style.borderRadius = "6px";
shortBtn.style.cursor = "pointer";
shortBtn.style.border = "1px solid var(--background-modifier-border)";

const longBtn = document.createElement("button");
longBtn.innerText = "Long Rest";
longBtn.style.padding = "6px 12px";
longBtn.style.fontWeight = "600";
longBtn.style.borderRadius = "6px";
longBtn.style.cursor = "pointer";
longBtn.style.border = "1px solid var(--background-modifier-border)";

restDiv.appendChild(shortBtn);
restDiv.appendChild(longBtn);
dv.container.appendChild(restDiv);

// --- Reset function affecting all three columns ---
function resetAll(type) {
  const allAbilities = [...abilities, ...racialAbilities, ...classAbilities];
  allAbilities.forEach(a => {
    if (!a.uses_max) return;
    if (type === "Short" && a.reset === "Short") {
      saveState(a.name.replace(/\s+/g,'_')+"_uses", Array(a.uses_max).fill(false));
    }
    if (type === "Long") {
      saveState(a.name.replace(/\s+/g,'_')+"_uses", Array(a.uses_max).fill(false));
    }
  });
  location.reload();
}

shortBtn.addEventListener("click", ()=>resetAll("Short"));
longBtn.addEventListener("click", ()=>resetAll("Long"));


```

## Spells
```dataviewjs
// === D&D Spellbook Display with Collapsible Cards + Nested Components Support ===

const f = dv.current()?.file?.frontmatter || {};
const spells = f.spells ?? [];
const spellSaveDC = f.spell_save_dc ?? "-";
const spellAttackMod = f.spell_attack_mod ?? "-";

if (!spells.length) {
  dv.paragraph("No spells found.");
} else {

  // --- Level normalization ---
  function normalizeLevel(lvl) {
    if (!lvl) return "Unknown";
    const lower = lvl.toLowerCase();
    if (lower === "cantrip" || lower === "cantrips") return "Cantrips";
    const num = lvl.replace(/[^0-9]/g, "");
    const suffix = num === "1" ? "st" : num === "2" ? "nd" : num === "3" ? "rd" : "th";
    return `${num}${suffix}-Level Spells`;
  }

  // --- Group spells by level ---
  const grouped = {};
  spells.forEach(spell => {
    const lvl = normalizeLevel(spell.level);
    if (!grouped[lvl]) grouped[lvl] = [];
    grouped[lvl].push(spell);
  });

  // --- Sort levels ---
  const order = ["Cantrips","1st-Level Spells","2nd-Level Spells","3rd-Level Spells","4th-Level Spells","5th-Level Spells","6th-Level Spells","7th-Level Spells","8th-Level Spells","9th-Level Spells"];
  const sortedLevels = Object.keys(grouped).sort((a,b) => order.indexOf(a) - order.indexOf(b));

  // --- Helper: format nested components ---
  function formatComponents(components) {
    if (!components) return "-";
    const parts = [];
    if (components.verbal) parts.push("V");
    if (components.somatic) parts.push("S");

    if (components.material && components.material.length > 0) {
      const materials = components.material.map(m => {
        let text = m.item ?? "Unknown item";
        if (m.consumed) text += " (consumed)";
        if (m.quantity_needed && m.quantity_needed > 1) text += ` x${m.quantity_needed}`;
        return text;
      }).join(", ");
      parts.push(`M (${materials})`);
    }

    return parts.join(", ") || "-";
  }

  // --- Collapsible Spell Card Builder ---
  function buildSpellCard(spell) {
    const card = document.createElement("div");
    card.style.border = "2px solid var(--background-modifier-border)";
    card.style.borderRadius = "10px";
    card.style.boxShadow = "0 2px 6px rgba(0,0,0,0.2)";
    card.style.backgroundColor = "var(--background-secondary)";
    card.style.overflow = "hidden";
    card.style.minWidth = "250px";
    card.style.flex = "1 1 250px";
    card.style.transition = "all 0.3s ease";

    // Header
    const header = document.createElement("div");
    header.style.padding = "10px";
    header.style.cursor = "pointer";
    header.style.fontWeight = "700";
    header.style.textAlign = "center";
    header.style.backgroundColor = "var(--background-primary-alt)";
    header.style.borderBottom = "1px solid var(--background-modifier-border)";
    header.innerText = spell.name;

    header.addEventListener("mouseover", () => {
      header.style.backgroundColor = "var(--background-modifier-hover)";
    });
    header.addEventListener("mouseout", () => {
      header.style.backgroundColor = "var(--background-primary-alt)";
    });

    card.appendChild(header);

    // Content (collapsed initially)
    const content = document.createElement("div");
    content.style.maxHeight = "0";
    content.style.overflow = "hidden";
    content.style.transition = "max-height 0.3s ease, padding 0.3s ease";
    content.style.padding = "0 10px";

    // Spell Details
    const details = document.createElement("div");
    details.style.fontSize = "12px";
    details.style.color = "var(--text-muted)";
    details.style.marginTop = "6px";
    details.style.lineHeight = "1.3";

    details.innerHTML = `
      <div style="font-weight:700; text-align:center;">${spell.school ?? ""}</div>
      <div><b>Casting Time:</b> ${spell.casting_time ?? "-"}</div>
      <div><b>Range:</b> ${spell.range ?? "-"}</div>
      <div><b>Duration:</b> ${spell.duration ?? "-"}</div>
      <div><b>Components:</b> ${formatComponents(spell.components)}</div>
      ${spell.concentration ? `<div style="color:#c0392b;"><b>⚠ Concentration</b></div>` : ""}
      <div style="margin-top:4px;"><b>Notes:</b> ${spell.notes ?? "-"}</div>
    `;

    content.appendChild(details);
    card.appendChild(content);

    // Toggle collapse
    let expanded = false;
    header.addEventListener("click", () => {
      expanded = !expanded;
      content.style.maxHeight = expanded ? content.scrollHeight + 20 + "px" : "0";
      content.style.padding = expanded ? "8px 10px" : "0 10px";
    });

    return card;
  }

  // --- Render Spellbook ---
  const container = dv.el("div");
  container.style.display = "flex";
  container.style.flexDirection = "column";
  container.style.gap = "12px";
  container.style.maxWidth = "1200px";
  container.style.margin = "16px auto";

  // Top: Spell Save DC / Attack Modifier
  const topInfo = document.createElement("div");
  topInfo.style.display = "flex";
  topInfo.style.justifyContent = "center";
  topInfo.style.gap = "24px";
  topInfo.style.fontWeight = "600";
  topInfo.style.marginBottom = "12px";
  topInfo.innerHTML = `<div>Spell Save DC: <b>${spellSaveDC}</b></div><div>Spell Attack: <b>${spellAttackMod}</b></div>`;
  container.appendChild(topInfo);

  sortedLevels.forEach(level => {
    const emoji = level === "Cantrips" ? "✨" : "📜";
    const levelDiv = document.createElement("div");
    levelDiv.style.marginBottom = "16px";

    const h4 = document.createElement("h4");
    h4.innerText = `${emoji} ${level}`;
    h4.style.marginBottom = "6px";
    levelDiv.appendChild(h4);

    const flexWrap = document.createElement("div");
    flexWrap.style.display = "flex";
    flexWrap.style.flexWrap = "wrap";
    flexWrap.style.gap = "8px";
    flexWrap.style.alignItems = "flex-start";
    flexWrap.style.justifyContent = "flex-start";

    grouped[level].forEach(spell => flexWrap.appendChild(buildSpellCard(spell)));
    levelDiv.appendChild(flexWrap);
    container.appendChild(levelDiv);
  });

  dv.container.appendChild(container);
}


```

## Inventory

```dataviewjs
// Full Inventory + Coins + Weight Meter + Component Pouch + Spell Component Tracker
// Drop in dataviewjs block. Works with flexible frontmatter formats (see examples).

const f = dv.current()?.file?.frontmatter || {};

// --- Config / Defaults ---
const coins = { cp:0, sp:0, ep:0, gp:0, pp:0, ...f.coins };
const backpackBaseWeight = Number(f.backpackBaseWeight ?? 5);
const smallCategories = new Set(["Utility","Comfort","Consumable"]);
const carryCapacity = Number(f.carryCapacity ?? 90);
const pushDragLift = Number(f.pushDragLift ?? 180);

// coin weight (lbs per coin)
const coinWeight = 0.02;
const rarityColors = {
  "Common": "inherit",
  "Uncommon": "#2ecc71",
  "Rare": "#3498db",
  "Very Rare": "#9b59b6",
  "Legendary": "#f1c40f",
  "Artifact": "#e74c3c"
};

// --- Helpers ---
const n = v => (v === undefined || v === null) ? 0 : Number(v);
const human = v => v === undefined || v === null ? "--" : String(v);

// normalize item qty keys
function qtyOf(item) {
  return n(item.qty ?? item.quantity ?? item.count ?? 0);
}
function weightOf(item) {
  return n(item.weight ?? item.wt ?? 0);
}
function itemName(item) {
  return item.name ?? item.item ?? item.title ?? "";
}

// coin totals
function totalGold(coinsObj){
  return (n(coinsObj.cp) * 0.01) + (n(coinsObj.sp) * 0.1) + (n(coinsObj.ep) * 0.5) + (n(coinsObj.gp)) + (n(coinsObj.pp) * 10);
}
function totalCoinWeight(coinsObj){
  return Object.values(coinsObj).reduce((s,c)=> s + n(c) * coinWeight, 0);
}

// Accept equipment as either an object of categories OR flat list with category property
function flattenSection(section){
  if(!section) return [];
  if(Array.isArray(section)) return section.map(it => ({ ...it }));
  // object with keys -> arrays
  const out = [];
  Object.keys(section).forEach(k => {
    const arr = section[k] || [];
    if(Array.isArray(arr)) arr.forEach(it => out.push({...it, category: k}));
  });
  return out;
}

// Attempt to parse legacy string-style spell components like "V, S, M (an octagonal sign)"
function parseMaterialsFromString(compStr){
  if(!compStr || typeof compStr !== "string") return [];
  const m = compStr.match(/M\s*\((.*?)\)/i);
  if(!m) return [];
  const inside = m[1].trim();
  // support comma-separated multiples inside parentheses
  const items = inside.split(/\s*,\s*/).map(x => ({ item: x, consumed: false, quantity_needed: 1 }));
  return items;
}

// sanitize spell's material list to a standard form { item/name, consumed(bool), quantity_needed }
// Spell can have: spell.components.material (array) or spell.components.materials or components string
function normalizeSpellMaterials(spell){
  const comps = spell.components ?? spell.components_raw ?? null;
  // If components is an object with material array
  if(typeof comps === "object" && comps !== null && (Array.isArray(comps.material) || Array.isArray(comps.materials))) {
    const arr = Array.isArray(comps.material) ? comps.material : comps.materials;
    return arr.map(m => {
      // m could be string or object
      if(typeof m === "string") {
        // try to parse "bat guano" or "Bat guano (consumed)" heuristics
        const mm = m.match(/^(.*?)(?:\s*\(consumed\))?$/i);
        return { item: mm ? mm[1].trim() : m, consumed: /consumed/i.test(m), quantity_needed: 1 };
      } else {
        // object - allow keys: item/name, consumed, quantity_needed
        return { item: (m.item ?? m.name ?? m.material ?? ""), consumed: !!m.consumed, quantity_needed: n(m.quantity_needed ?? m.qty ?? 1) };
      }
    });
  }
  // If components is a string, try to parse parentheses
  if(typeof spell.components === "string"){
    return parseMaterialsFromString(spell.components);
  }
  // fallback: look for direct "material" on spell
  if(Array.isArray(spell.material)) {
    return spell.material.map(m=> typeof m === "string" ? { item: m, consumed:false, quantity_needed:1 } : { item: m.item ?? m.name, consumed: !!m.consumed, quantity_needed: n(m.quantity_needed ?? 1) });
  }
  return [];
}

// --- Build UI pieces ---
// create simple element helper
function el(tag, props={}, inner=""){
  const d = document.createElement(tag);
  if(props.cls) d.className = props.cls;
  if(props.style) Object.assign(d.style, props.style);
  if(props.attrs) Object.keys(props.attrs).forEach(k => d.setAttribute(k, props.attrs[k]));
  if(inner !== "") d.innerHTML = inner;
  return d;
}

// coin stack builder (returns HTML string)
function renderCoinStack(label, key, color){
  return `<div style="margin-bottom:8px; text-align:center;">
    <div style="width:48px;height:48px;line-height:48px;border-radius:50%;
      border:2px solid ${color};display:inline-block;font-weight:700;font-size:15px;"
      class="coin-display" data-key="${key}">${coins[key]}</div>
    <div style="margin-top:4px;font-size:11px;font-weight:700;">${label}</div>
    <div style="display:flex;justify-content:center;gap:4px;margin-top:6px;">
      <input type="number" class="coin-input" data-key="${key}" style="width:44px;font-size:11px;padding:2px" placeholder="0">
      <button class="coin-add" data-key="${key}" style="font-size:11px;padding:2px 6px;">+</button>
      <button class="coin-sub" data-key="${key}" style="font-size:11px;padding:2px 6px;">−</button>
    </div>
  </div>`;
}

// Build a category section (keeps original collapse behavior)
// Accepts items array
function buildCategorySection(name, items, additionalWeight=0){
  if(!items || !items.length) return null;
  let sectionWeight = additionalWeight;
  items.forEach(it => sectionWeight += qtyOf(it) * weightOf(it));

  const sectionWrap = el("div", { style: { border: "1px solid var(--background-modifier-border)", borderRadius:"8px", overflow:"hidden" }});
  const header = el("div", { style: { padding: "8px 10px", backgroundColor:"var(--background-primary-alt)", cursor:"pointer", fontWeight:"700" }}, `${name} (${sectionWeight.toFixed(2)} lbs)`);
  sectionWrap.appendChild(header);

  const content = el("div", { style: { maxHeight: "0px", overflow: "hidden", transition:"max-height 0.25s ease, padding 0.25s ease", padding:"0 10px" }});
  // group small categories inline, large categories stacked
  const bySmall = {};
  const large = [];
  items.forEach(it => {
    const cat = it.category ?? "Other";
    if(smallCategories.has(cat)) {
      if(!bySmall[cat]) bySmall[cat] = [];
      bySmall[cat].push(it);
    } else {
      large.push(it);
    }
  });

  // small categories
  Object.keys(bySmall).forEach(cat => {
    const catTitle = el("div", { style: { fontWeight:700, color:"var(--accent-color)", marginTop:"8px" }}, cat);
    const grid = el("div", { style: { display:"grid", gridTemplateColumns: "repeat(auto-fill,minmax(120px,1fr))", gap:"6px", marginBottom:"8px" }});
    bySmall[cat].forEach(i=>{
      const color = rarityColors[i.rarity ?? "Common"] ?? "inherit";
      const card = el("div", { style: { border:`1px solid var(--background-modifier-border)`, borderRadius:"6px", padding:"6px", fontSize:"12px", textAlign:"center" }});
      card.innerHTML = `<div style="font-weight:700;color:${color}">${itemName(i)}</div><div style="color:var(--muted-text);font-size:12px;">Qty: ${qtyOf(i)} • Wgt: ${weightOf(i)}</div>`;
      grid.appendChild(card);
    });
    content.appendChild(catTitle);
    content.appendChild(grid);
  });

  // large categories stacked
  large.forEach(i=>{
    const title = el("div", { style: { fontWeight:700, color:"var(--accent-color)", marginTop:"8px" }}, i.category ?? "Other");
    const card = el("div", { style: { border:`1px solid var(--background-modifier-border)`, borderRadius:"6px", padding:"6px", fontSize:"12px", textAlign:"center", marginBottom:"6px" }});
    const color = rarityColors[i.rarity ?? "Common"] ?? "inherit";
    card.innerHTML = `<div style="font-weight:700;color:${color}">${itemName(i)}</div><div style="color:var(--muted-text);font-size:12px;">Qty: ${qtyOf(i)} • Wgt: ${weightOf(i)}</div>`;
    content.appendChild(title);
    content.appendChild(card);
  });

  sectionWrap.appendChild(content);
  // collapse toggle
  let expanded = false;
  header.addEventListener("click", () => {
    expanded = !expanded;
    content.style.maxHeight = expanded ? (content.scrollHeight + 20) + "px" : "0px";
    content.style.padding = expanded ? "8px 10px" : "0 10px";
  });

  return { section: sectionWrap, weight: sectionWeight };
}

// Build component pouch display (simple list with qty)
function buildComponentPouch(components){
  const arr = components || [];
  if(!arr.length) return null;
  const sect = el("div", { style: { border:"1px solid var(--background-modifier-border)", borderRadius:"8px", overflow:"hidden" }});
  const header = el("div", { style:{ padding:"8px 10px", backgroundColor:"var(--background-primary-alt)", fontWeight:700 }}, "Component Pouch");
  const content = el("div", { style: { padding:"8px 10px", fontSize:"12px" }});

  arr.forEach(c=>{
    const color = rarityColors[c.rarity ?? "Common"] ?? "inherit";
    const row = el("div", { style: { display:"flex", justifyContent:"space-between", gap:"12px", padding:"6px 0", borderBottom:"1px dashed var(--background-modifier-border)" }});
    const left = el("div", {}, `<strong style="color:${color}">${itemName(c)}</strong><div style="font-size:11px;color:var(--muted-text)">${c.description ?? ""}</div>`);
    const right = el("div", {}, `<div style="text-align:right">Qty: ${qtyOf(c)}</div>`);
    row.appendChild(left);
    row.appendChild(right);
    content.appendChild(row);
  });

  sect.appendChild(header);
  sect.appendChild(content);
  return { section: sect, weight: arr.reduce((s,c)=> s + qtyOf(c) * (weightOf(c) || 0), 0) };
}

// Spell Component Tracker - checks for each spell whether materials available, how many casts
function buildSpellComponentTracker(spells, components){
  const spellList = spells || [];
  if(!spellList.length) return null;
  const compArr = (components || []).map(c => ({ name: (c.name ?? c.item ?? "").toLowerCase(), qty: qtyOf(c) }));
  const compMap = {};
  compArr.forEach(c => compMap[c.name] = c.qty);

  const sect = el("div", { style: { border:"1px solid var(--background-modifier-border)", borderRadius:"8px", overflow:"hidden" }});
  const header = el("div", { style:{ padding:"8px 10px", backgroundColor:"var(--background-primary-alt)", fontWeight:700, cursor:"pointer" }}, "Spell Components Tracker");
  sect.appendChild(header);

  const content = el("div", { style: { maxHeight: "0px", overflow:"hidden", transition:"max-height 0.25s ease, padding 0.25s ease", padding:"0 10px" }});

  spellList.forEach(sp => {
    // Normalize spell materials
    const mats = normalizeSpellMaterials(sp);
    // If none, mark as no-materials or purely V/S
    if(!mats.length){
      const row = el("div", { style:{ padding:"8px 0", borderBottom:"1px dashed var(--background-modifier-border)" }});
      row.innerHTML = `<div style="font-weight:700">${sp.name}</div><div style="font-size:12px;color:var(--muted-text)">No material components required (or not specified in structured form)</div>`;
      content.appendChild(row);
      return;
    }

    // Evaluate materials
    const missing = [];
    let castsPossible = Infinity;
    mats.forEach(m=>{
      const itemKey = (m.item ?? m.name ?? "").toLowerCase();
      const need = n(m.quantity_needed ?? m.qty ?? 1);
      const invQty = compMap[itemKey] ?? 0;
      if(invQty < need){
        missing.push({ item: m.item ?? m.name, need, have: invQty, consumed: !!m.consumed });
      } 
      if(m.consumed){
        const possible = Math.floor(invQty / Math.max(1, need));
        castsPossible = Math.min(castsPossible, possible);
      } else {
        // if not consumed, unlimited when at least 1 exists
        if(invQty <= 0) castsPossible = 0;
      }
    });

    if(castsPossible === Infinity) castsPossible = (missing.length ? 0 : "Unlimited");

    const ok = missing.length === 0;
    const color = ok ? "#2ecc71" : (castsPossible === 0 ? "#e74c3c" : "#f39c12");
    const row = el("div", { style: { padding:"8px 0", borderBottom:"1px dashed var(--background-modifier-border)" }});
    const matsSummary = mats.map(m=> `${m.item ?? m.name}${m.consumed ? " (consumed)" : ""}${(m.quantity_needed && m.quantity_needed>1)?` x${m.quantity_needed}`:""}`).join(", ");
    const missingText = missing.length ? `<div style="color:#e74c3c;font-size:12px;margin-top:4px">Missing: ${missing.map(x=>`${x.item} (need ${x.need}, have ${x.have})`).join("; ")}</div>` : "";
    row.innerHTML = `<div style="display:flex;justify-content:space-between;align-items:center;">
        <div style="font-weight:700;color:${color}">${ok ? "✅" : "⚠️"} ${sp.name}</div>
        <div style="font-size:12px">${castsPossible === "Unlimited" ? "Castable: Unlimited" : `Castable: ${castsPossible}`}</div>
      </div>
      <div style="font-size:12px;color:var(--muted-text);margin-top:4px">Materials: ${matsSummary}</div>
      ${missingText}`;
    content.appendChild(row);
  });

  sect.appendChild(content);
  // allow header toggle
  let expanded = false;
  header.addEventListener("click", ()=>{
    expanded = !expanded;
    content.style.maxHeight = expanded ? (content.scrollHeight + 20) + "px" : "0px";
    content.style.padding = expanded ? "8px 10px" : "0 10px";
  });

  return sect;
}

// --- MAIN LAYOUT BUILD ---
// container
const root = dv.el("div", "");
root.style.display = "flex";
root.style.flexDirection = "column";
root.style.gap = "12px";
root.style.maxWidth = "1200px";

// TOP ROW - coins + meter
const topRow = el("div", { style: { display:"flex", justifyContent:"space-between", flexWrap:"wrap", gap:"12px"}});
const coinCol = el("div", { style: { display:"flex", gap:"12px", alignItems:"flex-start", flexWrap:"wrap'"}});
["pp","gp","ep","sp","cp"].forEach(k => {
  const color = k==="pp"?"purple":k==="gp"?"gold":k==="ep"?"silver":k==="sp"?"var(--accent-color)":"var(--muted-text)";
  coinCol.innerHTML += renderCoinStack(k.toUpperCase(), k, color);
});
topRow.appendChild(coinCol);

// coin totals small box
const totalsBox = el("div", { style: { textAlign:"center", fontWeight:700 }}, `
  <div style="font-size:13px">Total: ${totalGold(coins).toFixed(2)} GP</div>
  <div style="font-size:12px;color:var(--muted-text)">Coin Wgt: ${totalCoinWeight(coins).toFixed(2)} lbs</div>
`);
topRow.appendChild(totalsBox);

// meter
const meterWrap = el("div", { style: { minWidth:"240px", flexGrow:1 }});
const meterBar = el("div", { style: { height:"14px", backgroundColor:"var(--background-modifier-border)", borderRadius:"8px", overflow:"hidden" }});
const meterFill = el("div", { style: { height:"100%", width:"0%", backgroundColor:"#27ae60" }});
meterBar.appendChild(meterFill);
const meterText = el("div", { style: { fontWeight:700, fontSize:"12px", marginTop:"6px" }});
meterWrap.appendChild(meterBar);
meterWrap.appendChild(meterText);
topRow.appendChild(meterWrap);
const pushText = el("div", { style: { fontWeight: "700", fontSize: "12px", marginTop: "4px", color: "var(--muted-text)" } });
meterWrap.appendChild(pushText);

root.appendChild(topRow);

// MAIN ROW with left/right
const mainRow = el("div", { style: { display:"flex", gap:"20px", alignItems:"flex-start", flexWrap:"wrap" }});
const leftCol = el("div", { style: { flex:"1 1 480px", minWidth:"300px", display:"flex", flexDirection:"column", gap:"10px" }});
const rightCol = el("div", { style: { flex:"1 1 280px", minWidth:"250px", display:"flex", flexDirection:"column", gap:"10px" }});

// Prepare inventory sources (robust)
const equipmentList = flattenSection(f.inventory?.equipment ?? f.equipment ?? []);
const backpackList = flattenSection(f.inventory?.backpack ?? f.backpack ?? []);
const componentsList = (f.inventory?.components ?? f.components ?? []).map(c => ({ ...c }));

// Equipment & Backpack sections (collapsible)
const eqSection = buildCategorySection("Equipment", equipmentList);
if(eqSection) leftCol.appendChild(eqSection.section);
const bpSection = buildCategorySection("Backpack", backpackList, backpackBaseWeight);
if(bpSection) leftCol.appendChild(bpSection.section);

// Component pouch
const compSection = buildComponentPouch(componentsList);
if(compSection) rightCol.appendChild(compSection.section);

// Spell tracker
const spellTracker = buildSpellComponentTracker(f.spells ?? f.spellbook ?? [], componentsList);
if(spellTracker) rightCol.appendChild(spellTracker);

// assemble
mainRow.appendChild(leftCol);
mainRow.appendChild(rightCol);
root.appendChild(mainRow);

dv.container.appendChild(root);

// --- DYNAMIC BEHAVIOR: coins & meter updates ---
function updateAll(){
  // update coin displays
  coinCol.querySelectorAll(".coin-display").forEach(el => {
    const key = el.dataset.key;
    el.innerText = coins[key];
  });
  // update totals box
  totalsBox.innerHTML = `
    <div style="font-size:13px">Total: ${totalGold(coins).toFixed(2)} GP</div>
    <div style="font-size:12px;color:var(--muted-text)">Coin Wgt: ${totalCoinWeight(coins).toFixed(2)} lbs</div>
  `;
  // compute total item weights (recalc from lists)
  let itemsWeight = 0;
  equipmentList.forEach(i => itemsWeight += qtyOf(i) * weightOf(i));
  backpackList.forEach(i => itemsWeight += qtyOf(i) * weightOf(i));
  componentsList.forEach(i => itemsWeight += qtyOf(i) * weightOf(i));
  const totalWeight = itemsWeight + totalCoinWeight(coins);
  // meter fill and color zones
  const pct = Math.min(100, (totalWeight / carryCapacity) * 100);
  meterFill.style.width = `${pct}%`;
  if(pct <= 60) meterFill.style.backgroundColor = "#27ae60"; // green
  else if(pct <= 90) meterFill.style.backgroundColor = "#f1c40f"; // yellow
  else meterFill.style.backgroundColor = "#e74c3c"; // red
  meterText.innerText = `Weight: ${totalWeight.toFixed(2)} / ${carryCapacity} lbs ${totalWeight > carryCapacity ? "(Overencumbered!)" : ""}`;
  pushText.innerText = `Push/Drag/Lift: ${pushDragLift} lbs`;
  // update spell tracker content (rebuild simple way: remove and recreate)
  // For simplicity refresh page — but better to update DOM nodes in place.
}

// attach coin add/sub events
coinCol.querySelectorAll(".coin-add").forEach(btn => {
  btn.addEventListener("click", () => {
    const key = btn.dataset.key;
    const input = coinCol.querySelector(`.coin-input[data-key="${key}"]`);
    const val = parseInt(input.value) || 0;
    coins[key] = (coins[key] ?? 0) + val;
    input.value = "";
    updateAll();
  });
});
coinCol.querySelectorAll(".coin-sub").forEach(btn => {
  btn.addEventListener("click", () => {
    const key = btn.dataset.key;
    const input = coinCol.querySelector(`.coin-input[data-key="${key}"]`);
    const val = parseInt(input.value) || 0;
    coins[key] = Math.max(0, (coins[key] ?? 0) - val);
    input.value = "";
    updateAll();
  });
});

// initial update
updateAll();


```

## Pyro
```dataviewjs
// === Pyrothopy (Fury) Control Panel - Single Panel Dashboard ===

const f = dv.current()?.file?.frontmatter || {};

// Config / defaults (pull from frontmatter if present)
const PB = Number(f.pb ?? f.proficiency_bonus ?? 2); // proficiency bonus for damage calc
const CON_MOD = Number(f.con_mod ?? f.con ?? 0);     // CON modifier for damage calc
const storageKey = `pyrothopy_${dv.current().file.path}`;

// Fire size definitions
const FIRE_SIZES = [
  { key: "Pinprick", dc: 8, startPressure: 0, notes: "Candle, ember, spark, match. No automatic trigger." },
  { key: "Small", dc: 10, startPressure: 0, notes: "Torch, lantern. Possible slow buildup. Repeat after 1 minute." },
  { key: "Medium", dc: 13, startPressure: 1, notes: "Campfire, bonfire. Repeat save each turn within 30 ft. Failure → Pressure 1." },
  { key: "Large", dc: 15, startPressure: 2, notes: "Bonfire, burning tree. After 3 rounds exposure → auto Fury State. Failure → Pressure 2." },
  { key: "Massive", dc: 18, startPressure: 3, notes: "Building on fire, wildfire, lava. Automatic large-range check, Failure → Pressure 3." }
];

// Helper: persist/load state to localStorage
function loadState(){
  try{
    const raw = localStorage.getItem(storageKey);
    return raw ? JSON.parse(raw) : { pressure: 0, furyActive: false, lastFireSize: "Pinprick", exploded: false, aftermath: null };
  } catch(e){ return { pressure: 0, furyActive: false, lastFireSize: "Pinprick", exploded: false, aftermath: null }; }
}
function saveState(s){
  try{ localStorage.setItem(storageKey, JSON.stringify(s)); } catch(e){}
}

// Dice roller helpers
function rollDie(sides){ return Math.floor(Math.random()*sides) + 1; }
function rollNDice(n, sides){
  const rolls = [];
  for(let i=0;i<n;i++) rolls.push(rollDie(sides));
  return { total: rolls.reduce((a,b)=>a+b,0), rolls };
}

// Create DOM helper
function el(tag, style={}, inner=""){
  const d = document.createElement(tag);
  Object.assign(d.style, style);
  if(inner !== "") d.innerHTML = inner;
  return d;
}

// Load persisted state
let state = loadState();

// Root panel
const panel = dv.el("div");
panel.style.maxWidth = "880px";
panel.style.margin = "12px auto";
panel.style.border = "2px solid var(--background-modifier-border)";
panel.style.borderRadius = "12px";
panel.style.padding = "12px";
panel.style.background = "linear-gradient(180deg, rgba(255,255,255,0.01), rgba(0,0,0,0.02))";
panel.style.fontFamily = "inherit";

// Title
const title = el("div", { display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"8px" });
title.appendChild(el("div", { fontWeight:700, fontSize:"16px" }, "🔥 Pyrothopy — The Fury Control Panel"));
const resetBtn = el("button", { padding:"6px 8px", cursor:"pointer", fontSize:"12px" }, "Reset Panel");
title.appendChild(resetBtn);
panel.appendChild(title);

// Top row: Fire size selector and Save DC
const topRow = el("div", { display:"flex", gap:"12px", alignItems:"center", marginBottom:"12px", flexWrap:"wrap" });

// Fire size select
const fireWrap = el("div", { display:"flex", flexDirection:"column", minWidth:"240px" });
fireWrap.appendChild(el("div", { fontSize:"12px", color:"var(--muted-text)", marginBottom:"6px" }, "Active Flame Stimulus"));
const fireSelect = document.createElement("select");
fireSelect.style.padding = "6px";
fireSelect.style.borderRadius = "6px";
fireSelect.style.border = "1px solid var(--background-modifier-border)";
FIRE_SIZES.forEach(fs => {
  const opt = document.createElement("option");
  opt.value = fs.key;
  opt.innerText = `${fs.key} (DC ${fs.dc})`;
  fireSelect.appendChild(opt);
});
fireSelect.value = state.lastFireSize ?? "Pinprick";
fireWrap.appendChild(fireSelect);
topRow.appendChild(fireWrap);

// Show DC and starting Pressure
const dcBox = el("div", { display:"flex", flexDirection:"column", minWidth:"160px" });
dcBox.appendChild(el("div", { fontSize:"12px", color:"var(--muted-text)" }, "Save DC"));
const dcVal = el("div", { fontWeight:700, fontSize:"15px", marginTop:"4px" }, "—");
dcBox.appendChild(dcVal);
topRow.appendChild(dcBox);

// Fire notes
const notesBox = el("div", { flexGrow:1, fontSize:"12px", color:"var(--muted-text)" });
notesBox.innerHTML = "&nbsp;";
topRow.appendChild(notesBox);

panel.appendChild(topRow);

// Middle: Pressure tracker + Fury toggle + End Turn
const midRow = el("div", { display:"flex", gap:"12px", alignItems:"center", marginBottom:"12px", flexWrap:"wrap" });

// Pressure display block
const pressureBlock = el("div", { display:"flex", flexDirection:"column", alignItems:"center", minWidth:"220px", padding:"8px", borderRadius:"8px", border:"1px solid var(--background-modifier-border)" });
pressureBlock.appendChild(el("div", { fontSize:"12px", color:"var(--muted-text)" }, "Pressure"));
const pressureValue = el("div", { fontSize:"24px", fontWeight:700, marginTop:"6px" }, `${state.pressure}`);
pressureBlock.appendChild(pressureValue);

// Pressure buttons
const pbRow = el("div", { display:"flex", gap:"8px", marginTop:"8px" });
const plusBtn = el("button", { padding:"6px 10px", cursor:"pointer" }, "+");
const minusBtn = el("button", { padding:"6px 10px", cursor:"pointer" }, "−");
const setZeroBtn = el("button", { padding:"6px 10px", cursor:"pointer" }, "Reset 0");
pbRow.appendChild(plusBtn);
pbRow.appendChild(minusBtn);
pbRow.appendChild(setZeroBtn);
pressureBlock.appendChild(pbRow);

midRow.appendChild(pressureBlock);

// Fury state block
const furyBlock = el("div", { display:"flex", flexDirection:"column", minWidth:"240px", padding:"8px", borderRadius:"8px", border:"1px solid var(--background-modifier-border)" });
furyBlock.appendChild(el("div", { fontSize:"12px", color:"var(--muted-text)" }, "Fury State"));
const furyStatus = el("div", { fontSize:"16px", fontWeight:700, marginTop:"6px" }, state.furyActive ? "ACTIVE" : "Inactive");
furyBlock.appendChild(furyStatus);

const furyBtn = el("button", { padding:"8px 10px", marginTop:"8px", cursor:"pointer" }, state.furyActive ? "End Fury State" : "Enter Fury State");
furyBlock.appendChild(furyBtn);

// End Turn (pressure +1) — only meaningful in Fury state
const endTurnBtn = el("button", { padding:"6px 10px", marginTop:"8px", cursor:"pointer" }, "End Turn (+1 Pressure)");
furyBlock.appendChild(endTurnBtn);

midRow.appendChild(furyBlock);

// Explosion summary block (shows DC and quick explode button if pressure 6)
const explosionBlock = el("div", { display:"flex", flexDirection:"column", minWidth:"300px", padding:"8px", borderRadius:"8px", border:"1px solid var(--background-modifier-border)" });
explosionBlock.appendChild(el("div", { fontSize:"12px", color:"var(--muted-text)" }, "Explosion Tools"));
const explodeInfo = el("div", { fontSize:"13px", marginTop:"6px" }, "Pressure < 6 — explosion not ready");
explosionBlock.appendChild(explodeInfo);
const explodeBtn = el("button", { padding:"8px 10px", marginTop:"8px", cursor:"pointer", background:"#e74c3c", color:"#fff", border:"none", borderRadius:"6px" }, "Trigger Explosion (Pressure 6)");
explodeBtn.disabled = true;
explosionBlock.appendChild(explodeBtn);

midRow.appendChild(explosionBlock);

panel.appendChild(midRow);

// Bottom: Reference Panel (collapsible)
const refPanel = el("details", { padding:"8px", borderTop:"1px solid var(--background-modifier-border)", marginTop:"8px" });
const refSummary = el("summary", {}, "Full Pyrothopy Reference (click to expand)");
refPanel.appendChild(refSummary);

const refContent = el("div", { fontSize:"12px", marginTop:"6px", lineHeight:"1.4" });
refContent.innerHTML = `
<b>Curse Description:</b> Fire-drunk shapeshifting curse. Heat and flames induce Fury State. Spreads via burns/explosions.<br><br>
<b>Flame Hypnosis:</b> Pinprick (DC8), Small (DC10), Medium (DC13 → Pressure1), Large (DC15 → Pressure2), Massive (DC18 → Pressure3, DC+1 per round)<br><br>
<b>Fury State Features:</b><br>
1. Thermal Predator: +10ft, advantage on heat Perception, compelled to largest group, cannot Disengage/Dodge<br>
2. Smoldering Body: shed light 10/20ft, PB+CON fire damage on touch/grapple<br>
3. Fire-Drunk Focus: disadvantage ranged, advantage melee<br><br>
<b>Pressure System:</b> +1 per turn, +1 frightened, +2 cold damage, +1 if 3+ adjacent; reach 6 → explode<br><br>
<b>Explosion:</b> 20ft radius, Dex save DC8+PB+CON, fail 18d10 fire + prone, success half, not prone; ground difficult terrain 1d10 min; creatures entering area take (minutes)d6 fire damage<br><br>
<b>Aftermath:</b> collapse 1 HP, stable until flames die, 1 lvl exhaustion, cold vulnerability 24h, pressure resets<br><br>
<b>Optional Quirks:</b> smoke from nostrils, fire-drunk euphoria, ember eyes, stare at flames, hot food/drinks, scorch marks while angry
`;
refPanel.appendChild(refContent);
panel.appendChild(refPanel);

// append panel to dataview container
dv.container.appendChild(panel);

// --- UTILS: update UI based on state ---
function findFireSize(key){ return FIRE_SIZES.find(f => f.key === key) ?? FIRE_SIZES[0]; }

function setPressure(v, opts = { note: true }){
  const old = state.pressure;
  state.pressure = Math.max(0, Math.min(6, Math.floor(v)));
  saveState(state);
  pressureValue.innerText = state.pressure;
  if(state.pressure <= 2) pressureValue.style.color = "#27ae60";
  else if(state.pressure <= 4) pressureValue.style.color = "#f1c40f";
  else if(state.pressure === 5) pressureValue.style.color = "#e67e22";
  else pressureValue.style.color = "#e74c3c";
  explodeBtn.disabled = state.pressure < 6;
  if(opts.note) appendLog(`Pressure: ${old} → ${state.pressure}`);
  if(state.pressure >= 6 && !state.exploded) triggerExplosion();
}

function setFury(active, note=true){
  state.furyActive = !!active;
  saveState(state);
  furyStatus.innerText = state.furyActive ? "ACTIVE" : "Inactive";
  furyBtn.innerText = state.furyActive ? "End Fury State" : "Enter Fury State";
  appendLog(`Fury State ${state.furyActive ? "entered" : "ended"}`);
}

function updateDCAndNotes(){
  const sel = fireSelect.value;
  state.lastFireSize = sel;
  saveState(state);
  const fs = findFireSize(sel);
  dcVal.innerText = `DC ${fs.dc} (start ${fs.startPressure})`;
  notesBox.innerHTML = `<div style="font-size:12px">${fs.notes}</div>`;
}

function appendLog(txt){
  const t = document.createElement("div");
  t.style.marginBottom = "6px";
  t.innerHTML = `${(new Date()).toLocaleTimeString()} — ${txt}`;
  log.insertBefore(t, log.firstChild);
}

function triggerExplosion(){
  if(state.exploded) return;
  state.exploded = true;
  saveState(state);
  appendLog("⚠ Pressure reached 6 — Explosion triggered!");
  const explosionDC = 8 + PB + CON_MOD;
  const roll = rollNDice(18,10);
  const dmgTotal = roll.total;
  const burnMinutes = rollDie(10);
  state.aftermath = { explosionDC, dmgTotal, rolls: roll.rolls, burnMinutes, timestamp: Date.now() };
  saveState(state);
  explodeInfo.innerHTML = `
    <div><b>Explosion DC:</b> ${explosionDC}</div>
    <div><b>Damage (18d10):</b> ${dmgTotal} &nbsp; <small style="color:var(--muted-text)">[rolls: ${roll.rolls.join(", ")}]</small></div>
    <div><b>Radius:</b> 20 ft — creatures fail Dex save suffer full (18d10), prone; success half, not prone.</div>
    <div><b>Ground:</b> Burning molten blood — difficult terrain until flames die (${burnMinutes} min)</div>
  `;
  appendLog(`Explosion rolled ${dmgTotal} (18d10). Burning persists for ${burnMinutes} min.`);
  appendLog("Aftermath: You collapse unconscious at 1 HP. Gain 1 exhaustion level & Vulnerable to cold for 24 hours. Pressure resets to 0.");
  state.pressure = 0;
  state.furyActive = false;
  saveState(state);
  pressureValue.innerText = state.pressure;
  furyStatus.innerText = "Inactive";
  furyBtn.innerText = "Enter Fury State";
  explodeBtn.disabled = true;
  pressureValue.style.color = "#27ae60";
}

// --- EVENT HOOKS ---
fireSelect.addEventListener("change", ()=>{
  updateDCAndNotes();
  const fs = findFireSize(fireSelect.value);
  appendLog(`Selected stimulus: ${fs.key} (DC ${fs.dc})`);
  if(state.pressure < fs.startPressure) setPressure(fs.startPressure);
});

plusBtn.addEventListener("click", ()=> setPressure(state.pressure + 1));
minusBtn.addEventListener("click", ()=> setPressure(state.pressure - 1));
setZeroBtn.addEventListener("click", ()=> setPressure(0));

furyBtn.addEventListener("click", ()=> setFury(!state.furyActive));

endTurnBtn.addEventListener("click", ()=>{
  if(!state.furyActive){ appendLog("End Turn pressed while not in Fury State — no pressure gain."); return; }
  appendLog("End Turn: Fury pressure increases by 1.");
  setPressure(state.pressure + 1);
});

explodeBtn.addEventListener("click", ()=>{
  if(state.pressure < 6){ appendLog("Explosion button pressed but Pressure < 6 — no effect."); return; }
  triggerExplosion();
});

resetBtn.addEventListener("click", ()=>{
  if(!confirm("Reset Pyrothopy panel state? This will clear stored pressure/fury/explosion info.")) return;
  state = { pressure: 0, furyActive: false, lastFireSize: "Pinprick", exploded: false, aftermath: null };
  saveState(state);
  pressureValue.innerText = state.pressure;
  pressureValue.style.color = "#27ae60";
  furyStatus.innerText = "Inactive";
  furyBtn.innerText = "Enter Fury State";
  explodeInfo.innerHTML = "Pressure < 6 — explosion not ready";
  explodeBtn.disabled = true;
  log.innerHTML = "Activity log cleared.";
  appendLog("Panel reset.");
});

updateDCAndNotes();
pressureValue.innerText = state.pressure;
pressureValue.style.color = state.pressure <= 2 ? "#27ae60" : (state.pressure <= 4 ? "#f1c40f" : (state.pressure === 5 ? "#e67e22" : "#e74c3c"));
furyStatus.innerText = state.furyActive ? "ACTIVE" : "Inactive";
furyBtn.innerText = state.furyActive ? "End Fury State" : "Enter Fury State";
explodeBtn.disabled = state.pressure < 6;

if(state.exploded && state.aftermath){
  const a = state.aftermath;
  appendLog(`Previous explosion: ${a.dmgTotal} dmg, ${a.burnMinutes} min burning.`);
  explodeInfo.innerHTML = `<div><b>Prev Explosion (stored):</b> Damage ${a.dmgTotal}, Burning ${a.burnMinutes} min</div>`;
}

```

## Smudge


```statblock
dice: true
render: true
columns: 3
forceColumns: true
columnHeight: 550px
columnWidth: 447px

name: Smudge
image: [[Smudge.png]]
size: Tiny
type: Forsaken Companion
ac: 13 + PB
hp: Connected to Fig Snowberry
speed: 40 ft., climb 30 ft., burrow 10 ft.
stats: [6, 17, 15, 8, 14, 10]
cr: 5
saves:
  - Dex: +3 + PB
  - Con: +2 + PB
skillsaves:
  - Perception: +4 + PB
  - Stealth: +5 + PB
damage_vulnerabilities:
damage_resistances:
damage_immunities:
senses: truesight 60 ft.
languages: understands your languages telepathically
traits:
  - name: Void Form
    desc: "Smudge is made of Void essence. He leaves no tracks and cannot be detected by detect magic, divination spells, or magical detection items. He has advantage on saving throws against spells, and spells that target him have disadvantage to hit."
  - name: Mirrored Demise
    desc: "From birth, the Forsaken Companion is linked to its UnForsaken counterpart in life and death. They share hit points. When one takes damage, the other takes an equivalent amount as psychic damage. When one drops to 0 hit points, so does the other."
  - name: Magic
    desc: ""
actions:
  - name: Void Fang
    desc: "Melee Weapon Attack: +3 + PB to hit, reach 5 ft. Hit: 1d4 + PB void damage. If the target is a spellcaster, they lose mana equal to 1d4 + PB − 5. If the result is positive, that mana transfers to the UnForsaken Link."
  - name: Weave Cloak
    desc: "Smudge can cloak a spellcaster whose max spell level is equal to or lower than his UnForsaken Link. The cloaked creature gains Void Form benefits. Smudge must maintain concentration, cannot move, and must use his action each turn. Spells cast while cloaked must use a slot 1 level higher or the spell fails, triggers Smudge’s reaction, and breaks his concentration."
reactions:
  - name: Weave Absorption
    desc: "When a creature casts a spell within PB × 5 ft., Smudge may use his reaction to attempt to absorb it. He makes a Constitution save (DC 10 + spell level). On a failure, he suffers the spell's effects. On a success, the UnForsaken Link gains mana equal to the spell's level."

```


## Ideals
> [!column|2 no-title]
>
> 
>> [!metadata|ideals] Ideals
> *<font color="#7f7f7f">`VIEW[{ideals}][text]`</font>*
>
>> [!metadata|flaws] Flaws
> *<font color="#7f7f7f">`VIEW[{flaws}][text]`</font>*
> 
>> [!metadata|fear] Fears
> *<font color="#7f7f7f">`VIEW[{fears}][text]`</font>*
>
>> [!metadata|mannerism] Mannerisms
> *<font color="#7f7f7f">`VIEW[{mannerisms}][text]`</font>*
## Present

### Goals

#### Short-Term:



#### Long-Term:



## Past
### Birth:

**Day** `INPUT[inlineSelect(option(1), option(2), option(3), option(4), option(5), option(6), option(7), option(8), option(9), option(10), option(11), option(12), option(13), option(14), option(15), option(16), option(17), option(18), option(19), option(20), option(21), option(22), option(23), option(24), option(25), option(26), option(27), option(28), option(29), option(30), option(31), option(32), option(33), option(34), option(35), option(36), option(37), option(38), option(39), option(40)):fc-date.day]` **Month** `INPUT[inlineSelect(option(1, Month of a New Light),option(2, Month of Eaos), option(3, Month of Truth), option(4, Month of Qhathos), option(5, Month of Temp), option(6, Month of Vimnera), option(7, Month of Prosper), option(8, Month of Datarr), option(9, Month of Yearn), option(10, Month of Final Light)):fc-date.month]` **Year** `INPUT[number(class(nb-mb-55)):year]` `VIEW[\[{year}-*\]][text(hidden):fc-date.year]` `VIEW[{Vault Hub#dpy}*{year}+{Vault Hub#dpm}*({fc-date.month}-1)+{fc-date.day}][math(hidden):birthday]`
- Birth Location: Malmsbury
- Mother: Lyra Snowberry - A high-ranking sorceress in Malmsbury’s arcane network, Lyra was calm, collected, and incredibly protective. She had an affinity for teleportation magic, which was integral to her work in the Luminous Empire. Despite her powerful position, she was also deeply connected to her children’s welfare. Lyra’s strength wasn’t just in magic, but in her ability to shelter her family from the empire’s dangers, even if it meant giving up everything. 
- Father: Corwin Snowberry - A humble halfling with a knack for enchantment, Corwin was a skilled craftsman, working as a blacksmith and magical items maker for the Luminous Empire. His craft, though not as prestigious as his wife’s, allowed him to live comfortably. He was a kind, reliable figure who doted on his children and kept them grounded. While he never quite understood the full scope of Fig’s magic, he was loving and protective, ensuring Fig knew that he was just as much a part of their family as his more magically-inclined siblings.

## Database
 ![[Database - Player Note.base]]

### Backstory
#### Child in Hiding
Malmsbury was a city that thrummed with life — a glittering forge at the heart of the Luminous Empire. The air was thick with the scent of oil and magic, where mages wove enchantments into rivets and sails, and steam swirled around skyships that soared above the skyline. The city's veins ran with arcane energy, feeding the endless drive for invention.![[Fig anim.png|right lp|300]]

![[Plum Anim.png|left lp|300]]And yet, when the colossal Verriwind, the Empire's pride — a great train of magical power — first roared through the capital, its arcane exhaust unleashed a fury unlike any the city had seen before. It flooded the undercity, sparking violet flames and dripping liquid mana into the canals. To most, it was a spectacle, a marvel of industrial magic. But for a rare few, the fallout didn’t just disappear into the ether. It clung to their very souls.

They called them Unforsaken — beings born not of flesh, but of the Weave’s shattered essence. Children born from arcane rupture, magical accidents that shouldn’t exist. Fig Snowberry was one such child. Born of a sorceress — a circle keeper who managed one of the Empire's most important teleportation gates — and no father. Fig’s existence was a cosmic anomaly, a halfling-shaped echo of arcane excess, a being of pure magic that had learned to breathe and grow. Fig’s older siblings, **Plum** and **Sage**, were both mortal halflings with natural magical gifts, though none were as powerful as Fig's. Their father was a commoner, a simple halfling blacksmith and enchanter — but he loved Fig as if he were his own. Though they all adored him, they couldn't help but feel that Fig was different. His rapid growth, his inner glow, his magical aura — all of it made him a constant reminder that he wasn’t quite right, even in a family so steeped in magic.

#### Child on the Run 
When the Verriwind returned every half-year to Malmsbury, the city buzzed with rumors and whispers of Unforsaken being hunted by the Empire's inquisitors. Every time, Fig was hidden away — tucked into flour bins, cellars, or beneath the scent of fresh-baked bread, which his mother used to cover his unmistakable glow. Fig's earliest memory, the one most rooted in his soul, was the smell of food — his mother’s way of masking his presence, ensuring he would survive the Empire’s scrutiny. By the time Fig was four years old, whispers had reached the Counsel of Light — rumors of a family of magically gifted children, one of whom radiated raw arcane instability. The Empire's magic hunters were closing in. **Lyra Snowberry**, Fig’s mother, had no choice. One night, as soldiers scoured the district, she gathered her children and prepared them for the dangerous journey ahead. She draped her husband’s large, blacksmith’s chained shirt over Fig, who was already the biggest of the children, but still far too small for it. She fastened her children’s childhood blankets around them: Fig’s was blue, Sage’s green, and Plum’s purple. She pinned them all with their favorite cloak pins, as they used to do when they tried to pretend to be like their father. In her hands, she passed Plum a small, enchanted dagger — a family heirloom — and gave Sage a sending stone, a lifeline to their family. Fig, ever attached to the kitchen, would not leave without his precious cooking tools: a set of knives, a wooden spoon, and a cast-iron pan. His mother handed them to him, her eyes filled with both sorrow and love.![[Sage Anim.png|right lp|300]]

"Wherever this takes you" she whispered, her voice barely audible over the roar of magic, "Keep warm. Keep kind."

 ![[Smudge.png|left lp|300]]With that, the teleportation circle flared, pulling them from their home and casting them into the unknown. 

The Snowberry children awoke in Osse, the fabled refuge for runaway magical beings, a wild and untamed land. But children — even magical ones — are poor travelers. Hungry and disoriented, they wandered aimlessly for days, surviving only on whatever they could find. It wasn’t long before they crossed paths with a Legion convoy. The banners of the Luminous Empire were unmistakable. The soldiers were transporting cages filled with magical creatures, their eyes hollow and empty, bound by runic chains that suppressed their magic.

Before they could flee, the soldiers noticed Fig’s glow — that faint, shimmering aura that marked him as Unforsaken. In an instant, Plum and Sage sprang into action. With a shared look, Sage grabbed one of Fig’s cooking knives, and Plum unleashed wild magic to unlock the cages, causing the animals inside to panic. In the chaos, she shouted, “Run, Fig!” 

 But in their desperation, they freed more than they could control. One of the creatures — a Fury — was released into the wild. A werekivego, born of the Blood Curse of Temp, its primal instincts were drawn to the flickering flames of the convoy’s torches. It moved like a sleepwalker, its smoke-filled nostrils taking in the air, before it silently walked toward the largest group of soldiers. Without warning, it exploded.

The blast was deafening. Lava splattered against the trees, scorching everything in its path. The air screamed as fire and earth collided. Fig was hurled into the forest by the shockwave, his small body barely able to withstand the force before everything went
black.

#### Lost Child
When Fig awoke, the world was a scorched wasteland. The smell of charcoal and rain mixed in the air. The convoy was gone. His siblings were gone. There were only faint trails of melted iron and blackened footprints that turned to ash after a few steps. Fig stumbled throughthe charred remains, searching for his family — but only found ashes, smoke, and ruin. He searched until his legs gave out, then cried until his throat was raw and his voice was lost to the wind. That night, by the flickering embers of his own campfire, Fig’s eyes began to droop in exhaustion. But then, a movement caught his attention. A pitch-black weasel, slick as shadow, crept from the smoke and curled up against his neck, warm and silent. For a moment, it was as if time had stopped — the weasel’s presence grounding him, offering him a strange sense of comfort amidst the chaos. When Fig awoke the next morning, the weasel was still there. He named it **Smudge** — a quiet companion, a soul-shifting presence bound to him by an unseen force.

### Journey:



### Class Table:

| Level | Proficiency Bonus | Features | Cantrips Known | Spells Known | Mana Pool | Max Spell Level | Spell Catching Level |
|:---:|:---:|:---|:---:|:---:|:---:|:---:|:---:|
| 1st | +2 | Spellcasting, Forsaken Companion | 4 | 9 | 3 | 1 | — |
| 2nd | +2 | Weave Manipulation | 4 | 10 | 8 | 2 | — |
| 3rd | +2 | Soul Link (Redeemed) | 4 | 11 | 10 | 2 | — |
| 4th | +2 | ─ | 5 | 11 | 16 | 3 | — |
| 5th | +3 | Spell Catching | 5 | 12 | 20 | 3 | 1 |
| 6th | +3 | ─ | 5 | 13 | 26 | 4 | 1 |
| 7th | +3 | Ability Score Improvement | 5 | 14 | 30 | 4 | 1 |
| 8th | +3 | ─ | 6 | 15 | 38 | 5 | 2 |
| 9th | +4 | Spell Reflection | 6 | 16 | 43 | 5 | 2 |
| 10th | +4 | Strings of Concentration | 6 | 17 | 53 | 6 | 2 |
| 11th | +4 | Extra Spell Attack | 6 | 18 | 59 | 6 | 2 |
| 12th | +4 | ─ | 7 | 19 | 71 | 7 | 3 |
| 13th | +5 | Attached to Greatness | 7 | 20 | 75 | 7 | 3 |
| 14th | +5 | ─ | 7 | 21 | 86 | 8 | 3 |
| 15th | +5 | Ability Score Improvement | 7 | 22 | 91 | 8 | 3 |
| 16th | +5 | ─ | 7 | 23 | 108 | 9 | 4 |
| 17th | +6 | One with the Weave | 8 | 24 | 108 | 9 | 4 |
| 18th | +6 | ─ | 8 | 25 | 127 | 10 | 4 |
| 19th | +6 | Overflowing Magic | 8 | 25 | 127 | 10 | 4 |
| 20th | +6 | ─ | 8 | 25 | 155 | 11 | 5 |

## Pyrothopy
**The Curse of the Werekivego (Fury)**
*A fire-drunk shapeshifting curse driven by heat, crowds, and combustion.*

Creatures afflicted with Pyrothopy become heat-hunters. Even when stable, they exhale warm smoke in cold weather and feel restless near open flames. A true Fury is almost indistinguishable from its normal self—until the faint smoke rising from the nose and lips begins to coil.

When the Fury fully awakens, the curse _searches_ for the largest cluster of warm bodies like a predator sensing prey. Once its internal pressure peaks, the creature detonates in a spectacular volcanic burst: molten blood, shrapnel-bone, and superheated air. The Fury survives the blast but collapses, unconscious, until the flames around it die out.

Pyrothopy spreads to survivors of the explosion or to any rescuer burned by the lingering cursed flames.

#### **I. FIRE HYPNOSIS (Trigger System)**

Whenever the cursed character sees a flame, they must make a **Wisdom saving throw** to resist being hypnotized and slipping into **Fury State**.

The DC depends on flame size:

---

#### **FIRE SIZE → SAVE DC → STARTING PRESSURE**

|Flame Size|DC|Fury Pressure|
|---|---|---|
|Pinprick|8|No trigger|
|Small|10|Possible, slow buildup|
|Medium|13|**1**|
|Large|15|**2**|
|Massive Inferno|18|**3** (save each round, DC +1 each time)|

#### **Pressure 6 = Explosion**

18d10 fire, 20 ft radius, prone on fail.

####  **Fire Size Categories**
> [!column|5 no-title]
>> #### **1. Pinprick Flames — DC 8**
>>
>> _Candle, ember, spark, match_
>>
>> - Minor distraction
>>    
>> - No repeated saves needed
>>    
>> - Pure flavor unless already stressed or low HP
>    
>> #### **2. Small Flames — DC 10**
>> 
>> _Torch, lantern, oil lamp, candle cluster_
>> 
>> - Noticeable draw
>>     
>> - After 1 minute, make another save
>>     
>> - If stressed/wounded → **+2 DC**
>    
>> #### **3. Medium Flames — DC 13**
>> 
>> _Campfire, fireplace, magical bonfire_
>> 
>> - Strong hypnotic pull
>>     
>> - **Repeat save every turn** within 30 ft
>>     
>> - Failure → immediate **Fury State (Pressure 1)**
>    
>> #### **4. Large Flames — DC 15**
>> 
>> _Bonfire, burning tree, creature fully on fire_
>> 
>> - Entrancing trance
>>     
>> - Disadvantage on Perception checks unrelated to heat
>>     
>> - After **3 rounds of exposure** → automatic Fury State
>>     
>> - Failure → **Fury State (Pressure 2)**
>    
>> #### **5. Massive Inferno — DC 18**
>> 
>> _Building on fire, wildfire, lava, ship aflame, large lingering Fireball_
>> 
>> - Automatic save attempt **on sight**, up to 300 ft
>>     
>> - On failure → **Fury State (Pressure 3)**
>>     
>> - On success → DC rises by +1 each round of exposure

> [!column|2 no-title]
>> ###  **Modifiers**
>> 
>> - **+2 DC** if frightened, bloodied, or enraged
>>     
>> - **+1–3 DC** for magical flames
>>     
>> - **Optional:** +1 DC per 30 ft closer
>>     
>> - **If a creature is on fire:** use the flame category appropriate to its size (DC 13–15)
>   
>> ###  **Averting Gaze**
>> 
>> As an **action**, the cursed may avert their eyes:
>> 
>> - **Advantage** on hypnosis saves
>>     
>> - **Disadvantage** on attack rolls
>>     
>> - Lasts until they look again or 1 minute passes  

---

### **II. FURY STATE (Transformation)**

When the cursed fails a fire-hypnosis save, they enter **Fury State** for 1 minute (10 rounds).  
They no longer behave normally, but remain **in control of their choices**—the curse pushes, it does not dominate.

The Fury’s internal temperature skyrockets as “Pressure” builds until they combust.

---

####  **Entering Fury State**

Start at **Pressure 1, 2, or 3** depending on the flame size that triggered the curse:

|Flame Type|Starting Pressure|
|---|---|
|Medium|**1**|
|Large|**2**|
|Massive|**3**|

---

### **III. FURY STATE FEATURES**
> [!column|3 no-title]
>> ###  **1. Thermal Predator**
>> 
>> While transformed:
>> 
>> - Speed +10 ft
>>     
>> - Advantage on Perception checks to locate heat sources or living creatures
>>     
>> - The Fury is _compelled_ to approach the largest group of creatures it senses  
>>     _(You choose the path and tactics — this is strong instinct, not mind control.)_
>>    
>> You cannot willingly take the **Disengage** or **Dodge** action.
>
>> ###  **2. Smoldering Body**
>> 
>> - You shed bright light (10 ft) and dim light (20 ft).
>>     
>> - A creature that touches you or ends its turn grappling you takes  
>>     **fire damage = PB + CON mod**.
>   
>> ###  **3. Fire-Drunk Focus**
>> 
>> You have **disadvantage on ranged attack rolls** and **advantage on melee attacks**, reflecting tunnel-vision toward close heat sources.


### **IV. PRESSURE SYSTEM**

Each round, your internal temperature rises. This is what eventually forces the explosion.
> [!column|3 no-title]
>> ### **Pressure Gain**
>> 
>> At the **end of each of your turns**, gain **1 Pressure**.
>
>> ### **Instant Pressure Gains**
>> 
>> - Become frightened → +1 Pressure
>>     
>> - Take cold damage → +2 Pressure
>>     
>> - End your turn adjacent to 3+ creatures → +1 Pressure
>>     
>> - Hit by water or drenched → **No gain this round** (steam flash)
>    
>> ### **Pressure Threshold**
>> 
>> When you reach **Pressure 6**, you immediately explode.

### V. Mitigation Pressure
Explosion is **not inevitable** if you can act to reduce or halt Pressure:
> [!column|3 no-title]
>> #### **1. Environmental Mitigation**
>> 
>> - Move away from heat sources
>>     
>> - Enter a non-burning area
>>     
>> - Extinguish nearby flames  
>>     _(DM may allow a Wisdom or Constitution check to halt automatic Pressure gain each turn)_
>    
>> #### **2. Venting Actions (Optional Rule)**
>> 
>> - Spend **1 action** to “vent” pressure:
>>     
>>     - Reduce Pressure by 1–2 (DM discretion)
>>         
>>     - Take 1d4 fire damage or gain 1 level of exhaustion
>>         
>> - Represents self-control or partial cooling
>    
>> #### **3. Temporary Suspension**
>> 
>> - Being soaked by water or magical ice can halt Pressure gain for 1 round

### **VI. EXPLOSIVE CRESCENDO (The Fury Explosion)**

When you hit Pressure 6, you combust in a devastating pyroclastic burst.

####  **Volcanic Burst**

All creatures within **20 ft** must make a Dexterity saving throw:  
**DC = 8 + PB + CON mod**
> [!column|2 no-title]
>> **Failure:**
>> 
>> - **18d10 fire damage**
>>     
>> - Knocked prone
>    
>> **Success:**
>> 
>> - Half damage
>>     
>> - No knockdown 

The explosion coats the area in burning molten blood. The affected ground becomes **difficult terrain** until the flames fully die out (**1d10 minutes**).

A creature that enters the area or starts its turn there while the ground is still burning takes **(minutes remaining)d6 fire damage**.


---
> [!column|2 no-title]
>> ### **VII. AFTERMATH**
>> 
>> Immediately after exploding:
>> 
>> - You collapse **unconscious** at **1 HP**
>>     
>> - Stable
>>     
>> - Cannot awaken until **all flames within 20 ft are extinguished**
>>     
>> - Upon awakening, gain:
>>     
>>     - **1 level of exhaustion**
>>         
>>     - **Vulnerability to cold damage for 24 hours**
>>         
>> 
>> Pressure resets to **0**.
>
>> ### **VIII. OPTIONAL QUIRKS (Roleplay Flavor)**
>> 
>> Roll 1d6 or choose:
>> 
>> 1. Smoke leaks from your nostrils when lying or anxious
>>     
>> 2. You become “fire-drunk” and euphoric near flames
>>     
>> 3. Eyes flicker like embers in dim light
>>     
>> 4. You stare too long at lanterns and candles
>>     
>> 5. Preference for hot food, hot drinks
>>     
>> 6. Tiny scorch marks appear where you walked while angry

---



### **Fury State Duration:** 1 minute or until explosion.
## Notes

[Player Handout](https://docs.google.com/document/d/1_eFTuK3teRJSAVbd2QSZxjDTgE_RZH54zZg-3Eoo4Hk/edit?usp=sharing)

