---
tags:
  - Character
  - NPC
  - Deity
art: 99 Images/PlaceholderDeity.png
aliases:
pronouns:
deityPower:
languages:
  - "[[Common]]"
organizations: []
currentLocation: []
condition:
whichParty: []
party1Relation:
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
>> **Aliases** | `INPUT[list:aliases]` |
>> **Pantheon Height** | `INPUT[Pantheon][inlineListSuggester:PantheonHeight]` |
>> **Domain** | `INPUT[textArea:domain]` |
>> **Parents** | `INPUT[list:parents]`
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
>> **Languages** | `INPUT[Languages][inlineListSuggester:languages]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"98 Templates"), useLinks(partial)):organizations]` |
>> **Condition** | `INPUT[Condition][inlineListSuggester:condition]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"98 Templates"), useLinks(partial)):currentLocation]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ![[PlaceholderAudio.webm]]
> 
> # Bio
> | |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Pantheon Height** | `VIEW[{PantheonHeight}][text]`
> | **Domain** | `VIEW[{domain}][text]` |
> | **Parents** | `VIEW[{parents}][link]`
> 
> # Info
> | |
> |---|---|
> | **Languages** | `VIEW[{languages}][link]` |
> | **Organizations** | `VIEW[{organizations}][link]` |
> | **Condition** | `VIEW[{condition}]` |
> | **Current Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`

> *<font color="#7f7f7f">Summarize who this Deity is, highlighting their role, personality, and what makes them stand out in the story or world.</font>*

## Database

![[Database - Deity Note.base]]

## Overview

### Description:

> *<font color="#7f7f7f">Describe the Deity’s physical appearance, including build, features, clothing, and any distinctive marks or details.</font>*

### Personality & Mannerisms:

> *<font color="#7f7f7f">Describe the Deity’s personality and mannerisms, including their general demeanour, tone of voice, habits, and any quirks that define how they interact with others.</font>*

### Motivations:

> *<font color="#7f7f7f">Describe what drives this Deity, including their goals, desires, fears, or values that influence their choices and actions.</font>*

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

## Present

### History:

#### Example Event:

> *<font color="#7f7f7f">Describe an important event from this Deity's past, describe how it shaped who they are, such as a triumph, tragedy, or a turning point.</font>

## Notes

