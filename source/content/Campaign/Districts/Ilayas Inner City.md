---
tags:
  - "#Location"
  - "#District"
art: z_Assets/Locations/Ilayas Inner City art.webp
pronounced: Inner City
aliases:
  - Ilayas Inner City
districttype:
  - Financial
  - Political
  - Educational
location:
  - "[[Ilayas]]"
  - "[[Aetherian Hall]]"
organization:
  - "[[Ilayas Council]]"
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
> **Type** | `INPUT[DistrictType][inlineListSuggester:districttype]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{districttype}][text]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!recite]+ Introduction
> Noble Elegance: The Inner City is the heart of Ilayas, comprising 15% of the city's area. This district is a sight to behold, with opulent mansions and grand estates housing the high nobility, but most importantly the political hub of the city. Towering spires, magical gardens, and cascading fountains decorate the streets. Here, the most powerful mages and influential families in Teseon reside, engaging in the highest echelons of magical studies and political intrigue.

> [!metadata|map]- Map
> ```leaflet
> id: TBD
> image: [[PlaceholderImage.png]]
> height: 600px
> width: 640px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 1
> zoomDelta: 0.5
> unit: meters
> scale: 1
> darkMode: false
> ```

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(location), ", ") AS "Location", join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "POI") AND  !contains(poitype, "Shop")
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|shops]- Shops
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(location), ", ") AS "Location", join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND (contains(tags, "POI") and contains(poitype, "Shop"))
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|organizations]- Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Organization")
> SORT tags DESC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview 

## History
The Inner City stands as the epicenter of power and privilege in Ilayas. Walled and opulent, it is a haven for the city's aristocracy and magical elite. The streets are paved with intricate patterns of cobblestones, and grandiose mansions rise like magical spires. The Inner City is a testament to the city's history, with ancient landmarks, towering mage academies, and the majestic Grand Citadel, where the ruling council convenes. The air is filled with the subtle scent of arcane incense, and the streets are patrolled by magically animated guardians. Lavish gardens, adorned with mystical sculptures and fountains, add to the enchantment of the Inner City.

### Notable Locations
**Aetherian Hall**: The seat of the ruling council, a massive structure with soaring towers and enchanted defenses.

**Aetherium Academy of Mystic Arts**: Home to prestigious mage academies and magical research institutions.

**Noble Gardens**: Lavish gardens where aristocrats gather for social events and diplomatic discussions.

**Council Square**: A central plaza surrounded by important government buildings and historical monuments.


## Notes

