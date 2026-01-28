---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/The Lunar Radiance Inn.webp
pronounced: Lunar Radiance
aliases:
  - Lunar Radiance
poitype:
  - Shop [Tavern]
  - Shop
location:
  - "[[The Wealthy District]]"
  - "[[Ilayas]]"
owner:
  - "[[Astern Lobreil ]]"
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
> Situated within the Inner City of Ilayas, the Lunar Radiance Inn stands as a beacon of luxury and sophistication.

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

## Appearance
### Exterior

The inn's exterior boasts celestial motifs, with spires reaching towards the sky and intricate engravings depicting constellations and celestial beings. The architecture combines magecraft with artistic finesse, captivating passersby with its ethereal allure.

### Interior

Inside, the Lunar Radiance Inn is adorned with celestial-themed decorations. Crystal chandeliers cast a soft, enchanting glow, and celestial murals adorn the walls, depicting cosmic landscapes and celestial events.

### Ambiance

The inn exudes an air of refinement and grandeur, with ornate architecture and tasteful embellishments that reflect the city's mage-centric culture. Crystal chandeliers, plush furnishings, and celestial-themed decor create an elegant and enchanting atmosphere.

### Magical Enchantments

The inn itself is enchanted, providing guests with comforts beyond the mundane. Enchanted hearths that provide warmth without smoke, floating lights reminiscent of stars, and soothing melodies that seem to emanate from the very walls contribute to the inn's enchanting ambiance.

## About
### Astern Lobreil - owner  
**Aquatic Features:** Astern embodies the Azarketi's aquatic nature with pale, opalescent skin that shimmers like the moon reflecting on the ocean's surface. Her skin glistens with a faint pearlescent hue, a testament to her connection to the sea.

 **Aquatic Eyes:** Instead of the usual azure eyes, Astern's eyes gleam with the luminosity of bioluminescence, displaying hues of a bright sky-blue that is reminiscent of clear ocean waves.

**Name Choice** During Astern's childhood she bore witness to a Solar eclipse and saw the Sun slowly being veiled by the moon. She cannot explain it but she experienced a moment of clarity and an overwhelming sense of connection with the cosmos.

## Menu
**Lunar Radiance Inn Menu**

**Appetizers:**

- _Stardust Soup_: A celestial-inspired blend of rare herbs and vegetables - 4 gold pieces (gp)
- _Moonlit Seafood Platter_: Assorted exotic seafood delicacies from Tamlem Lake - 8 gp
- _Starlight Salad_: Fresh greens, celestial fruits, and infused dressing - 5 gp

**Main Courses:**

- _Astral Steak_: Prime cut of magical beef, seasoned with celestial herbs - 12 gp
- _Enchanted Sea Bass_: Freshly caught and infused with coastal spices - 10 gp
- _Celestial Pasta_: Handcrafted pasta with rare mushrooms and celestial cream sauce - 7 gp

**Desserts:**

- _Lunar Cheesecake_: Creamy cheesecake topped with moonlit berries - 6 gp
- _Starry Night Sorbet_: Icy delight infused with exotic flavors - 4 gp
- _Galactic Chocolate Mousse_: Rich, decadent mousse with a celestial twist - 7 gp

**Beverages:**

- _Nebula Nectar (House Specialty)_: A celestial-inspired blend of exotic fruit juices - 3 gp
- _Stellar Sparkle Wine_: Sparkling wine with hints of celestial fruit - 9 gp per glass / 40 gp per bottle
- _Moonlit Elixir (Non-alcoholic)_: Refreshing drink infused with lunar herbs - 2 gp

**Accommodations:**

- _Celestial Suite_: Lavish suite with a private balcony and enchanting views - 50 gp per night
- _Aurora Chamber_: Elegant room with luxurious amenities - 30 gp per night
- _Stardust Quarters_: Comfortable lodging for a relaxing stay - 20 gp per night

_Note: Prices may vary based on seasonal availability and market fluctuations._
## DM Notes

>[REDACTED]
## Notes

