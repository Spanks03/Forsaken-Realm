---
tags:
  - Location
  - POI
  - Shop
location:
  - "[[Oar's Break]]"
mapmarker:
art: 99 Images/z_Assets/POIs/BrimasBlades.png
aliases:
  - Ironroot Forge
poiType:
  - Shop
dominion: []
owners:
  - "[[Brenna Ironroot]]"
assistants: []
organizations: []
currentLocation: []
tradePartners:
shopType:
  - Blacksmith
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
>> **Type** | `INPUT[ShopType][inlineListSuggester:shopType]` |
>> **Nation** | `INPUT[Nation][inlineListSuggester(optionQuery(Nation AND !"98 Templates"), useLinks(partial)):nation]` |
>> **Owners** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"98 Templates"), useLinks(partial)):owners]` |
>> **Assistants** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"98 Templates"), useLinks(partial)):assistants]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"98 Templates"), useLinks(partial)):organizations]` |
>> **Location** | `INPUT[Location][inlineListSuggester(optionQuery(#Location AND !"98 Templates"), useLinks(partial)):location]` |

> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> 
> # Info
> | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Type** | `VIEW[{shopType}][text]` |
> | **Nation** | `VIEW[{nation}][link]` |
> | **Owners** | `VIEW[{owners}][link]` |
> | **Assistants** | `VIEW[{assistants}][link]` |
> | **Organizations** | `VIEW[{organizations}][link]` |
> | **Location** | `VIEW[{location}][link]` |
> 
> # [[Travel Calculator]] 
> | |
> |---|---|
> | **TBD** | `VIEW[round(52 / (({Travel Calculator#MilesPerHour}*{Travel Calculator#HoursPerDay})*{Travel Calculator#SpeedMultiplier}),1)]` Day(s)
> | **TBD** | `VIEW[round(0.5 / ({Travel Calculator#MilesPerHour} * {Travel Calculator#SpeedMultiplier}) * 60, 1)]` Minute(s)

# `=this.file.name`

> [!quote]- Scene Introduction
> A script to read from when the party arrives to the point of interest for the first time to set the scene.

Tucked near the northern edge of Oar’s Break, where the earth rises slightly and the wind always smells faintly of soot and iron, **Ironroot Forge** stands squat and resolute—**a blackened stone building with a roof darkened by years of smoke and grit**. The wide, open-mouthed workspace glows from within like the heart of a volcano. Even from the road, the rhythmic **clang of Brenna’s hammer** echoes out in steady beats, like the heartbeat of the town itself—constant, reliable, unrelenting.

Inside, **heat presses against your skin like a thick, invisible blanket**, and the air carries a mix of metallic tang, scorched coal, and sweat. Sparks snap from the anvil like fireflies on the attack. Racks of tools line the walls in perfect order—**from delicate pliers used to set filigree into a sword hilt to sledgehammers that could knock a bull to its knees.** Every item has its place. Every corner is swept clean. The only mess is in motion—flying sparks, steam from quenched blades, and the ever-turning bellows that breathe life into the flame.

**[[Brenna Ironroot]]**, broad-shouldered and dusted in soot, works with a rhythm that borders on sacred. Her hair is usually tied up in a knot of leather cords, her sleeves rolled and thick arms rippling with every strike. She speaks little unless spoken to—and even then, prefers nods, shrugs, or pointed gestures to unnecessary words. Yet her silence isn’t cold; it’s just focused, like everything she does. A compliment from her—a simple “It’ll hold” or “Good eye”—**feels like being knighted**.

Weapons, tools, horseshoes, wagon axles, intricate door hinges—**if it’s forged metal in Oar’s Break, it came from her hands**. Her signature mark, a tiny root wrapping around an iron nail, is etched into the hilt or heel of each piece she makes. Locals say you can trust a blade by the weight of it—and by whether it bears **Brenna’s root**.

She takes custom work, but only if she likes the reason. Ask her for a fancy sword and she might scoff. Ask her for a wedding ring forged from your family’s old plow, and she might pause, nod once, and begin without another word.

At night, the forge glows softly in the dark, and sometimes the clangs continue even then—though nobody ever sees Brenna leave or light the lanterns. Some say she was born of the mountain. Others say she just **loves her work more than sleep.**

## Database

![[Database - POI Note.base]]

## Goods & Services

### Goods:
#### Items on Hand (Ready to Purchase)

While Brenna prefers to forge on commission, her wall racks and locked chests carry a rotating stock of commonly requested goods, all bearing her **root-and-nail signature**.

|Item|Quantity|Price (Standard)|Notes|
|---|---|---|---|
|Longswords (martial)|2|25 gp|Functional and balanced. No frills.|
|Battleaxe|1|20 gp|One solid piece. Well-weighted.|
|Spears (simple)|3|6 gp|Iron tips, ashwood shafts.|
|Light Hammer|2|8 gp|Compact. Usable as tool or weapon.|
|Shield (iron-rimmed wood)|2|10 gp|Burned with stylized knot designs.|
|Studded Leather Armor (light)|1|45 gp|Fitted for average build.|
|Scale Mail (medium)|1|50 gp|Old design, reinforced under armpits.|
|Chainmail (heavy)|1|75 gp|Gleaming rings, minimal rusting.|
|Arrows (20)|5 bundles|1 gp|Ironroot tips, fletched locally.|
|Horseshoes (set of 4)|6 sets|5 sp|She’ll nail them in for free if you’re polite.|
|Iron Nails (bag of 50)|—|1 sp|Always available. Ask the apprentice.|
|Smith’s Tools|1 set|20 gp|Wrapped in oiled leather. Durable.|

### Services:
####  Custom Work

Brenna will forge to order—but **only if she likes the reason.** A flashy noble asking for a gilded saber? Probably not. A farmer asking for a sword forged from the plow that broke saving their kid? She’s already firing the coals.

She does **not** haggle. But if she respects the request, or likes you, the price may just come out lower—though she’ll never explain why.

| Item                                                             | Price (Standard) | Price (Friends/Locals/“Good Reason”)        |
| ---------------------------------------------------------------- | ---------------- | ------------------------------------------- |
| **Simple Weapons** (clubs, maces, spears, etc.)                  | 5–10 gp          | 4–8 gp                                      |
| **Martial Weapons** (longswords, warhammers, greatswords, etc.)  | 15–50 gp         | 12–40 gp                                    |
| **Ammunition** (20 arrows, bolts, etc.)                          | 1 gp             | 8 sp                                        |
| **Shield** (wood or iron-rimmed)                                 | 10 gp            | 8 gp                                        |
| **Light Armor** (padded, leather, studded leather)               | 5–45 gp          | 4–35 gp                                     |
| **Medium Armor** (hide, chain shirt, scale mail)                 | 10–50 gp         | 8–40 gp                                     |
| **Heavy Armor** (ring mail, chainmail, splint)*                  | 30–200 gp        | 25–175 gp                                   |
| **Smith’s Tools, Tinker’s Tools, etc.**                          | 20 gp            | 15 gp                                       |
| **Iron Nails, Horseshoes (set of 4), Hinges, Basic Metal Goods** | 1–5 sp           | Often tossed in if you’re patient or polite |

 _Splint and plate armor take 2–4 weeks and cost extra for materials unless brought by the customer._


## Present

<font color="#ffc000">**Trade Partners:**</font> `VIEW[{tradePartners}][link]`

### Local Inhabitants (Random Encounter):

| `dice: 1d20\|noform` (Result) | Name    | Information / Description |
| ----------------------------- | ------- | ------------------------- |
| 1                             | Example |                           |

### Current Events:

> *<font color="#7f7f7f">- Example Quest</font>*
> *<font color="#7f7f7f">    - Summary of a quest the player can get involved in.</font>*
> *<font color="#7f7f7f">- Example Event</font>*
> *<font color="#7f7f7f">    - Summary of an event that's going on in the area which may not relate to a specific quest or may relate to multiple.</font>*

## Past

### History:

> *<font color="#7f7f7f">What key events have shaped this continent over time? Consider ancient civilizations, major wars, migrations, natural disasters, or political shifts. How has its past influenced the cultures, borders, and conflicts that exist today?</font>*

### Secrets, Rumours & Legends:

> *<font color="#7f7f7f">What hidden truths or mysteries lie across the continent? These could include lost kingdoms, ancient technologies, forbidden magic, hidden societies, or concealed geopolitical agendas. Who knows about them and what would it mean if they were revealed?</font>*


## Notes


---
