---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/The Cleric's Wineskin.webp
pronounced: Giddy's
aliases:
  - Cleric's Wineskin
poitype:
  - Shop [Tavern]
  - Shop
location:
  - "[[Ilayas]]"
  - "[[The Port District]]"
owner:
  - "[[Gideon Wavebreaker]]"
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
> Nestled along the bustling docks of Ilayas' Port District, The Cleric's Wineskin is a charming inn that beckons weary travelers and locals alike. With its weathered wooden exterior and a sign adorned with a serene cleric raising a wineskin in a toast, this inn offers more than just a place to rest.

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

The Cleric's Wineskin boasts a façade adorned with maritime charm. Sea-themed tapestries flutter in the salty breeze, and potted plants line the entryway, creating a lively and welcoming atmosphere.

### Entrance

As patrons step through the arched doorway, they are greeted by the comforting scent of salt air and the low hum of conversations. A flickering lantern above the entrance casts a warm glow, inviting travelers to find respite within.

### Common Room

The heart of the inn is its common room, adorned with driftwood furniture and nautical trinkets. A crackling fireplace provides a cozy nook for patrons to share tales of the sea over mugs of ale.

### Bar

The bar, polished to a sheen, showcases an impressive array of spirits. The innkeeper, a seasoned sailor turned host, stands ready to recommend a selection of fine wines and hearty ales to suit every palate.

### Rooms

Upstairs, guests find modest yet comfortable chambers adorned with maritime motifs. Ship wheels, compass roses, and sea charts decorate the walls, evoking a sense of adventure and seafaring spirit.

### The Proprietor

The inn's proprietor, [[Gideon Wavebreaker]], a retired cleric with a penchant for storytelling, warmly welcomes guests. With a twinkle in his eye and a wineskin always at hand, Gideon ensures that every visitor feels a sense of camaraderie.

### Culinary Delights

The kitchen, tucked away behind the bar, produces delectable seafood dishes and hearty stews. The scent of freshly baked bread wafts through the air, tempting even the most discerning palates.

### Harbor-View Terrace

For those seeking a breath of sea air, a terrace overlooks the bustling harbor. Wooden tables and lanterns create an enchanting ambiance, making it the perfect spot to enjoy a sunset drink or a morning coffee.

### Events Board

Near the entrance, an events board displays announcements for maritime gatherings, local festivals, and rumored tales of mystical seacreatures. Patrons often find leads to new adventures and opportunities.

### The Healing Quarters

A unique feature of The Cleric's Wineskin is a small room dubbed "The Healing Quarters," where a resident cleric offers basic healing services to patrons, ensuring that even the battle-weary find solace.

## Menu

#### Starters

- **Salted Cod Cakes** - Pan-fried cod cakes served with a zesty dipping sauce. _(8 silver pieces)_
- **Seaside Salad** - Mixed greens, cherry tomatoes, and cucumber in a tangy vinaigrette. _(6 silver pieces)_
- **Garlic Shrimp Skewers** - Grilled shrimp skewers marinated in garlic and herbs. _(10 silver pieces)_

#### Main Courses

- **Fisherman's Stew** - A hearty stew with fish, potatoes, and carrots. _(8 silver pieces)_
- **Sailor's Pie** - Flaky pastry filled with seafood and creamy sauce. _(9 silver pieces)_
- **Sailor's Sandwich** - Grilled fish fillet with lettuce, tomato, and tartar sauce on a bun. _(7 silver pieces)_

#### Sides

- **Salted Sea Beans** - Sautéed sea beans with garlic and lemon. _(4 silver pieces)_
- **Sailor's Slaw** - Coleslaw with a tangy dressing. _(3 silver pieces)_
- **Seafarer's Fries** - Crispy fries seasoned with sea salt. _(5 silver pieces)_

#### Desserts

- **Sea Salt Caramel Pudding** - Creamy caramel pudding topped with sea salt. _(5 silver pieces)_
- **Nautical Nut Tart** - A nut-filled tart with a hint of cinnamon. _(6 silver pieces)_
- **Tropical Fruit Cup** - A refreshing mix of seasonal fruits. _(4 silver pieces)_

#### Drinks

- **Seabreeze Sip** - A refreshing mix of fruit juices. _(3 silver pieces)_
- **Mariner's Mug Ale** - Locally brewed ale with a hint of citrus. _(4 silver pieces)_
- **Seaside Sipper** - A non-alcoholic fruity drink. _(2 silver pieces)_

## Notes

