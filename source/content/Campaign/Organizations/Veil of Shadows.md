---
tags:
  - Organization
art: z_Assets/Misc/veil of shadows logo.jpg
pronounced: ""
aliases:
  - Veil of Shadows
organizationtype:
  - Faith
hq: "[[Ilayas]]"
location:
  - "[[Ilayas]]"
  - "[[Teseon]]"
  - "[[The Port District]]"
head:
  - "[[Elandra Nightshade]]"
worship:
  - "[[Calistria]]"
---

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Type** | `INPUT[OrganizationType][inlineListSuggester:organizationtype]` |
> **Hierarchy** | `INPUT[Null][suggester(optionQuery("Campaign/Organizations/Hierarchies"), useLinks(partial)):hierarchy]` | 
> **Head** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):head]` |
> **Steward** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):steward]` |
> **Parent Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Worship** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):worship]` |
> **HQ** | `INPUT[Null][suggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):hq]` |
> **Operating Areas** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> ###### `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>>  |
>> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{organizationtype}][text]` |
> **Hierarchy** | `VIEW[{hierarchy}][link]` |
> **Head** | `VIEW[{head}][link]` |
> **Steward** | `VIEW[{steward}][link]` |
> **Parent Organization** | `VIEW[{organization}][link]` |
> **Worship** | `VIEW[{worship}][link]` |
> **HQ** | `VIEW[{hq}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!recite]+ Introduction
> 

> [!metadata|geography]- Geography
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Geography") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Settlement") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|district]- Districts
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "District") AND econtains(organization, this.file.link)
> SORT districttype ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE contains(tags, "POI") AND econtains(organization, this.file.link)
> SORT poitype ASC, file.name ASC

> [!metadata|organizations]- Child Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "Organization") AND econtains(organization, this.file.link)
> SORT organizationtype ASC, file.name ASC

> [!metadata|letters]- Letters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(organization, this.file.link) AND contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(organization, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview

The Veil of Shadows stands as a covert sect within the Church of Calistria, embodying the clandestine and enigmatic aspects of the goddess's worship. Rooted in the lore and teachings of Calistria, the Veil of Shadows operates in the shadows, weaving webs of intrigue and manipulation to further the divine agenda of their deity. With a focus on espionage, secrets, and the pursuit of revenge, the Veil of Shadows serves as the clandestine arm of Calistria's faithful, navigating the intricate web of politics, intrigue, and deception that permeates the world.

## Culture

The culture of the Veil of Shadows is deeply intertwined with the teachings and ethos of Calistria. Members of the sect embrace the tenets of cunning, vengeance, and liberation, channeling their devotion to the goddess into clandestine operations and covert maneuvers. They operate with a sense of autonomy and individuality, guided by their own interpretations of Calistria's teachings and the pursuit of their divine mission.

## Modus Operandi 
The Veil of Shadows operates with precision and subtlety, leveraging their skills in espionage, subterfuge, and manipulation to achieve their objectives. They excel in gathering intelligence, conducting covert operations, and wielding secrets as weapons in the pursuit of divine justice. Through clandestine meetings, covert communications, and subtle manipulation, members of the Veil of Shadows navigate the intricate tapestry of intrigue that surrounds them, ever vigilant for opportunities to advance the divine agenda of Calistria.

## Acquaintances



## Current Events

The party has met the The Mistress of Revels [[Elandra Nightshade]] at [[The Red Door]] and hired the services of [[Veil of Shadows]].

The party has seen [[Elandra Nightshade]] at [[The Veridane Ball]] as a guest.


## Notes
The party has received [[Veil of Shadows Report]].