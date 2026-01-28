---
tags:
  - Organization
art: z_Assets/Locations/Ilayas Inner City art.webp
aliases:
  - Ilayas Council
organizationtype:
  - Council
head:
  - "[[Lord Ealdred Corlas]]"
hq: "[[Aetherian Hall]]"
location:
  - "[[Aetherian Hall]]"
  - "[[Ilayas]]"
  - "[[Ilayas Inner City]]"
steward:
  - "[[Livia Riversong]]"
  - "[[Eltane Gestal]]"
organization: []
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

> [!abstract]+
> The Council of Ilayas serves as the governing body of the illustrious city, overseeing its affairs with wisdom, prudence, and a dedication to the prosperity of its inhabitants. Comprised of esteemed individuals from diverse backgrounds, the council convenes regularly to deliberate on matters of governance, legislation, and the advancement of the city's interests.

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

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(organization, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview

Led by a leading councillor, the councilors bring a wealth of knowledge, experience, and expertise to their roles, representing various sectors of Ilayas's society. From esteemed magistrates to influential merchants, each councilor contributes a unique perspective and insight to the deliberations of the council, ensuring that decisions are made with the best interests of the city in mind.

As the primary legislative body of Ilayas, the council enacts laws, regulations, and policies that shape the city's governance and development. Through open debate, careful consideration, and consensus-building, the councilors strive to address the needs of the populace while upholding the principles of justice, fairness, and equality.

Beyond its legislative duties, the council also plays a crucial role in diplomacy, trade relations, and the maintenance of order and security within the city. Through collaboration with allied nations, trade guilds, and law enforcement agencies, the councilors work tirelessly to foster prosperity, stability, and harmony within the city and beyond.

In times of crisis or uncertainty, the councilors rise to the occasion, demonstrating leadership, resilience, and a steadfast commitment to the welfare of Ilayas and its citizens. Guided by the principles of integrity, accountability, and public service, the Council of Ilayas stands as a beacon of governance and leadership, guiding the city forward into a future of promise and opportunity.

## Councillors

### Lord Ealdred Corlas - Chancellor of Ilayas

Responsibility: Head of the council, overseeing the overall governance of the city. As the Chancellor, Lord Corlas ensures the coordination of various departments and serves as the primary advisor to the ruling nobility.

###  Lady Isolde Ravenshadow - Minister of Arcane Affairs

Responsibility: Manages magical and arcane matters within the city. Lady Ravenshadow oversees the magical institutions, regulation of magical trade, and the city's relations with magical entities and organizations.

###  Sir Percival Ironheart - Commander of the City Watch

Responsibility: Leads the city's law enforcement and defense. Sir Ironheart (dwarf) is responsible for maintaining order, ensuring the safety of the citizens, and coordinating efforts against external threats.

###  Lord Cedric Veridane - Minister of Commerce

Responsibility: Oversees trade, commerce, and economic policies. Lord veridane facilitates partnerships with merchants, regulates trade routes, and ensures the prosperity of Ilayas through economic initiatives.

###  Lord Teryn Stormwind - Master of Infrastructure

Responsibility: Manages city infrastructure, including construction, maintenance, and development projects. Lord Stormwind ensures the functionality and aesthetics of Ilayas' architecture.

###  Dame Elara Swiftbrook - Mistress of Culture and Arts 

Responsibility: Promotes and preserves the cultural heritage of Ilayas. Dame Swiftbrook (halfling) oversees artistic endeavors, cultural events, and the city's renowned festivals, fostering a vibrant cultural environment.

###  Ambassador Elenor Vale - Guild Representative

Responsibility: As the appointed Ambassador of Guild-related Operations, Elenor Vale oversees the operations within the Guildhall. Her primary duties include facilitating collaboration between the various guilds, acting as a liaison between the council and guild representatives, and managing the issuance of quests or missions endorsed by the council.

###  Lord Alistair Greycastle - Minister of Health and Well-being

Responsibility: Oversees matters related to public health, sanitation, and well-being. Lord Greycastle ensures access to healthcare, manages epidemics, and promotes a healthy living environment.

###  Duchess Leonora Emberwood - Protector of Wynsend Forest

Responsibility: Represents the interests of Wynsend Forest and its inhabitants. Duchess Emberwood ensures the preservation of the forest, manages interactions with forest communities, and addresses environmental concerns.

###  Sir Thaddeus Lightbringer - High Justiciar

Responsibility: Heads the judiciary system, ensuring the fair and just application of laws. Sir Lightbringer presides over high-profile legal cases, ensuring the integrity of the legal system.

### (Unofficial) Mistress Elandra Nightshade - Spymaster of the Veil

Responsibility: Represents the interests of the Veil of Shadows in the council. The Mistress of the Veil provides insight into clandestine affairs and ensures that the council is informed of potential threats from the shadows.

## Notes



