---
tags:
  - Location
  - POI
  - Shop
location:
  - "[[Oar's Break]]"
mapmarker:
art: 99 Images/z_Assets/POIs/JirisShop.png
aliases:
  - The Braided Ram Inn
poiType:
  - Shop
dominion: []
owners:
  - "[[Lette Braidshear]]"
assistants: []
organizations: []
currentLocation: []
tradePartners:
shopType:
  - Inn
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

Nestled near the heart of Oar’s Break, just off the cobbled crossroads where most foot traffic naturally converges, the **Braided Ram Inn** stands as a cornerstone of comfort and conversation. The sign above the door—a wooden ram’s head with real rope horns, meticulously braided and replaced each spring—sways gently in the breeze, creaking like it’s in on the latest joke.

The inn's wide oak door opens to a rush of warmth and the inviting scent of **[[Lette Braidshear]]’s famous stew**, a rich, savory concoction of root vegetables, thick gravy, and cuts of meat so tender they surrender to a spoon. The hearth is always ablaze, no matter the season, casting dancing firelight across braided wall tapestries that tell winding stories of local legends, farming cycles, and a few cheeky scenes added over the years by mischievous weavers.

The **common room buzzes with life**—clinks of mugs, muttered deals over dice games, and the occasional burst of laughter rising over the steady hum of gossip. The wooden floors are worn smooth by boots and time, with a few creaky boards near the fireplace that everyone knows to step around (unless you want the whole room’s attention).

Behind the long, polished counter stands **Lette**, the inn’s owner and matron, built sturdy and unshakable like the Ram itself. She has flour on her sleeves, a ladle always within reach, and a sharp memory for faces—especially those who eat but don’t pay. She doesn’t need to raise her voice to command the room; a look or a click of her tongue usually does the trick. Yet to travelers and townsfolk alike, she’s as reliable as sunrise, quick with a refilled mug, a fresh blanket, or a pointed warning when needed.

The **guest rooms upstairs** are small but spotless, with lavender bundles hung by the windows and hand-stitched quilts on every bed. The walls are thick enough to dull even the loudest snores—or the whispered confessions of those lulled by firelight and ale.

In Oar’s Break, **news travels fast**, but it almost always starts here—with a bowl of stew, a warming cup of cider, and the gentle clatter of life unfolding in the inn where everyone eventually ends up. Whether you're a farmer with aching feet or a stranger with questions in your eyes, **The Braided Ram will take you in—if Lette says so**.
## Database

![[Database - POI Note.base]]

## Goods & Services

### Goods:
#### **Braided Ram Inn Menu**

|Item|Description|Price (Standard)|Price (Friends/Locals)|
|---|---|---|---|
|**Lette’s Famous Stew**|Thick, hearty stew of root veggies and tender meat|5 sp|3 sp|
|**Freshly Baked Bread**|Warm, crusty loaf served with herb butter|2 sp|1 sp|
|**Roasted Root Vegetables**|Seasonal mix, slow-roasted with herbs|3 sp|2 sp|
|**Ale (Mug)**|Rich, dark ale brewed locally|4 sp|3 sp|
|**Honey Mead (Mug)**|Sweet and smooth, with a hint of wildflowers|6 sp|4 sp|
|**Cheese and Pickles Plate**|Local cheeses paired with pickled vegetables|4 sp|3 sp|
|**Sweetberry Tart**|Seasonal berries in flaky pastry|3 sp|2 sp|

### Services:
#### **Braided Ram Inn Room Prices**

|Room Type|Description|Price per Night (Standard)|Price per Night (Friends/Locals)|
|---|---|---|---|
|**Common Room**|Shared space with bunks and basic bedding|5 sp|3 sp|
|**Private Room**|Small, single room with simple furnishings|2 gp|1.5 gp|
|**Larger Private Room**|Spacious room with a sturdy bed and chest|3 gp|2 gp|
|**Suite**|Room with a fireplace, larger bed, and seating area|5 gp|3.5 gp|

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


