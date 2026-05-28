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
  - "[[Marnick Turrow]]"
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

Down by the banks of the meandering creek that slips lazily along Oar’s Break’s western edge, the **Oldstone Mill** leans ever so slightly with age, as though bowing politely to time. Its squat frame is built from thick blocks of river-rounded stone, mottled with moss and lichen that seem to change color with the weather. The waterwheel groans as it turns — slow, deliberate, and never quite silent — a creaking lament that’s become part of the town’s ambient rhythm. Children mimic it in jest. Old-timers swear they can hear it in their bones.

Inside, the air hangs thick with flour dust, soft as fog and just as intrusive. It clings to every beam and sack, settling into the folds of clothing, into the creases around your eyes and nose. Wooden gears clunk and sigh as the great stone millstones grind grain with a dull, thunderous patience. The scent is earthy and warm — crushed wheat and dry husk, with a faint undertone of sweat and old leather.

[[Marnick Turrow]] works the mill like a man who lost a bet to it long ago and now honors the terms with grudging loyalty. A stooped figure with shoulders like bundled rope and hands permanently dusted in white, he moves with surprising purpose between sacks, levers, and stone. His beard is long, yellowed in places from pipe smoke and tea, and often holds a crumb or two, unnoticed and unbothered.

He talks almost constantly — mostly to himself, occasionally to the grain, rarely to customers, unless you're buying. And even then, the conversation is a one-way road paved in curmudgeonly wisdom:

  “You know, back _last season_, the wheat didn’t crumble like this. Whole heads, clean as a whistle — now? Cracked and lazy, like everything else.”

Every season was better than the one you’re currently in. Every bag of flour is a shadow of the glory days. And if you dare ask _when_, exactly, these good days were, Marnick will only grunt and say, “You weren’t there, so don’t bother pretending.”

Despite the grumbles, the townsfolk rely on Marnick’s flour — and truth be told, they respect the man. Not because he’s friendly (he isn’t), but because every sack he sells is ground with an attention bordering on reverence. He measures by hand, tests by taste, and can spot an off-batch before it hits the hopper.

The building hums when it’s quiet, like it remembers things. Some say Marnick does too, though he’d never admit it.

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




