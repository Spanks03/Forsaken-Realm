---
tags:
  - Location
  - World
location:
mapmarker:
art: "[[PlaceholderPlanet.png]]"
aliases:
worldType:
dominion: []
organizations: []
currentLocation:
---

> [!metadata|info] Tip for Bag of Tips
> This can be used for Worlds and Moons. You could even make work for objects in space such as large Asteroids!

> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!{art}][text(renderMarkdown)]`
> 
> # Info
> | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Type** | `VIEW[{worldType}][text]` |
> | **Dominion** | `VIEW[{dominion}][link]` |
> | **Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`

> [!quote]- Scene Introduction
> A script to read from when the party arrives to the planet for the first time to set the scene.

> *<font color="#7f7f7f">Write a short summary of the world, highlighting its most defining traits such as it's environment, atmosphere, and its role or significance.</font>*

## Database

![[Database - Planet Note.base]]


## Map

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

### Current Events:

> *<font color="#7f7f7f">- Example Quest</font>*
> *<font color="#7f7f7f">    - Summary of a quest the player can get involved in.</font>*
> *<font color="#7f7f7f">- Example Event</font>*
> *<font color="#7f7f7f">    - Summary of an event that's going on on this world which may not relate to a specific quest or may relate to multiple.</font>*

## Past

### History:

> *<font color="#7f7f7f">What key events have shaped this world over time? Consider ancient civilizations, major wars, migrations, natural disasters, or political shifts. How has its past influenced the cultures, borders, and conflicts that exist today?</font>*

### Secrets, Rumours & Legends:

> *<font color="#7f7f7f">What hidden truths or mysteries lie across the world? These could include lost kingdoms, ancient technologies, forbidden magic, hidden societies, or concealed geopolitical agendas. Who knows about them and what would it mean if they were revealed?</font>*

## Notes

