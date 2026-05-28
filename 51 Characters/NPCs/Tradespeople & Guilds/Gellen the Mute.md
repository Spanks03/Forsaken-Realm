---
tags:
  - Character
  - NPC
art: 99 Images/Oar's Break Images/Pasted image 20250802132045.png
languages:
  - Common
  - Common Sign Language
pronounced:
ancestry: Orc
gender: Male
pronouns:
age: 29
sexuality:
alignment: Chaotic Good
occupation:
organizations:
ownedLocation:
currentLocation:
  - "[[Oar's Break]]"
  - "[[The Verdant Jar]]"
condition:
heritage: Eophoris
aliases:
  - Gellen
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
Male Orc – Woodcarver & Cigar Roller

**Physical Description:**  
A red-haired orc with a shock of thick curls brushed back and a pair of bushy mutton chops framing his jaw like twin fuses ready to spark. His eyes are a piercing steel-gray, always alert but never speaking. Heavy tattoos in a curling script—possibly an old dialect or personal code—span his knuckles, faded where the skin bends from years of precise carving. Always clad in a buttoned vest with rolled sleeves, a slim blade tucked at the hip, and a leather apron stained with wood dust and tobacco oil. His fingers are thick, but move with the grace of a pianist.

**Character Description:**  
Gellen hasn’t spoken in years, but everyone in Oar’s Break knows what he means. His silences are loud, his glances telling. He crafts small, intricate wooden birds that seem ready to fly, each one different, each with personality. When not carving, he’s drying tobacco leaves or rolling strong cigars, often shared in quiet barter. There’s a sharpness to him—a watchfulness that suggests he hears more than he lets on. No one knows why he went quiet, but few question it twice.