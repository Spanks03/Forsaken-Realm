---
tags:
  - Party
art: Death's Door.png
partyID: 2
---

# `=this.file.name`

## Current Party

![[Database - Party Members.base]]

### Known Party Languages

~~~dataview
TABLE WITHOUT ID
  A as "Language",
  length(rows) as "Count",
  rows.file.link as "Spoken By"
FROM "51 Characters"
WHERE econtains(whichParty, this.file.link) AND languages
FLATTEN languages AS A
GROUP BY A
SORT length(rows) DESC
~~~

## Individual Relations

> [!metadata|info] Tip for Bag of Tips
> Due to the nature of parties changing their name after so many sessions after starting, for simplicity, we use the property of Party1, Party2, etc.
> Because of this, you will need to make a unique relations database for each new party.

## Story

![[Database - Story.base]]

## Notes

