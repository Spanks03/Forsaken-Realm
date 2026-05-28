---
tags:
  - Character
  - NPC
art: 99 Images/z_Assets/NPCs/JeforHellie.png
languages: Common
pronounced:
ancestry: Halfling
gender: Male
pronouns:
age: 31
sexuality:
alignment: Chaotic Good
occupation:
organizations:
ownedLocation:
  - "[[The Hollow Hearth Tavern]]"
currentLocation:
  - "[[Oar's Break]]"
  - "[[The Hollow Hearth Tavern]]"
condition:
aliases:
  - Tuck
heritage: Lightfoot
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
_Physical Description:_ Tuck Wren is a round-bellied halfling with a mop of curly chestnut hair that always seems just slightly out of place, giving him a perpetually windswept look. His cheeks are ruddy from years behind the hearth fire, and his hazel eyes crinkle at the edges from constant smiling. He dresses in rolled-up sleeves, patched waistcoats, and aprons stained with ale and stew. His hands are calloused from lugging barrels as much as from polishing tankards. A carved wooden pipe, worn smooth from years of use, is nearly always clenched between his teeth, even when unlit.

_Character:_ Tuck is the heart of the tavern and, in many ways, of Oar’s Break itself. Warm-voiced and quick with a story, he knows everyone’s name, drink, and business (whether they’ve told him or not). He has a talent for smoothing quarrels before they turn ugly, often sliding a mug or a plate across the bar at just the right moment. Though jovial and good-natured, he has a shrewd streak; years of listening have made him a keen judge of character. Tuck prefers to stay out of politics but is a well of local knowledge, making him invaluable to anyone passing through.