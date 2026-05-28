---
tags:
  - Location
  - Area
art: "[[PlaceholderArea.png]]"
aliases:
terrain:
dominion:
organizations:
currentLocation:
---
> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!{art}][text(renderMarkdown)]`
> 
> # Info
> | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Terrain** | `VIEW[{terrain}][text]` |
> | **Dominion** | `VIEW[{dominion}][link]` |
> | **Location** | `VIEW[{currentLocation}][link]` |

> [!metadata|info] Tip for Bag of Tips
> This is an optional template which helps you break down your regions into areas, such as Mountainscape, Forests, Expansive Plains, etc.
> Use this template if you want to get more details or break down regions into more manageable chunks.

# `=this.file.name`

> <font color="#7f7f7f">Summarize the area by noting its overall size, climate, major landmarks, and the role it plays in the surrounding world.</font>

## Geography

### Flora & Fauna

> *<font color="#7f7f7f">Describe the plants and animals found in this area, noting how they adapt to the environment and what makes them unique or significant.</font>*

### Geographical Features:

> *<font color="#7f7f7f">What are the common traits, values, and traditions shared across the continent or how do they differ between regions? Describe languages, religions, customs, social structures, and how people interact within and across borders.</font>*

## Database

![[Database - Area Note.base]]

## Maps

> [!metadata|map] Map
> ```leaflet
> ### TUTORIAL: INSERT VIDEO LINK HERE
> ### Lines that start with ### are commented out, meaning they will not effect the code. Used to offer guidance. Feel free to remove these.
> ### Uncomment (Remove the ### ) height and width if you would like to manually set the height and width of the leaflet display.
> ### height: 600px
> ### width: 640px
> ### id: vallue will be replaced each time you create a new note.
> id: {{VALUE}}
> image: [[PlaceholderImage.png]]
> lock: true
> recenter: true
> noScrollZoom: false
> ### Leave the first [0,0], then replace the second [5000,5000] with [HEIGHT, WIDTH] of your image.
> bounds: [[0,0], [5000, 5000]]
> ### Use lat & long to set center point of the map.
> lat: 0
> long: 0
> ### Set min, max and default zoom to your desired zooms levels.
> minZoom: -3.5
> maxZoom: 6.5
> defaultZoom: -3.5
> zoomDelta: 0.5
> unit: miles
> ### Measure between two points you know the distance of, then scale up and down util you have your desired distance.
> scale: 0.0404
> ### MapIt is the tag we apply to notes we want to mark on the map. Replace "TBD" with whatever you like WITHOUT spaces.
> ### To add a marker to the map, include the MapIt- tag, and the location and mapmarker property within said note.
> markerTag: 
> - "#MapIt-TBD"
> ```

## Present

### Travel:

| `dice: 1d4\|noform` (Result) | Event                           | Infoamtion / Description                                                                                      |
| ---------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| 1                            | Nothing                         | Nothing eventful happens on this leg of the journey.                                                          |
| 2                            | Pass Traveling NPC              | You cross paths with a NPC(s), they are either uninterested with the party or are willing to have small talk. |
| 3                            | Interesting Sighting            | You spot something interesting, either something beautiful within nature or maybe a forgotten pouch of gold.  |
| 4                            | <font color="#ffff00">Encounter | Use the Random Encounter table below.                                                                         |

### Local Inhabitants (Random Encounter):

| `dice: 1d4\|noform` (Result) | Name   | Infoamtion / Description                                                         |
| ---------------------------- | ------ | -------------------------------------------------------------------------------- |
| 1                            | Bandit | A group of bandits are roaming the area, looking to score some gold.             |
| 2                            | Wolves | A hungry pack of wolves roam the treelines.                                      |
| 3                            | Troll  | A troll has wandered too far from it's cave... I thought you would like to know. |
| 4                            | Dragon | A dragon nests in the area, looking for a meal for it's harchlings.              |

### Current Events:

> *<font color="#7f7f7f">- Example Quest</font>*
> *<font color="#7f7f7f">    - Summary of a quest the player can get involved in.</font>*
> *<font color="#7f7f7f">- Example Event</font>*
> *<font color="#7f7f7f">    - Summary of an event that's going on in this worldscape which may not relate to a specific quest or may relate to multiple.</font>*

## Past

### History:

> *<font color="#7f7f7f">What key events have shaped this worldscape over time? Consider ancient civilizations, major wars, migrations, natural disasters, or political shifts. How has its past influenced the cultures, borders, and conflicts that exist today?</font>*

### Secrets, Rumours & Legends:

> *<font color="#7f7f7f">What hidden truths or mysteries lie across the worldscape? These could include lost kingdoms, ancient technologies, forbidden magic, hidden societies, or concealed geopolitical agendas. Who knows about them and what would it mean if they were revealed?</font>*

## Notes




