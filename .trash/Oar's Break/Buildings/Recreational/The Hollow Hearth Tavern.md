---
tags:
  - Location
  - POI
  - Shop
location:
  - "[[Oar's Break]]"
mapmarker:
art: 99 Images/z_Assets/POIs/BearAndBottle.png
aliases:
poiType:
  - Shop
dominion: []
owners: []
assistants: []
organizations: []
currentLocation: []
tradePartners:
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

From the outside, **The Hollow Hearth** leans slightly into the street like a drunk too proud to fall. Its dark timber walls are stained with soot and laughter, and above the swinging sign—a fire-blackened chunk of stone shaped like a heart—the smell of ale and roasted meat spills into the air, pulling in locals and wanderers alike.

Inside, the tavern is **rowdy, warm, and permanently a little too loud**. The central hearth, the tavern’s namesake, has a wide crack running through the stone foundation—**an old wound from a chimney fire three decades ago**. Instead of fixing it, the owners just cleared the ash and built around it, leaving the fireplace more symbolic than functional. Above it, someone’s scrawled in charcoal: _Still Warmer Than the Mayor’s Bed_.

To the right of the hearth, hammered into the cracked stone with iron nails, hangs a crooked **[[Bounty board]]**, made of mismatched planks and half-charred parchment. The papers flutter in the draft from the door—some marked with fresh ink, others so old the names have faded. Locals call it **“The Wall of Regrets”**, though plenty of mercenaries and desperate farmhands call it something closer to rent. **Jobs range from monster sightings and stolen pigs to suspicious disappearances and worse.** Tuck says he doesn’t run it, but **he’s always the one who pays out**, and the ink on the oldest contracts looks a lot like his handwriting.

**[[Thoma Wren]]**, the barkeep, has run the place since the last owner disappeared during a card game gone wrong. No one knows if Tuck won or lost—**and anyone who asks tends to get a stale heel of bread and no eye contact**. He’s a wiry man with a quick hand for pouring and a quicker one for stashing coin. His signature move is to **laugh at a joke a second too late**, like he was somewhere else entirely. Locals say **he was a sailor once**, or a smuggler, or both—but again, **don’t ask questions unless you want your drink served sideways.**

The regulars include:

- **[[Big Yolla]]**, who arm-wrestles for drinks and always wins.

- **[[Pip and Nerik]]**, twin halflings who sing dirty duets off-key, with harmonies that can clear a room.

- **[[Sawbones Varrick]]**, a retired field medic who drinks to forget, but keeps remembering.


At any given hour, **someone is dancing, someone is arguing**, and someone is trying to sleep in a booth using a scarf as a curtain. The back room is **off-limits**, but coin has a way of making doors open—though **rumor says Tuck keeps a ledger back there with names that don’t match faces.**

Despite the chaos, Hollow Hearth is **weirdly safe**, like a storm you’ve learned to sail through. **Fights break out, but knives stay sheathed**, and anyone who breaks a bottle without paying gets mopped up by Big Yolla and dumped in the canal.

They say if you sit by the cracked hearth long enough, someone will offer you a job, a secret, or a way out of town.  
**They just won’t tell you which until it’s too late.**

## Database

![[Database - POI Note.base]]

## Goods & Services

### Goods:
#### The Hollow Hearth Menu

|**Item**|**Description**|**Cost**|
|---|---|---|
|**Crackfire Stew**|Thick rabbit stew with charred leeks and cracked pepper, served in a scorched bowl.|8 cp|
|**Drunkard’s Pie**|Savory meat pie stuffed with turnip, venison, and ale-soaked onions.|1 sp|
|**Scarf Bread**|Flat, chewy bread “stitched” with garlic and sea salt, always slightly stale.|3 cp|
|**Big Yolla’s Ribs**|Smoked boar ribs, slathered in a honey-ale glaze. One rib is enough.|2 sp|
|**Sleepy Boar Sausage**|Cured sausage mixed with calming herbs—might help you nap through a tavern brawl.|7 cp|
|**Canal Eel (Fried)**|Fresh-caught eel fried in ash-ale batter. Crunchy, salty, maybe still watching.|6 cp|
#### Drinks & Spirits

|**Drink**|**Description**|**Cost**|
|---|---|---|
|**Ash Ale**|The house staple—dark, smoky, and bitter as local gossip.|4 cp|
|**Charcoal Stout**|Black as the hearthstone, with a kick that arrives after the third gulp.|6 cp|
|**Sootshine**|Illicit clear spirit—tastes like regret and burns twice. Ask Tuck quietly.|1 sp|
|**Hearth’s Ember**|Sweet mulled wine spiced with cloves and a splash of orange bark tincture.|5 cp|
|**Whispersap**|Syrupy cordial with calming effects—"for when the twins won’t shut up."|8 cp|
|**Barrel Bottom Special**|Mystery drink. Could be stout. Could be vinegar. Roll a d6.|2 cp|

### Services:

| Name    | Price (gp) | Information / Description |
| ------- | ---------- | ------------------------- |
| Example | 0.1        |                           |

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


#### Drinks & Spirits

|**Drink**|**Description**|**Cost**|
|---|---|---|
|**Ash Ale**|The house staple—dark, smoky, and bitter as local gossip.|4 cp|
|**Charcoal Stout**|Black as the hearthstone, with a kick that arrives after the third gulp.|6 cp|
|**Sootshine**|Illicit clear spirit—tastes like regret and burns twice. Ask Tuck quietly.|1 sp|
|**Hearth’s Ember**|Sweet mulled wine spiced with cloves and a splash of orange bark tincture.|5 cp|
|**Whispersap**|Syrupy cordial with calming effects—"for when the twins won’t shut up."|8 cp|
|**Barrel Bottom Special**|Mystery drink. Could be stout. Could be vinegar. Roll a d6.|2 cp|