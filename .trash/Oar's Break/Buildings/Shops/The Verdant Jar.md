---
tags:
  - Location
  - POI
  - Shop
location:
  - "[[Oar's Break]]"
mapmarker:
art: 99 Images/z_Assets/POIs/DancingHourglass.png
aliases:
poiType:
  - Shop
dominion: []
owners:
  - "[[Renwin Mossfoot]]"
assistants:
  - "[[Gellen the Mute]]"
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

Stepping into **The Verdant Jar** is like entering a living tapestry of greens and scents, where sunlight filters softly through stained glass jars filled with vibrant powders and swirling liquids. Shelves groan beneath the weight of countless vials, each glowing with hues of amber, emerald, ruby, and sapphire—colors that promise healing, protection, or quiet magic. Bundles of herbs hang from the rafters, their dried leaves whispering faintly in the gentle breeze that drifts through the open windows, carrying the mingled fragrances of mint, lavender, and wildroot.

At the heart of this alchemical nursery moves **[[Renwin Mossfoot]]**, a calm and steady presence whose soft voice often drifts into quiet conversation with the plants around her. Her slender fingers brush gently over leaves and stems, and sometimes, if you listen closely, the faintest rustle or sigh answers back—as if the very greenery is alive and aware. Renwin’s eyes, steady and bright, reflect a deep understanding of nature’s subtle rhythms, and her alchemical experiments blend old wisdom with a touch of whispered secrets.

Tucked alongside vials and bundles, you’ll find a modest corner dedicated to the quieter talents of her husband, **[[Gellen the Mute]]**. Here, delicate wooden birds perch on small shelves, their carved feathers smooth and lifelike, and hand-rolled cigars wrapped in tobacco hang neatly beside pouches of fragrant herbs. Renwin’s pride in Gellen’s craftsmanship is quietly evident—she often encourages visitors to explore these handcrafted tokens and soothing tobaccos, sharing the stories behind each with a warm smile.

The air hums with possibility—a mixture of earth, magic, and love—where each vial holds a story, every dried sprig a promise, and every wooden bird or tobacco cigar carries the patient care of hands that speak in silence. Visitors find in **The Verdant Jar** a place of calm, knowledge, and wonder—where nature’s quiet magic pulses softly beneath Renwin’s careful hands, and the gentle craft of Gellen’s creations finds its own quiet voice.

## Database

![[Database - POI Note.base]]

## Goods & Services

### Goods:

|Item|Price (Standard)|Price (Friends/Locals)|Notes|
|---|---|---|---|
|Goodberries (per berry)|5 gp|4 gp|Magical berries that heal 1 HP each|
|Healing Potion (Standard)|50 gp|40 gp|Restores 2d4+2 HP|
|Poison (basic, vial)|100 gp|80 gp|Deals 1d4 poison damage on hit|
|Acid (vial)|25 gp|20 gp|Deals 2d6 acid damage on contact|
|Healing Herbs (dried, per dose)|10 gp|8 gp|Used to make poultices or teas|
|Antitoxin Potion|50 gp|40 gp|Neutralizes poisons|
|Sleep Draught|25 gp|20 gp|Induces restful sleep|
|Herbal Salve (healing balm)|15 gp|12 gp|Applied to wounds, soothes pain|
|Elixir of Resistance (acid, cold, fire, or poison)|75 gp|60 gp|Grants resistance for 1 hour|
|Rare Herb Bundles (Moonleaf, Nightbloom)|40 gp|30 gp|Used for advanced alchemy or rituals|
|Plant-based Dyes (natural colors)|5 gp|4 gp|For cloth, leather, and decorative use|

| Item                                | Price (Standard) | Price (Friends/Locals) | Notes                                             |
| ----------------------------------- | ---------------- | ---------------------- | ------------------------------------------------- |
| Small Wooden Bird (carving)         | 2 sp             | 1 sp                   | Hand-carved, painted; believed to bring good luck |
| Wooden Bird (set of 3)              | 1 gp             | 6 sp                   | Varied species; perfect for decoration or gifts   |
| Bird Whistle (wooden)               | 5 sp             | 2 sp                   | Produces a clear, sweet chirp when blown          |
| Pipe Tobacco (small pouch)          | 7 sp             | 5 sp                   | Hand-dried, aromatic blend                        |
| Tobacco Pipe (wooden)               | 1 gp             | 8 sp                   | Simple yet well-crafted pipe, smooth finish       |
| Bundle of Smoking Herbs             | 5 sp             | 3 sp                   | Mild herbs for calming or ritual use              |
| Standard Cigar                      | 7 sp             | 5 sp                   | Rolled tobacco cigar, for leisure and reflection  |
| Healing Cigar (like Goodberries)    | 60 gp            | 45 gp                  | When smoked, heals 3d4 +5 HP over 10 minutes      |
| Restful Cigar (short rest effect)   | 300 gp           | 250 gp                 | Smoking grants effects of a short rest (1 hour)   |
| Deep Dream Cigar (long rest effect) | 1000 gp          | 750 gp                 | Smoking grants effects of a long rest (8 hours)   |

### Services:


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


