---
tags:
  - Character
  - NPC
art: "[[PlaceholderNPC.png]]"
aliases:
ancestry:
heritage:
gender:
pronouns:
sexuality:
languages:
  - "[[Common]]"
occupation: []
organizations: []
religions: []
currentLocation:
condition:
whichParty: []
party1Relation:
fc-date:
  year: "[-*]"
birthday: -28
age: 836
---

> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> ```meta-bind
> INPUT[select(
> option(1, Tab 1),
> option(2, Tab 2),
> class(tabbed)
> )]
> ```
>
>> [!tabbed-box]
>> `VIEW[!{art}][text(renderMarkdown)]`
>>
>> ![[PlaceholderNPC.png]]
>
> ![[PlaceholderAudio.webm]]
>
> # Bio
> | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Ancestry** | `VIEW[{ancestry}][link]` |
> | **Heritage** | `VIEW[{heritage}][link]` |
> | **Gender** | `VIEW[{gender}]` |
> | **Pronouns** | `VIEW[{pronouns}]` |
> | **Sexuality** | `VIEW[{sexuality}]` |
> | **Age** | `VIEW[floor(({Vault Hub#time}-{birthday})/{Vault Hub#dpy})][:age]` yrs |
> 
> # Info
> | |
> |---|---|
> | **Languages** | `VIEW[{languages}][link]` |
> | **Occupations** | `VIEW[{occupation}][text]` |
> | **Organizations** | `VIEW[{organizations}][link]` |
> | **Religions** | `VIEW[{religions}][link]` |
> | **Condition** | `VIEW[{condition}]` |
> | **Current Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`

> *<font color="#7f7f7f">Summarize who this NPC is, highlighting their role, personality, and what makes them stand out in the story or world.</font>*

## Database
 
 ![[Database - NPC Note.base]]

## Overview

### Description:

> *<font color="#7f7f7f">Describe the NPC’s physical appearance, including build, features, clothing, and any distinctive marks or details.</font>*

### Personality & Mannerisms:

> *<font color="#7f7f7f">Describe the NPC’s personality and mannerisms, including their general demeanour, tone of voice, habits, and any quirks that define how they interact with others.</font>*

### Motivations:

> *<font color="#7f7f7f">Describe what drives this NPC, including their goals, desires, fears, or values that influence their choices and actions.</font>*

#### Goals:

- [ ] *<font color="#7f7f7f">Example Goal</font>*
    - *<font color="#7f7f7f">What is currently going on in their lives that are bothering them or they are trying to achieve?</font>*

## Present

### Current Events:

- [ ] *<font color="#7f7f7f">Example Event </font>*
    - *<font color="#7f7f7f">What is currently going on in their lives?</font>*

### Secrets:

- [ ] *<font color="#7f7f7f">Example Secret</font>*
    - *<font color="#7f7f7f">What are the details of this secret?</font>*

### Acquaintances:

- *<font color="#7f7f7f">Example Person | Relation</font>*
    - *<font color="#7f7f7f">How do they know this person and what is their relationship like?</font>*

## Past

### Birth:

**Day** `INPUT[inlineSelect(option(1), option(2), option(3), option(4), option(5), option(6), option(7), option(8), option(9), option(10), option(11), option(12), option(13), option(14), option(15), option(16), option(17), option(18), option(19), option(20), option(21), option(22), option(23), option(24), option(25), option(26), option(27), option(28)):fc-date.day]` **Month** `INPUT[inlineSelect(option(1, Aurora),option(2, Novus), option(3, Iter), option(4, Florera), option(5, Tersus), option(6, Solis), option(7, Calor), option(8, Caelum), option(9, Visus), option(10, Messis), option(11, Cedrus), option(12, Tornu), option(13, Parago)):fc-date.month]` **Year** `INPUT[number(class(nb-mb-55)):year]` `VIEW[\[{year}-*\]][text(hidden):fc-date.year]` `VIEW[{Vault Hub#dpy}*{year}+{Vault Hub#dpm}*({fc-date.month}-1)+{fc-date.day}][math(hidden):birthday]`

- Birth Location: 
- Mother: | Father: 

### History:

#### Example Event:

> *<font color="#7f7f7f">Describe an important event from this NPC's past, describe how it shaped who they are, such as a triumph, tragedy, or a turning point.</font>*

## Notes

