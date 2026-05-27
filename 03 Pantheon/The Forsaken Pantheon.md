---
tags:
  - Pantheon
  - Deity
  - Realm
location:
  - The Forsaken Realm
mapmarker:
art: "[[Cosmo.webp]]"
aliases:
worldType:
dominion: []
organizations: []
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
> | **Type** | `VIEW[{worldType}][text]` |
> | **Dominion** | `VIEW[{dominion}][link]` |
> | **Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`

> [!quote]- Scene Introduction
> A script to read from when the party arrives to the planet for the first time to set the scene.

> *<font color="#7f7f7f">Write a short summary of the world, highlighting its most defining traits such as it's environment, atmosphere, and its role or significance.</font>*

## Pantheon Tree

> [!metadata|map] Map
>```leaflet  
>id: PantheonBox ### Must be unique with no spaces  
>image: [[Pantheon.png]] ### Link to the map image file. Do not add a ! in front of the image  
>bounds: [[0,0], [2550, 3300]] ### Size of the map in px Height_y, Width_x. Ignore 0,0  
>height: 500px ### Size of the leaflet embed in px on your screen  
>width: 95% ### Size of the leaflet embed in your note  
>lat: 1275 ### To center the map, make this half of the map height.  
>long: 1650 ### To center the map, make this half of the map width.  
>minZoom: -2.3 ### Controls how far away from the map you can zoom out. Hover over the target icon to see the current level.  
>maxZoom: 1 ### Controls how far towards the map you can zoom in. Hover over the target icon to see the current level.  
>defaultZoom: -2.3 ### Sets the default zoom level when the map loads. Hover over the target icon to see the current level.  
>zoomDelta: 0.2 ### Adjust how much the zoom changes when you zoom in or out.  
>unit: mi ### The value displayed when measuring so you know what type of unit is being measure.  
>scale: 0.09328358208955223 ### Real units/px (resolution) of your map  
>recenter: false  
>darkmode: false ### marker
>```

## Ideal Gods
> ![[Database - IdealGods.base]]
## Lesser Gods
> ![[Database - LesserGods.base]]
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

