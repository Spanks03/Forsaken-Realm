---
tags:
  - Character
  - Player
art: 99 Images/image Tilly.png
playedBy: MamaWitch
aliases:
  - Tilly
ancestry: Halfling
heritage: Lightfoot
gender: Female
pronouns:
languages:
  - Common
  - Halfling
  - Common Sign Language
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
age: 24
pronounced: TIL-ee MOON-bug
alignment: Chaotic Good
ideals: |
  Uplift Through Truth and Performance - Each melody, story, or witty comment is meant to help others see their truest selves. 

  Unshakable Vow- her friends and family will never be left behind, she would rather silence the stage than risk their well-being

  Motivated by a deep desire to grow and change—emotionally, spiritually, and magically—and she nudges others to do the same. 

  Connection Over Applause -The bond with her friends and the emotional impact of her art matters more than fame or perfection

  Curiosity and Wisdom- she treasures learning—not just from books, but from people, their hearts, and their journeys
flaws: |-
  Overperforms When Nervous

  In tense situations, she might default to performance—songs, quips, dances—to mask fear or uncertainty.

  Can’t Sit Still

  Her constant movement, fidgeting, and habit of climbing furniture when bored can come across as chaotic, immature, or even disrespectful in more formal or serious situations

  Not Knowing When to Stop Performing

  Even though she believes in knowing when to stop the show… sometimes she doesn’t. She overextends, overstimulates, or keeps the mask on a little too long

  As a bard, her emotions can channel through her performances. When upset or overwhelmed, her spells might reflect her inner turmoil
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
> | **Pronouns** | `VIEW[{pronouns}]` |
> | **Sexuality** | `VIEW[{sexuality}]` |
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

