---
tags:
  - Location
  - POI
location:
  - "[[Oar's Break]]"
mapmarker:
art: 99 Images/PlaceholderPointOfInterest.png
aliases:
poiType: []
dominion: []
owners:
  - "[[Halder Briarwind]]"
assistants: []
organizations: []
currentLocation: []
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

Just beyond the gentle bend of the river loop, where the wind rolls unbothered across the open earth, lies **Briarwind Farm** — a modest but sprawling patchwork of golden wheat, crooked vegetable rows, and meandering chickens fat on lazy days. The fields stretch toward the treeline like a sleeping animal, furrowed and sun-browned, buzzing with bees and the dry whisper of stalks brushing in the breeze. Old wooden fencing tilts slightly with age, trailing ivy climbing where nails have long since rusted.

A sagging barn, bleached silver by decades of sun, leans protectively near the farmhouse — a squat, weather-stained structure of cob and timber, its red clay tiles patched with moss. From the wide porch, you might catch a glimpse of [[Halder Briarwind]]: a man carved from quiet, with shoulders like stacked stones and a wide straw hat that shadows his face even at noon. His eyes are pale and unreadable, like unturned soil, and his words are measured and few.

He doesn’t greet strangers unless they come with coin in hand or hands ready to dig. When he speaks, it’s with the gravity of someone who counts his sentences like seeds — no waste, no fluff. “Take three, leave one,” he might say when you ask about carrots, or simply nod toward a bushel as if the vegetables can speak for themselves.

The scent of damp earth lingers thick in the air, joined by the faint musk of animals and the sweet green of crushed grass underfoot. A small chicken coop rattles with contented clucks, its residents more curious than their keeper, watching travelers with cocked heads and jerky steps. Sometimes, before the morning fog lifts from the riverbanks, a visitor might spot Halder tending the fields in silence, the mist swallowing his outline as if the earth itself were reclaiming him.

Locals don’t bother him much. They respect the rhythms of Briarwind Farm — and the man who keeps it growing.

## Database

![[Database - POI Note.base]]

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
