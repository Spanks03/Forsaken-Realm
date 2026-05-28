---
tags:
  - Location
  - POI
location:
  - "[[Oar's Break]]"
mapmarker:
art: 99 Images/z_Assets/POIs/IriusMansion.png
aliases:
  - Mayor's Manor
poiType: []
dominion: []
owners:
  - "[[Elira Voss]]"
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

Perched on a low rise just east of the town square, **Greystone Manor** stands with the kind of dignity that doesn’t demand attention — it simply has it. The estate is built of smooth, weathered stone, each block laid with intention, its gray facade dappled with ivy that climbs toward the slate roof like time itself trying to reclaim the place. No banners or embellishments mark it as a seat of power, but the calm symmetry of its architecture and the quiet hum of activity at its doors reveal its importance.

The manor is neither grand nor ostentatious — just _right_. Windows framed in dark-stained wood open to the scent of rosemary and lemon balm from the small garden nestled beside the entryway. The garden is Mayor Voss’s personal pride: neat rows of trimmed herbs, a pair of low peach trees, and a weathered bench beneath a wrought-iron trellis. In spring, the trellis blooms with white climbing roses, filling the air with their delicate perfume, softening the stone with a touch of grace.

Inside, the manor breathes warmth and order. Hardwood floors polished smooth with age echo faintly under booted feet, and the scent of old parchment and beeswax hangs in the air. A fireplace crackles in the main hall, casting amber light on shelves of well-read books, local ledgers, and records that track the pulse of Oar’s Break with a meticulous eye.

**[[Elira Voss]]** is often found at a simple oak desk by the garden-facing window, quill in hand, back straight, every movement measured. They are a tall, lean figure with silver-threaded hair bound back in a modest braid, and eyes the color of storm-washed stone. Voss speaks little, but when they do, people listen — not out of fear, but because their words carry weight, shaped by reason and the hard-won trust of years.

There is no bluster in their governance. Voss listens more than they speak, resolves conflict with clarity, and always leaves a conversation making the other person feel heard, even if the answer is no. To the townsfolk, they are less a ruler and more a keeper — of peace, of order, of Oar’s Break’s quiet way of life.

And though they rarely smile, when they do — in those rare garden moments, perhaps watching a bee dance between basil stems — it feels like sunlight through morning fog: brief, but enough to warm the day.

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




