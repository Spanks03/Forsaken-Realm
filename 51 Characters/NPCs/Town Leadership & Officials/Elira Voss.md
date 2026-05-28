---
tags:
  - Character
  - NPC
art: 99 Images/Oar's Break Images/Pasted image 20250727144825.png
languages: Common
pronounced:
ancestry:
gender:
pronouns:
age:
sexuality:
alignment:
occupation:
organizations:
ownedLocation:
  - "[[Oar's Break]]"
currentLocation:
  - "[[Oar's Break]]"
  - "[[Greystone Manor]]"
condition:
aliases:
  - Mayor Voss
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
Mayor Elira Voss is a tall, lean figure with silver-threaded hair pulled into a modest braid. Their features are sharply defined but never severe — high cheekbones, a smooth brow, and eyes the color of storm-washed stone. They dress with quiet precision: tailored but simple robes in natural hues, often accompanied by a pin bearing the town’s crest. They are most often seen seated at a plain oak desk beside a garden-facing window, quill in hand, back straight, every movement calm and deliberate.

**Character Description:**  
Elira Voss governs without bluster or ego. They speak sparingly, but when they do, people fall silent — not out of fear, but because their words carry the weight of wisdom and earned respect. Voss is a listener first, a decision-maker second. Conflicts brought before them are met with steady logic and a clarity that cuts through noise. Even when saying no, Voss has a way of making people feel heard. To the people of Oar’s Break, they are not a ruler but a steward — the one who keeps the waters still, the gates secure, and the rhythm of life unbroken.

Though often stoic, there are rare moments — often in the garden, watching bees meander through basil — when a soft smile touches their face. In those fleeting seconds, it feels like the whole town exhales.