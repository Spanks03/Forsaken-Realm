---
tags:
  - Location
  - POI
  - Shop
location:
  - "[[Oar's Break]]"
mapmarker:
art: 99 Images/PlaceholderPointOfInterest.png
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

Nestled at the crossroads of the town square, under a faded green awning patched with love and old canvas, sits **[[Lysa Hayweather]]’s produce stall**—a crooked table overflowing with turnips, radishes, leeks, and whatever else is in season or sneaked in from a nearby farm.

What sets this stall apart isn’t the vegetables—it’s **Lysa’s smile**. Sweet, ever-knowing, and just a touch too amused, **Lysa has been listening longer than most folk have been alive.** She's the kind of woman who sells you a handful of ripe tomatoes while whispering, _"Tell your sister to stay off the roof this time, would you?"_

She **never gossips**, but everyone talks to her anyway. They say she knows **who’s cheating, who’s lying, and who’s hiding something in the old shed out by the creek.** She’s the keeper of the town’s unspoken truth: **secrets are safer when they’re planted like seeds and left alone.**

The stall itself is **cluttered but charming**. Handwritten signs hang from bits of twine, prices smudged and rewritten in charcoal. A fat white rooster named **Turnip** guards the back crates and pecks at anyone who tries to haggle too hard.

Lysa doesn’t barter. She doesn’t haggle. She tells you the price, and it’s always fair—even if sometimes **it feels like you’re paying for more than just carrots**.

Children love her candied apples, and old men leave her wildflowers for no reason at all. She never married, never left town, and **always seems to know what storm’s coming next—weather or otherwise.**

If you're looking for information, **she won’t tell you a thing. But she might sell you an onion that makes you cry just the right amount.**

## Database

![[Database - POI Note.base]]

## Goods & Services

### Goods:

#### **General Inventory** 

_(Prices follow 5e PHB for goods when applicable)_

|**Item**|**Price (Normal)**|**“If she likes you” Price**|
|---|---|---|
|Fresh carrots (bundle)|1 cp|Free with another purchase|
|Leeks, radishes, beets|1 cp per item|5 for 3 cp|
|Tomatoes (plump, ripe)|2 cp|1 cp|
|Strawberries (basket)|5 cp|3 cp|
|Candied apple (children’s favorite)|3 cp|2 for 5 cp if you bring kids|
|Wild mushrooms (local)|4 cp (risky types)|“Tell me what you’re cooking” discount applies|
|Dried herbs (sage, thyme)|1 sp per pouch|6 cp if you compliment her sign handwriting|
|Lavender bunch (fresh)|3 cp|“You look like you need this” freebie possible|
|Eggs (from Turnip’s coop)|2 cp per egg|1 cp per egg or “pay what’s right”|
|Honey jar (small, from a friend)|1 sp|7 cp if you’re kind to animals|
|Pickled vegetables (jarred)|6 cp|“Pick your favorite” and round down|

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
