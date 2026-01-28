---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Lidia Riversong.jpg
aliases:
  - Livia Riversong
ancestry: Human
gender: Male
pronouns: She/Her
age: Mature Adult
sexuality: 
alignment: 
language:
  - Common
  - Elven
  - Dwarven
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
> Livia Riversong, in her late 40s, exudes an aura of quiet authority and wisdom that has earned her respect throughout the city of Ilayas. Her features bear the subtle marks of age, softened by a youthful vitality that belies her years of dedicated service to the city. Her most striking feature is her hair, intricately braided and shimmering with streaks of silver, a symbol of her maturity and experience.

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
With penetrating brown eyes that seem to miss nothing, Livia gazes out upon the world with a mixture of determination and thoughtfulness. Her attire is elegant yet understated, reflecting her pragmatic approach to politics and leadership, she carries herself with poise and grace, commanding attention wherever she goes.

As the right hand of the leading councillor, [[Lord Ealdred Corlas]], Livia plays a pivotal role in the governance of Ilayas, using her keen intellect and strategic insight to navigate the complex landscape of city politics. Though she does not hail from nobility, her tireless dedication to the welfare of the city has earned her the admiration and respect of both peers and constituents alike.

Behind her composed demeanor lies a fierce determination to uphold the values of justice and integrity that she holds dear. Whether negotiating with rival factions, resolving disputes, or championing causes close to her heart, Livia's unwavering commitment to the betterment of Ilayas marks her as a respected and influential figure in the city's political landscape.


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
### Responsibilities

**Scheduling and Coordination**

Livia manages Lord Corlas' schedule, coordinating meetings, briefings, and official functions. She ensures that the Chancellor's time is optimized for key responsibilities.

**Document Management**

Organizing and managing the influx of official documents, reports, and correspondence that pass through the Chancellor's office. Livia ensures that pertinent information reaches Lord Corlas in a timely manner.

**Communication Liaison**

Acting as a liaison between Lord Corlas and other council members, city officials, and external entities. Livia handles communications, relaying messages and gathering necessary information.

**Protocol and Etiquette**

Guiding Lord Corlas on matters of protocol and etiquette, especially during diplomatic engagements and formal events. Livia ensures that the Chancellor presents an appropriate image to dignitaries and guests.

**Research and Briefings**

Conducting research on various topics relevant to council discussions and providing concise briefings to Lord Corlas. Livia ensures that the Chancellor is well-informed and prepared for council meetings.

**Record-Keeping**

Maintaining meticulous records of council decisions, discussions, and action items. Livia ensures that a comprehensive archive is maintained for reference and historical purposes.

### Location

Lord Ealdred Corlas' official business is conducted from the Chancellor's Office in the [[Aetherian Hall]], a well-appointed space within the administrative wing of the city's central government building. The Chancellor's Office is designed to facilitate both formal meetings and private discussions. It boasts a strategic location, offering a commanding view of the city and providing an atmosphere conducive to focused decision-making.

Livia Riversong manages the day-to-day operations from her own adjoining office within the administrative wing. Her workspace is organized and efficient, with shelves of neatly labeled documents, a well-used desk, and a small table for private discussions with Lord Corlas. Together, Lord Ealdred Corlas and Livia Riversong form a formidable team, ensuring the effective governance of Ilayas.


## Notes





