---
tags:
  - Party
art: "[[Party 1 image.png]]"
partyID: 1
fc-date:
  year: "[-*]"
birthday: -28
---

# `=this.file.name`

## Current Party

![[Database - Party Members.base]]

### Known Party Languages

~~~dataview
TABLE WITHOUT ID
  A as "Language",
  rows.file.link as "Known By"
WHERE contains(whichParty, this.file.link) AND contains(tag, Character)
FLATTEN languages AS A
GROUP BY A
SORT length(rows) DESC
~~~


## Individual Relations

![[Database - Party 1 Relations.base]]

## Story

![[Database - Story.base]]

## Notes

