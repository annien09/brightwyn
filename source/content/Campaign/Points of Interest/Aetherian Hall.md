---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/Ilayas Inner City art.webp
aliases:
  - Aetherian Hall
poitype:
  - Guildhall
dominion:
  - "[[Ilayas Council]]"
location:
  - "[[Ilayas]]"
  - "[[Teseon]]"
  - "[[Ilayas Inner City]]"
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
>> **Pronounced** |  `INPUT[textArea:pronounced]`
>> **Aliases** | `INPUT[list:aliases]` |
>> **Type** | `INPUT[POIType][inlineListSuggester:poitype]` |
>> **Dominion** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):dominion]` |
>> **Owners** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):owner]` |
>> **Assistant** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):assistant]` |
>> **Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{poitype}][text]` |
> **Dominion** | `VIEW[{dominion}][link]` |
> **Owners** | `VIEW[{owner}][link]` |
> **Assistant** | `VIEW[{assistant}][link]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>


> [!recite]+ Introduction
> The grand building where the Council of Ilayas convenes and conducts its official business is known as the Aetherian Hall.

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
> defaultZoom: 2
> zoomDelta: 0.5
> unit: meters
> scale: 1
> darkMode: false
> ```

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "POI")
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview 

### Exterior

The Aetherian Hall stands as a majestic testament to the fusion of magic and architectural grandeur. Its exterior, crafted from gleaming turqoise stone quarried from the Diamond mountains, is adorned with intricate carvings depicting scenes from Ilayas' history and the Empire of Teseon. The facade is embellished with enchanted symbols that shimmer softly in the sunlight, hinting at the magical essence within.

The main entrance is framed by towering pillars, each intricately carved with runes and motifs. Above the entrance arch, a magnificent transmutation enchantment displays dynamic scenes, transforming from the city's founding to its present-day splendor.

The building is crowned with a massive dome, where an ever-present magical aura creates a captivating display of lights during the night. Teseon's imperial crest, a symbol of unity, is proudly displayed at the apex of the dome.

Magical gardens surround the Aetherian Hall, featuring flora native to the region. Elaborate pathways lead to the entrance, guiding visitors through the enchanting landscape.

### Lobby

**Grand Entrance**: The lobby of the Aetherian Hall serves as a grand entrance to the council building. The space is adorned with intricate magical tapestries depicting key moments in the history of Ilayas and the Empire of Teseon.

**Monumental Statues**: Dominating the center of the circular room are life-sized statues paying tribute to "The Three," the highest-ranking leaders of the Empire of Teseon. The statues capture the essence of wisdom, strength, and diplomacy, representing the qualities that have guided the empire.

**Artistic Displays**: The lobby is adorned with paintings, murals, and sculptures that celebrate the cultural heritage of Ilayas. Scenes from historical events, portraits of influential figures, and magical displays contribute to the rich tapestry of the city's identity.

**Interactive Displays:** Enchanted displays provide visitors with interactive experiences powered by magic, offering information about the city's history, the council's role, and the accomplishments of the Empire of Teseon.

### Wings - West and East

**Councilors' Offices:** The wings on the west and east sides of the Aetherian Hall house the individual offices of each council member. Each office is uniquely decorated, reflecting the personal tastes and interests of the respective councilor.

**Conference Rooms:** Adjacent to the offices are conference rooms for private discussions and meetings. These rooms are equipped with magical communication devices, allowing councilors to confer with each other and external parties.

**Decorative Elements:** The corridors leading to the offices are adorned with elegant tapestries, sculptures, and enchanted artifacts. These decorative elements highlight the achievements of Ilayas and showcase the city's commitment to both art and magic.

**Staff Offices:** Additional offices are present to accommodate administrative staff, aides, and assistants who support the councilors in their daily tasks. These offices facilitate the efficient functioning of the council's administrative operations.

**Common Areas**: Shared spaces, such as lounges and meeting areas, are strategically placed to encourage informal discussions and collaboration among council members. These areas contribute to a sense of camaraderie within the Aetherian Hall.

The Aetherian Hall, with its impressive lobby and wings, not only serves as a hub for political discussions but also as a testament to the city's cultural richness and the collaborative spirit of its leaders. The layout is designed to foster an environment where the past, present, and future of Ilayas converge in a harmonious blend of art, history, and governance.

## Current Events


## History


## Notes

