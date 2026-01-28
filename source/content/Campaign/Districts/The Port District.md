---
tags:
  - "#Location"
  - "#District"
art: z_Assets/Locations/The Port District.webp
aliases:
  - Port District
districttype:
  - Entertainment
  - Industrial
organization:
  - "[[Veil of Shadows]]"
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
> Located to the north, the Port District is Ilayas' connection to the world beyond. A bustling harbor serves as a vital trade route for Teseon, where enchanted ships bring goods from distant lands. Warehouses, inns, and mystical seafaring guilds cater to both sailors and merchants. It's a place of constant movement, as travelers arrive with exotic tales and rare magical artifacts.

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
The Port District, known as Maritime Enclave, is a vibrant and bustling hub of trade, maritime activities, and cultural exchange. The district is located along the shores of Tamlem Lake, and its landscape is dominated by docks, piers, and warehouses. The air is infused with the scent of saltwater and the calls of seagulls. Maritime Enclave is a melting pot of cultures, with merchants, sailors, and adventurers from distant lands converging to trade exotic goods and share tales of their travels. The district is a testament to the city's connection to the wider world and the wealth that flows through its port.

## Notable Locations
**Dockside Market**: An expansive market where merchants from distant lands offer exotic goods, spices, and magical artifacts.

**Shipwright's Quarters**: The area where skilled shipbuilders and repair crews work on vessels of various sizes.

**Captain's Square:** A meeting point for ship captains and navigators to exchange information and plan voyages.

**The Pier:** Crucial navigating hub connecting the city to the wider world. 

## The Pier
As characters make their way to the Port District of Ilayas, they come upon the bustling and picturesque Ilayas Pier, a vibrant and crucial hub connecting the city to the wider world. The pier offers a unique blend of commerce, leisure, and enchantment. Here's a vivid description:

### Overview

The Ilayas Pier stretches out into the sparkling waters of Tamlem Lake, providing an exquisite view of the tranquil lake and the sprawling Wynsend Forest beyond. It's a place where the magical heart of the city meets the natural beauty of the region. The pier is designed to accommodate both business and pleasure, making it a versatile space. It is run by [[Harbourmaster Alaric Stormwind]]

### Magical Lamps and Enchanted Lanterns

The pier is illuminated by an array of magical lamps and lanterns that line its edges. They cast a soft, iridescent glow that shimmers on the water's surface. The lanterns are enchanted to change colors periodically, creating an entrancing display of light.

### Whimsical Arcades

Covered arcades run along the length of the pier, providing shade and shelter from inclement weather. These arcades are adorned with intricate carvings and frescoes of maritime scenes and legendary sea creatures. Seating areas with comfortable benches and small, round tables offer visitors a place to relax and enjoy the view.

### Lively Street Performers

Street performers and buskers are a common sight on the pier. Magicians, jugglers, and musicians entertain the crowd with their enchanting acts. Their performances often include breathtaking displays of elemental magic, adding to the atmosphere of wonder.

### Local Seafood Eateries

The pier is dotted with seafood eateries, offering delectable dishes created from the day's fresh catches. Visitors can savor the flavors of Tamlem Lake, enjoying grilled fish, shrimp scampi, and a variety of locally inspired seafood cuisine.

## Notes

