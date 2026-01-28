---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/Sanctum of the Final Veil.webp
pronounced: Final Veil
aliases:
  - Final Veil
poitype:
  - Temple
owner:
  - "[[Arioneth Duskwhisper]]"
assistant:
  - "[[Acolyte Tharion Shane]]"
organization:
  - "[[Sanctum of the Final Veil (Org)]]"
location:
  - "[[The Common District]]"
  - "[[Teseon]]"
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
> This temple is devoted to [[Pharasma]], the Lady of Graves. Its eastern facade displaces an intricate stained-glass mural depicting a stern Pharasma judging a darkly clad noble. Crows roost in murders on the high roofs of the temple, their beady eyes watching you with fascination. Scattered about the grounds and inside the temple are numerous acolytes in study or attending the maintenance of the temple.

> [!metadata|map]- Map
> ```leaflet
> id: Final_Veil
> image: [[Pharasma Temple Night.png]]
> height: 600px
> width: 900px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 2.5
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

## History
Built with a fusion of dark granite and silver accents, the Sanctum of the Final Veil is a beacon of quiet sophistication. It features arched doorways and stained glass windows depicting scenes of the Boneyard. The temple's exterior is adorned with intricate engravings depicting cycles of life and death. Inside, the temple is a symphony of arches, domes, and stained glass, creating an atmosphere that's both reverent and comforting.

## Notable Locations
### 1. Altar of Pharasman Judgment

At the heart of the temple lies the Altar of Pharasman Judgment. A massive stone structure, it features a delicate balance of scales representing the impartiality of Pharasma. Devotees place tokens or symbols of their departed loved ones here, seeking the Lady of Graves' guidance for the souls' journey.

### 2. Hall of Whispers

This sacred hall is adorned with tapestries depicting significant events in the history of the temple and the wider world. Here, priests and priestesses conduct private consultations, offering divinations and guidance to those seeking insights into their destinies.

### 3. Hall of the Final Veil

This solemn hall is where funeral ceremonies take place. The chamber is adorned with veils that gently sway in an ethereal breeze, and mourners gather to pay their respects. Clerics perform rites, offering prayers and soothing words to comfort grieving hearts, and guide departed souls to the River of Souls which takes them to Pharasma's Boneyard (a neutral plane where the souls of dead mortals from the Material Plane are judged by the goddess Pharasma.)

### 4. Garden of Whispering Leaves

Surrounding the temple is the Garden of Whispering Leaves, a tranquil oasis in the heart of the city. The soft rustle of leaves provides a backdrop to outdoor funeral ceremonies and quiet contemplation. Gravestones are elegantly arranged amid carefully tended flora.

### 5. Crypts of Veilstead

Beneath the temple are the Crypts of Veilstead, where influential city figures and devout worshippers are laid to rest. The crypts are accessible to the public during designated times, fostering a sense of community and shared remembrance.

### 6. Watchtower of Celestial Vigilance

A watchtower overlooks the city, where acolytes study the skies and maintain a celestial calendar. This allows for precise timing of funeral rites and a deeper understanding of the Lady of Graves' divine plan as it unfolds within the city.

### Ebon Fields (cemetery map)

The Ebon Fields is the actual graveyard, a harmonious blend of nature and memorial, adorned with weeping willows, marble benches, and pathways that wind through the grounds. Headstones are elegantly arranged in family plots, and well-tended flower beds add splashes of color to the otherwise muted landscape.

### Wards of Protection

Enchanted wards, maintained by the temple, ensure the sanctity of the Ebon Fields. They deter grave robbers and malicious entities, preserving the tranquility and sacredness of the resting place.

## Services
The temple conducts daily funeral rites for city residents and oversees the proper interment of the deceased. Clerics also offer counseling services to the grieving, providing solace and guidance during times of loss.


## Notes

