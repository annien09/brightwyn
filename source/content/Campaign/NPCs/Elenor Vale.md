---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/Misc/PlaceholderImage.png
quest:
  - "[[Strange Humming]]"
ancestry: Human
heritage: Half-Elf
gender: Female
pronouns: She/Her
age: Mature Adult
sexuality: 
alignment: 
language:
  - Common
  - Elven
  - Dwarven
occupation:
  - Diplomat
organization:
  - "[[Ilayas Council]]"
location:
  - "[[Aetherian Hall]]"
condition: Healthy
party1relation: Acquaintance
aliases:
  - Guild Ambassador
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
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Party 1 Relation** | `INPUT[Party1Relation][:party1relation]` |
>> **Quest** | `INPUT[inlineListSuggester(optionQuery(#Quest AND !"z_Templates"), useLinks(partial)):quest]` |

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
> Elenor Vale is a figure of elegant poise, a human with long, auburn hair cascading in gentle waves down her back. Her vibrant green eyes reflect a keen intellect and warmth. She wears a fine robe, signifying her role as an important figure among the guilds. Her stature exudes confidence and diplomacy, with a demeanor that blends approachability with authority

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
### Role and Responsibilities
As the appointed Ambassador of Guild-related Operations, Elenor Vale oversees the operations within the Guildhall. Her primary duties include facilitating collaboration between the various guilds, acting as a liaison between the council and guild representatives, and managing the issuance of quests or missions endorsed by the council.

#### Interview
Association
- Are you associated with any guild?
  
Background and Skills
- What expertise or skills do you possess that could aid in investigating mysterious phenomena?
- Have you encountered similar anomalies or investigated mysterious occurrences before?

Team Dynamics
- What roles do each of you usually take on during investigations or quests?

Approach to Investigations
- What methods or tools would you employ to trace the origin of the mysterious hum?
- How do you handle unexpected or dangerous situations during investigations?

Problem-Solving and Adaptability
- Can you provide an example of a challenging situation you've faced and how you resolved it?

Knowledge of the City and its Surroundings
- Have you interacted with any locals who might have information about these disappearances or the strange hum?

## History
### What we know

A low, incessant hum emerged on the 20th of Desnus, stirring whispers among the townsfolk. At first, it was dismissed as the wind whistling through the thickets or the echoes of some natural phenomenon. But as days passed, the hum grew in intensity and persistence, resonating like a haunting. Additionally, 1-2 days after the hum started, there have been disappearances in the outskirts of the City.

SEE [[Strange humming]] for more info.
## The Guild of Valiant Explorers

>[REDACTED]

### Duties

>[REDACTED]

### Hierarchy and Leadership

#### Guildmaster
>[REDACTED]

#### Captains 
>[REDACTED]

#### Members
>[REDACTED].

### Leadership and Governance
>[REDACTED]
## Notes





