---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/Discount Bazaar.webp
aliases:
  - Discount Bazaar
poitype:
  - Shop [General]
  - Shop [Magic]
  - Shop
location:
  - "[[Ilayas]]"
  - "[[The Port District]]"
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
> [!kirk|info] Info (Remove me)
> Point of Interest: A location within your world, anything from a homes, shops, forts, volcanos or dungeons.

> [!recite]- Introduction
> 

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
Nestled within the bustling Port District of Ilayas, the Discount Bazaar stands as a treasure trove of eclectic goods and unexpected finds. The shop, with its weathered but welcoming exterior, caters to adventurers, sailors, and curious locals seeking affordable wares.

## About

### Exterior

The Discount Bazaar's exterior is a mishmash of colorful banners and faded signs, hinting at the diverse array of goods within. Sturdy wooden shelves outside display discounted items, beckoning passersby with promises of bargains.

### Sign

A whimsical sign swings above the entrance, depicting a winking merchant surrounded by bags of gold and curious trinkets. The words "Discount Bazaar" are boldly painted in a mishmash of vibrant hues, adding a touch of charm to the otherwise unassuming storefront.

### Layout

Once inside, visitors are greeted by shelves and tables, each overflowing with an assortment of merchandise. The shop is organized by categories such as potions, scrolls, curiosities, and even used magical items.

### Wares

The Discount Bazaar prides itself on offering a bit of everything. Shelves hold dusty tomes with worn covers, enchanted knick-knacks, and a variety of trinkets that seem to have found a second home here. Barrels near the entrance overflow with mysterious odds and ends waiting to be explored.

### Atmosphere

Despite the apparent disorder, there's a sense of excitement in the Discount Bazaar. Adventurers sift through dusty scrolls, sailors haggle over navigational instruments, and locals search for peculiar trinkets to add to their collections. The air is tinged with the scent of ancient parchment and the faint hum of enchantment.

### Pricing Strategy

Quillen's pricing strategy is as whimsical as his shop's appearance. Items bear tags with crossed-out original prices, replaced by a seemingly arbitrary, but often more affordable, figure. It's a place where haggling is not just expected but encouraged.

### Rumors and Lore

The Discount Bazaar is not just a shop; it's a repository of stories. Locals claim that Quillen has a keen eye for magical potential, and many a hero has found a crucial tool or a mystical relic hidden among the seemingly mundane.

## Shopkeeper

The shopkeeper, a wizened gnome named Quillen Quickcoin, presides over the chaos with a knowing smile. His sharp eyes catch every movement in the shop, and he's always ready with a quip or a tale about the origins of a particular item. Quillen is known for his knack for finding hidden gems amidst the clutter.

## Items

- Whispering Conch Shell - This enchanted conch shell allows the possessor to speak into it, and the sound is carried to another shell of the same kind, creating a telepathic link over short distances. This item allows the user to cast Message through the shell. - Price 25gp

- Ghost Ink - This pale-blue ink dries rapidly, becoming fully transparent 1 minute after application. The ink glows red when exposed to heat, such as that from a torch or other open flame. This glow lasts only as long as the ink is exposed to heat, after which the ink becomes invisible again. The crafter of the ghost ink can alter the formula slightly to instead make the ink sensitive to sunlight, starlight, magical light, or heatless light created by an alchemical effect such as a sunrod. While the text isn't glowing, a creature closely examining a surface marked with ghost ink can detect the presence of the ink with a successful DC 25 Perception check. On a critical success, they can make out the ink well enough to use Society to Decipher Writing. One vial of ghost ink is sufficient to write a page worth of text.

- Invisible Ink - This ink dries rapidly, becoming invisible 1 minute after application. The ink is visible only under the effects of the Detect Magic spell or similar magical illumination. - Price: 10gp

- Weatherworn Compass - This compass always points toward the nearest significant weather event within 50 miles, such as a storm, rainfall, or clear skies. - Price 30gp

- Levitating Top Hat - While worn, this miniature top hat hovers above the wearer's head. While more of a novelty, it has been known to distract enemies and entertain children.
  
- Glowing Gemstone Pebbles (set of 5) -  These 5 small, enchanted gemstone pebbles emit a soft glow, providing dim light in a 5-foot radius. They can be used to mark paths or create temporary magical markers. - Price: 5gp




## Notes

