---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Eltane Gestal.webp
pronounced: El-thane
ancestry: Human
gender: Male
pronouns: He/Him
age: Adult
sexuality: 
alignment: 
language:
  - Common
  - Draconic
  - Elven
  - Halfling
  - Celestial
occupation:
  - Scribe
organization:
  - "[[Ilayas Council]]"
location:
  - "[[Aetherian Hall]]"
  - "[[Ilayas]]"
  - "[[Ilayas Inner City]]"
condition: Healthy
party1relation: Unmet
quest:
  - "[[Looking for Eltane Gestal]]"
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
> Eltane Gestal, a young man in his mid-twenties, possesses a keen intellect and a boundless enthusiasm for the arcane arts. Born and raised in the bustling city of [[Ilayas]], Eltane's journey led him to the prestigious halls of the [[Arcanamirium]], where he aspired to become a master of magic.

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

## Aspirations
Eltane Gestal is a relatively young man, born and raised in [[Ilayas]]. His passion for magic from an early age and being born in an upper class family led him to be accepted to pursue magical studies at the [[Arcanamirium]] the largest and oldest magical school in Inazzur's Hold, and quite possibly the most prestigious arcane magic academy in the entire continent of Ailira. Despite his initial aspirations, Eltane faced challenges on his magical path and could not progress beyond the rank of acolyte.

Now serving as the diligent assistant to [[Livia Riversong]], a prominent figure in Ilayas, Eltane's passion for magic endures, manifested in his voracious appetite for knowledge and his personal collection of arcane tomes. With a noble bearing and a gentle demeanor, Eltane exudes an air of quiet determination and unwavering curiosity, ever eager to unlock the secrets of the arcane and contribute to the enchanting tapestry of magic that weaves through the city.

### Transition to Scribing

Undeterred by setbacks, Eltane returned to Ilayas with a wealth of magical knowledge. Drawing on his background as an acolyte, he found a new calling as a scribe, utilizing his understanding of magical principles to excel in his newfound role.

## Responsibilities as Livia Riversong's Assistant

### Magical Correspondence

Eltane handles magical correspondence, ensuring that enchanted messages and scrolls are properly cataloged and delivered. His familiarity with magical writings proves invaluable in deciphering intricate spells and symbols.

### Archiving Magical Records

Managing the magical section of Lord Ealdred Corlas' records, Eltane organizes and maintains a comprehensive archive of magical documents, reports, and historical texts.

### Research Assistance

Assisting Livia Riversong in researching magical topics relevant to council discussions. Eltane's personal enthusiasm for magic allows him to delve into esoteric subjects, providing valuable insights for decision-making.

### Personal Enthusiasm for Magic

Eltane's passion for magic extends beyond his professional duties. As a scion of an upper-class family, he has amassed a personal collection of magical books, artifacts, and curiosities. His private library showcases a diverse range of magical disciplines, from elemental conjurations to ancient enchantments.

### Workspace

Eltane's workspace is a blend of functionality and magical ambiance. Adorned with symbols of his acolyte status and shelves filled with his magical book collection, Eltane's corner in the administrative wing exudes an air of intellectual curiosity and dedication to the arcane arts.


## Acquaintances
Eltane Gestal's family, while belonging to the upper echelons of society, is not among the esteemed noble houses that dominate the political landscape of Ilayas. Instead, they are known for their contributions to the city's economic and cultural spheres, holding a respected position within the upper class.

#### Background and Lineage
The Gestal family has a lineage steeped in Ilayas' mercantile history. For generations, they have been prominent figures in the city's economic landscape, having established successful businesses and enterprises. Their wealth has been amassed through astute business acumen, investments in trade, and patronage of the arts.

#### Eltane's Upbringing
Growing up in this environment exposed Eltane to a blend of economic prowess and appreciation for cultural endeavors. His family's emphasis on education and the arts nurtured his love for magic and knowledge, leading him to pursue studies at the prestigious Arcanamirium, albeit without achieving the desired rank.



### Family
>[REDACTED]

## History



## Notes





