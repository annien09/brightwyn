---
tags:
  - Organization
art: z_Assets/Locations/Jade Gate Logo.png
aliases:
  - Jade Gate
organizationtype:
  - Syndicate
head:
  - "[[The Gatekeeper]]"
hq: "[[Teseon]]"
location:
  - "[[Ilayas]]"
  - "[[Teseon]]"
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
- [ ] The Jade Gate is a clandestine and highly sophisticated criminal syndicate that operates on a global scale. Known for their ruthless efficiency and expertise in smuggling contraband, they have gained a notorious reputation within criminal circles and law enforcement agencies alike.

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


### Hierarchy and Structure

- [ ] The organization is structured in a hierarchical manner, with a tight-knit group of leaders at the top, overseeing various divisions and operations. At the helm is a mysterious figure, known only as the "Gravedigger," who remains elusive and shrouded in secrecy. Beneath the Gravedigger are trusted lieutenants who manage different aspects of the organization, such as procurement, transportation, distribution, and security. The Gatekeeper is one of the lieutenants acting in Teseon.

### Activities and Smuggling Operations

- [ ] The Jade Gate specializes in smuggling a wide array of illicit goods, including drugs, weapons, counterfeit currency, stolen artifacts, and even human trafficking. They have developed an intricate network of contacts and connections, allowing them to operate across borders and exploit vulnerabilities in various nations. Their operations range from smuggling goods via land, sea, and air to utilizing underground tunnels, hidden compartments, and sophisticated concealment techniques.

### Infrastructure and Resources

- [ ] The organization boasts a vast infrastructure that enables their illegal activities. They possess safe houses, warehouses, and storage facilities strategically located in various regions, serving as operational hubs and secure storage for their illicit merchandise. The Jade Gate also maintains a fleet of customized vehicles, sea and skyships.

### Secrecy and Protection

- [ ] The Jade Gate takes extreme measures to protect its members and maintain secrecy. They utilize communication through magic means, coded language, and aliases to communicate and conduct business. The organization employs a network of skilled operatives proficient in combat, surveillance, and counterintelligence to safeguard their operations and eliminate potential threats.


## Player Info: Society DC  20

I'll tell you what I told Gwyn, that Gatekeeper individual is part of a smuggling organization known as the Jade Gate.

- [x] The Jade Gate is a highly sophisticated criminal syndicate that operates on a global scale. They are known for their ruthless efficiency and expertise in smuggling contraband, and have gained a notorious reputation within criminal circles and law enforcement agencies alike. The Jade Gate specializes in smuggling a wide array of illicit goods, including drugs, weapons, counterfeit currency, stolen artifacts, and even human trafficking. They are powerful, have a vast infrastructure and global reach.

- [x] Not much is known about their inner dealings though. Supposedly their leader goes by the Gravedigger, and has lieutenants under them, the Gatekeeper being one of the lieutenants acting in Teseon. They use magic to disguise their appearances and voices so it's difficult to learn much about their identities.


## Improck

Agents have also been keeping an eye on Improck from afar through contacts with local bookseller Voz Lirayne.

>[REDACTED]
>
## The Vessels

### Known Vessels 
1. **Sloth (Vessel for Jubilex) - Harlow the Uninspired**:
	(Quote) The Gatekeeper: *"The bard known as Harlow the Uninspired may hold the key to Jubilex's vessel."*
	- Description: Unknown 
    - Location: Unknown
    
2. **Wrath (Vessel for Orcus) - Krel**:
    
    - Description: Krel is a half-elven spellcaster, brother to [[Aelwynn Ianven]] and Vessel of Orcus.
    - Location: Unknown
3. **Lust - "The Lady"**:
    - Description: Unknown
    - Location: Unknown
  
### Undiscovered Vessels 
>[REDACTED]

## Notes



