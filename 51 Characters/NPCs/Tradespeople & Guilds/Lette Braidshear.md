---
tags:
  - Character
  - NPC
art: 99 Images/Oar's Break Images/Pasted image 20250727150024.jpg
languages: Common
pronounced:
ancestry: Dwarf
gender: Female
pronouns:
age: 42
sexuality:
alignment: Neutral Good
occupation:
organizations:
ownedLocation:
  - "[[The Braided Ram Inn]]"
currentLocation:
  - "[[Oar's Break]]"
  - "[[The Braided Ram Inn]]"
condition:
aliases:
  - Lette
heritage: Hill Dwarf
party1Relation:
  - Neutral
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
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>> ---|---|
>> **Pronounced** |  `INPUT[textArea:pronounced]` |
>> **Aliases** | `INPUT[list:aliases]` |
>> **Ancestry** | `INPUT[Ancestry][suggester:ancestry]` |
>> **Heritage** | `INPUT[Heritage][suggester:heritage]` |
> **Creature Type** | `INPUT[textArea:ancestry]` |
> **Creature Sub-Type** | `INPUT[textArea:heritage]` |
>> **Gender** | `INPUT[Gender][suggester:gender]` |
>> **Age** | `INPUT[number:age]` |
>> **Alignment** | `INPUT[Alignment][suggester:alignment]` |
>
>> [!metadata|metadataoption]- NPC Info
>> #### NPC Info
>>  |
>>---|---|
>> **Languages** | `INPUT[Languages][inlineListSuggester:languages]` |
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"98 Templates"), useLinks(partial)):organizations]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"98 Templates"), useLinks(partial)):religions]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"98 Templates"), useLinks(partial)):ownedLocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"98 Templates"), useLinks(partial)):currentLocation]` |
>> **Condition** | `INPUT[Condition][:condition]` |
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery("50 Party"), useLinks(partial)):whichParty]` |
>> **Party 1 Relation** | `INPUT[party1Relation][inlineListSuggester:party1Relation]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ![[PlaceholderAudio.webm]]
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Ancestry** | `VIEW[{ancestry}]` |
> **Heritage** | `VIEW[{heritage}]` |
> **Gender** | `VIEW[{gender}]` |
> **Age** | `VIEW[{age}]`yrs |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Languages** | `VIEW[{languages}][text]` |
> **Occupation** | `VIEW[{occupation}][text]` |
> **Organizations** | `VIEW[{organizations}][link]` |
> **Religions** | `VIEW[{religions}][link]` |
> **Owned Locations** | `VIEW[{ownedLocation}][link]` |
> **Current Location** | `VIEW[{currentLocation}][link]` |
> **Condition** | `VIEW[{condition}]` |


# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|letters]- Letters
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|literature]- Literature
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Literature")
> SORT file.name ASC

## Overview



> [!column|2 no-title]
>
> 
>> [!metadata|ideals] Ideals
> `VIEW[{ideals}][text]`
>
>> [!metadata|flaws] Flaws
> `VIEW[{flaws}][text]`
> 
>> [!metadata|fear] Fears
> `VIEW[{fears}][text]`
>
>> [!metadata|mannerism] Mannerisms
> `VIEW[{mannerisms}][text]`

## Goals



## Acquaintances


## Current Events



## History



## Notes

**Physical Description:**  
Lette is stout and sturdy, with broad shoulders and arms that speak of years spent tending hearth and home. Her braided hair—her namesake—is a thick, intricate crown of copper and chestnut strands, woven with bits of wildflowers and worn bits of ribbon from the inn’s regulars. Her face is round and warmly flushed, with crow’s feet carved gently at the corners of her bright hazel eyes—eyes that sparkle like embers from the ever-burning hearth. A perpetual dusting of flour often smudges her apron, and her hands are calloused but nimble, accustomed to both stirring giant pots of stew and settling rowdy guests.

**Character Description:**  
Lette’s presence is as comforting as the inn she runs. She has a hearty laugh that fills the room like the scent of her famous stew—rich, warming, and impossible to ignore. She’s both motherly and no-nonsense, quick to silence foolishness but always ready to listen to a weary traveler’s tale. The Braided Ram is as much a home as a business, and Lette treats her guests with a mix of tough love and genuine care. Her knowledge of the town’s stories and secrets is vast, woven from years of quiet observation and countless late-night conversations over mugs of ale. Behind her cheerful demeanor lies a keen mind and an iron will, ensuring her inn remains a steadfast refuge amid the town’s ebb and flow.