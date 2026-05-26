---
tags:
  - Location
  - World
location:
mapmarker:
art: "[[ParchmentTerra.jpg]]"
aliases:
  - Terra
dominion:
  - Ogul
  - Nosduh
organizations: []
currentLocation:
  - Forsaken Realm
---

> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!{art}][text(renderMarkdown)]`
> 
> # Info
> | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Dominion** | `VIEW[{dominion}][link]` |
> | **Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`

> [!quote]- Scene Introduction
> A script to read from when the party arrives to the planet for the first time to set the scene.

> *<font color="#7f7f7f">Write a short summary of the world, highlighting its most defining traits such as it's environment, atmosphere, and its role or significance.</font>*

## Map

> [!metadata|map] Map
> ```leaflet  
>id: TerraMap ### Must be unique with no spaces  
>image: 
>- [[Terra Map (High Res).jpg]] ### Link to the map image file. Do not add a ! in front of the image 
>- [[Terra Region  Map.jpg]]
>bounds: [[0,0], [6144, 8192]] ### Size of the map in px Height_y, Width_x. Ignore 0,0  
>height: 545px ### Size of the leaflet embed in px on your screen  
>width: 100% ### Size of the leaflet embed in your note  
>lat: 3072 ### To center the map, make this half of the map height.  
>long: 4096 ### To center the map, make this half of the map width.  
>minZoom: -3.5 ### Controls how far away from the map you can zoom out. Hover over the target icon to see the current level.  
>maxZoom: 1 ### Controls how far towards the map you can zoom in. Hover over the target icon to see the current level.  
>defaultZoom: -3.5 ### Sets the default zoom level when the map loads. Hover over the target icon to see the current level.  
>zoomDelta: 0.2 ### Adjust how much the zoom changes when you zoom in or out.  
>unit: mi ### The value displayed when measuring so you know what type of unit is being measure.  
>scale: 4.830917874396135 ### Real units/px (resolution) of your map  
>recenter: true  
>darkmode: false ### markermarker: default,2160,2752,Oar's 
>```

## Database

![[Database - Planet Note.base]]

### History:

> ![[Database - Timelines.base]]

### Secrets, Rumours & Legends:

> *<font color="#7f7f7f">What hidden truths or mysteries lie across the world? These could include lost kingdoms, ancient technologies, forbidden magic, hidden societies, or concealed geopolitical agendas. Who knows about them and what would it mean if they were revealed?</font>*

## Notes

