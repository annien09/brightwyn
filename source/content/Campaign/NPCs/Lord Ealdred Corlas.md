---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Ealdred Corlas.jpg
pronounced: El-dread
aliases:
  - Ealdred Corlas
ancestry: Human
gender: Male
pronouns: He/Him
age: Mature Adult
sexuality: 
alignment: 
language:
  - Common
  - Dwarven
  - Elven
  - Halfling
occupation:
  - Diplomat
organization:
  - "[[Ilayas Council]]"
location:
  - "[[Aetherian Hall]]"
  - "[[Ilayas]]"
  - "[[Ilayas Inner City]]"
condition: Healthy
party1relation: Unmet
quest:
  - "[[The Veridane Ball]]"
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
>> **Gender** | `INPUT[Gender][:gender]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]` |
>> **Age** | `INPUT[Age][:age]` |
>> **Sexuality** | `INPUT[Sexuality][:sexuality]` |
>> **Alignment** | `INPUT[Alignment][:alignment]` |
>
>> [!metadata|metadataoption]- NPC Info
>> #### NPC Info
>>  |
>>---|---|
>> **Languages** | `INPUT[Language][inlineListSuggester:language]` |
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):religion]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):ownedlocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>> **Condition** | `INPUT[Condition][:condition]` |
>> **Quest** | `INPUT[inlineListSuggester(optionQuery(#Quest AND !"z_Templates"), useLinks(partial)):quest]` |
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Party 1 Relation** | `INPUT[Party1Relation][:party1relation]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Ancestry** | `VIEW[{ancestry}]` |
> **Heritage** | `VIEW[{heritage}]` |
> **Gender** | `VIEW[{gender}]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Age** | `VIEW[{age}]` |
> **Sexuality** | `VIEW[{sexuality}]` |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Languages** | `VIEW[{language}][text]` |
> **Occupations** | `VIEW[{occupation}][text]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |
> **Quest** | `VIEW[{quest}][link]` |


# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>
> [!recite]+ Introduction
> Lord Ealdred Corlas cuts a distinguished figure, standing at a height that commands attention. His well-groomed salt-and-pepper hair frames a face adorned with the subtle lines of wisdom and experience. Ealdred's piercing blue eyes, often described as windows to a strategic mind, reflect a deep understanding of the intricacies of governance. Despite the weight of his responsibilities, he carries himself with a regal grace that befits his station.

> [!metadata|quest]- Quests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(status, ", ") AS Status
> FROM "Campaign"
> WHERE econtains(NPC, this.file.link) AND contains(tags, "Quest")
> SORT tags DESC, file.name ASC

> [!metadata|letters]- Letters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|literature]- Literature
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Literature")
> SORT file.name ASC

## Overview
**Attire**

Ealdred Corlas's attire is a reflection of his position as Chancellor. He is often seen donning elaborate robes adorned with symbols of Ilayas and Teseon, showcasing the unity between the city and the empire. A carefully crafted medallion, bearing the crest of the Chancellor's office, hangs from a chain around his neck. Ealdred's wardrobe seamlessly blends traditional elegance with subtle magical enhancements, underscoring the fusion of tradition and modernity within Ilayas.

**Demeanor**

A man of measured words and decisive actions, Lord Ealdred Corlas exudes an air of authority that naturally commands respect. His demeanor is characterized by a calm and collected composure, even in the face of challenges. Ealdred possesses a keen sense of diplomacy, skillfully navigating the intricate web of political relationships both within the council and beyond.


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

## About
### Background

Ealdred Corlas hails from a long line of distinguished nobility, with a family history deeply intertwined with the governance of Ilayas. His upbringing in the noble circles of Teseon instilled in him a sense of duty and a commitment to the welfare of his city. Ealdred's journey through the ranks of Teseon's political landscape, coupled with his strategic acumen, led him to the esteemed position of Chancellor.

### Leadership Style

As Chancellor, Lord Ealdred Corlas is known for his inclusive leadership style. He values input from each council member, fostering an environment where diverse perspectives are considered in decision-making. Ealdred is a pragmatist, seeking solutions that benefit both the noble houses and the common citizens of Ilayas. His commitment to the unity of Teseon and the prosperity of Ilayas is unwavering.

### Magical Prowess

While not a mage himself, Ealdred Corlas possesses a respectable understanding of magical principles. His collaboration with magical advisors and aides, such as Livia Riversong and Eltane Gestal, ensures that the magical aspects of governance are well-managed. Ealdred views magic as a valuable tool for progress, diplomacy, and the preservation of Ilayas' cultural heritage.


## History

## Veridane Ball
As the Lord Minister of Ilayas and leader of the Council, Ealdred Corlas is one of the most influential political figures present at the Veridane Ball. 



