---
tags:
  - "#Location"
  - "#District"
art: z_Assets/Locations/The Wealthy District.webp
aliases:
  - Wealthy District
districttype:
  - Residential
  - Financial
  - Cultural
location:
  - "[[Ilayas]]"
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
> Bustling Prosperity: South of the Inner City lies the Wealthy District. Lavish townhouses, upscale boutiques, and exclusive arcane academies cater to the affluent citizens of Ilayas. The streets are alive with the vibrancy of commerce and enchantment. Alchemists, merchants, and renowned spellcasters can be found here, making it a hub of both business and scholarly activity.

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

## History
The Wealthy District, known as Gilded Heights, is an enclave of prosperity and luxury. Nestled between the Inner City and the Common District, Gilded Heights is characterized by elegant townhouses, upscale boutiques, and cultural venues. Cobblestone streets are lined with shops selling exquisite wares, and fashionable citizens move about in vibrant, enchanted carriages. The district is a blend of affluence and artistic expression, with enchanting street performances and live music enhancing the atmosphere. Gilded Heights exudes an air of sophistication, and its residents take pride in their refined tastes and influential connections.

## Notable Locations

**Artisan's Avenue:** A boulevard lined with high-end boutiques, art galleries, and exquisite craft shops.

**Golden Plaza**: A central square surrounded by upscale restaurants, cafes, and open-air markets.

**Elegant Mansions:** Lavish townhouses and mansions adorned with magical gardens and private courtyards.

**Cultural Palaces:** Theaters, concert halls, and opera houses that host prestigious cultural events.

**The Colosseum**


## Notes

