---
tags:
  - Character
  - Player
art: 99 Images/openart-7e58df2fde8e4137825ea263e65297b8_raw.jpg
playedBy: Red
aliases:
  - Selene
ancestry: Aasimar
heritage: Protector
gender: Female
pronouns:
languages:
  - Common
  - Celestial
occupation: []
organizations: []
religions: []
condition:
currentLocation: []
whichParty:
  - "[[Party 1 - TBD|Party 1 - TBD]]"
fc-date:
  year: "[-*]"
birthday: -28
year:
age: 54
pronounced: sih-LEE-nee aw-REH-lee-ohs
alignment: Lawful Good
ideals: |-
  Balance. “Light without shadow blinds. Shadow without light devours. I am the bridge between them.”

  Duty. “If I was chosen for this path, then I will walk it—even if I must walk it alone.”
flaws: |-
  1. Growing up in a celestial realm with serene detachment and cosmic perspectives, Selene sometimes finds it difficult to connect deeply with mortal emotions. She empathizes, but can come across as emotionally distant or unrelatable. She might offer logical or philosophical comfort when someone just wants a hug… or vengeance. 

  2. She puts the needs of others first to a fault—willing to endure exhaustion, injury, or emotional strain if it means others are safe. She often believes that pain is simply her burden to bear. She may refuse healing for herself, or protect others even when tactically unwise.
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
>> **Played By** |  `INPUT[textArea:playedBy]` |
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
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery("49 Organizations"), useLinks(partial)):organizations]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(Organization AND !"98 Templates"), useLinks(partial)):religions]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(Location AND !"98 Templates"), useLinks(partial)):ownedLocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(Location AND !"98 Templates"), useLinks(partial)):currentLocation]` |
>> **Condition** | `INPUT[Condition][inlineListSuggester:condition]` |
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery("50 Party")):whichParty]` |
>> **Party 1 Relation** | `INPUT[party1Relation][inlineListSuggester:party1Relation]` |



> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> 
> ###### **Played By:** <font color="#ffc000">`VIEW[{playedBy}][text]`</font>
> 
> # Bio
> | | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Ancestry** | `VIEW[{ancestry}][link]` |
> | **Heritage** | `VIEW[{heritage}][link]` |
> | **Gender** | `VIEW[{gender}]` |
> | **Age** | `VIEW[{age}]` yrs |
> 
> # Details
> | | |
> |---|---|
> | **Languages** | `VIEW[{languages}][link]` |
> | **Occupations** | `VIEW[{occupation}][text]` |
> | **Organizations** | `VIEW[{organizations}][link]` |
> | **Religions** | `VIEW[{religions}][link]` |
> | **Condition** | `VIEW[{condition}]` |
> | **Current Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`

## Database
 ![[Database - Player Note.base]]

## Ideals
> [!column|2 no-title]
>
> 
>> [!metadata|ideals] Ideals
> *<font color="#7f7f7f">`VIEW[{ideals}][text]`</font>*
>
>> [!metadata|flaws] Flaws
> *<font color="#7f7f7f">`VIEW[{flaws}][text]`</font>*
> 
>> [!metadata|fear] Fears
> *<font color="#7f7f7f">`VIEW[{fears}][text]`</font>*
>
>> [!metadata|mannerism] Mannerisms
> *<font color="#7f7f7f">`VIEW[{mannerisms}][text]`</font>*
## Present

### Goals

#### Short-Term:



#### Long-Term:



## Past
### Birth:

**Day** `INPUT[inlineSelect(option(1), option(2), option(3), option(4), option(5), option(6), option(7), option(8), option(9), option(10), option(11), option(12), option(13), option(14), option(15), option(16), option(17), option(18), option(19), option(20), option(21), option(22), option(23), option(24), option(25), option(26), option(27), option(28), option(29), option(30), option(31), option(32), option(33), option(34), option(35), option(36), option(37), option(38), option(39), option(40)):fc-date.day]` **Month** `INPUT[inlineSelect(option(1, Month of a New Light),option(2, Month of Eaos), option(3, Month of Truth), option(4, Month of Qhathos), option(5, Month of Temp), option(6, Month of Vimnera), option(7, Month of Prosper), option(8, Month of Datarr), option(9, Month of Yearn), option(10, Month of Final Light)):fc-date.month]` **Year** `INPUT[number(class(nb-mb-55)):year]` `VIEW[\[{year}-*\]][text(hidden):fc-date.year]` `VIEW[{Vault Hub#dpy}*{year}+{Vault Hub#dpm}*({fc-date.month}-1)+{fc-date.day}][math(hidden):birthday]`
- Birth Location: 
- Mother: | Father: 



### Childhood:



### Journey:



### Worship:



## Notes

[Player Handout](https://docs.google.com/document/d/1_eFTuK3teRJSAVbd2QSZxjDTgE_RZH54zZg-3Eoo4Hk/edit?usp=sharing)

