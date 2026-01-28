---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/The Knight and the Goblet.webp
pronounced: Knight and the Goblet
aliases:
  - Knight and the Goblet
poitype:
  - Shop [Tavern]
  - Shop
assistant:
  - "[[Teryn Ward]]"
owner:
  - "[[Master Sigmur Reydun]]"
location:
  - "[[Ilayas]]"
  - "[[The Common District]]"
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
> Nestled within the heart of Ilayas' bustling Common District, the The Knight and the Goblet Inn is a cozy and inviting establishment that caters to travelers, mages, and visitors seeking refuge in the vibrant city.

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

> [!warning]+ Message
> Behind the counter is who you would assume to be the bartender, a man in his middle 20s with colorfully painted nails who is currently shuffling a pack of cards. You walk up to the bar, and strike up conversation with the man, who introduces himself as [[Teryn Ward]].

## Description
### Exterior

As characters approach the The Knight and the Goblet Inn, they are greeted by a charming, two-story building constructed from weathered and enchanted oak wood. Above the entrance, a faded but welcoming sign swings gently in the breeze, depicting a gallant knight raising a goblet in a toast.

### Entrance and Common Room

As guests enter, they are greeted by the comforting aroma of hearth-baked bread and the soft murmur of conversation. The common room is adorned with wooden beams, sturdy tables, and mismatched chairs that invite patrons to relax in a casual setting.

### Fireplace

A crackling fireplace, adorned with simple tapestries, takes center stage, providing a cozy warmth during chilly evenings. It serves as a focal point for guests to gather, share stories, and unwind.

### Bar Area

The modest bar, fashioned from polished oak, is stocked with a selection of local ales and spirits. A friendly innkeeper stands ready to offer recommendations and share tales of the city.

### Dining Area

The dining area boasts sturdy wooden tables covered with checkered tablecloths. Guests can enjoy affordable, hearty meals prepared with locally sourced ingredients. The menu includes comfort foods like savory stews, fresh bread, and seasonal desserts.

### Affordable Decor

The decor is simple but thoughtful, featuring a few framed landscapes and sketches on the walls. Local artwork and crafts, obtained from nearby artisans, contribute to the inn's character.

### Dining Area

The dining area boasts sturdy wooden tables covered with checkered tablecloths. Guests can enjoy affordable, hearty meals prepared with locally sourced ingredients. The menu includes comfort foods like savory stews, fresh bread, and seasonal desserts.
### Community Board

A community board near the entrance displays announcements for local events, job postings, and even a few handwritten notes expressing gratitude from satisfied guests.

### Goblet Emblem

The inn's emblem—a knight raising a goblet—is prominently displayed throughout, symbolizing the establishment's commitment to providing a convivial space for relaxation and good company.

## Notes

### Innkeeper's Recommendations

The innkeeper takes pride in providing personalized recommendations for local attractions, markets, and events. Guests can rely on these suggestions for an authentic experience in Hearthstone Haven. [[Teryn Ward]]

### Menu
**Mains**
Barbecued Tiger Fish +5sp
Rack of Lamb Platter +5sp
Pork Chop and Curds
Baked Potatoes and Pork Loin with Gravy
Broiled Salmon and Potatoes
Squash and Fish Soup

**Dessert**
Cornbread
Roseapple pie

#### Breakfast

- **Sunrise Omelette** - A three-egg omelette filled with sautéed mushrooms, cheese, and herbs. _(3 sp)_
- **Morning Glory Porridge** - A hearty bowl of oats, nuts, dried fruits, and a hint of honey. _(2 sp)_
- **Rise and Shine Platter** - Bacon, eggs cooked to your liking, toast, and a side of roasted potatoes. _(5 sp)_

#### Lunch

- **Mage's Veggie Wrap** - Fresh vegetables, hummus, and herbs wrapped in warm flatbread. _(4 sp)_
- **Hunter's Stew** - Hearty stew filled with game meat, root vegetables, and savory spices. _(6 sp)_
- **Elven Salad** - Mixed greens, berries, nuts, and a tangy vinaigrette. _(3 sp)_

#### Dinner

- **Dragonfire Grilled Steak** - Juicy steak seasoned with spices and grilled to perfection. _(8 sp)_
- **Sea Serpent's Delight** - Grilled fish served with a citrus glaze and accompanied by seasoned rice. _(6 sp)_
- **Harvest Moon Risotto** - Creamy risotto made with seasonal vegetables and topped with parmesan cheese. _(5 sp)_

#### Desserts

- **Enchanted Apple Tart** - Sliced apples baked in a flaky crust, sprinkled with cinnamon and sugar. _(4 sp)_
- **Feywild Berry Cheesecake** - Rich and creamy cheesecake topped with a medley of wild berries. _(5 sp)_
- **Sorcerer's Chocolate Delight** - Decadent chocolate cake served with a scoop of vanilla ice cream. _(6 sp)_

#### Beverages

- **Elixir of Refreshment** - Freshly squeezed fruit juice of your choice. _(2 sp)_
- **Dwarven Ale** - A hearty, robust ale brewed in the depths of the mountains. _(3 sp)_
- **Elven Wine** - A delicate and fragrant wine from the vineyards of the elves. _(4 sp)_
- **Mage's Brew** - A special blend of herbal tea, brewed with mystical herbs. _(2 sp)_

### Rooms

The inn offers a variety of rooms, each adorned with basic furnishings and a comfortable bed. Quaint floral bedspreads and homemade quilts add a touch of homeliness. Small windows allow natural light to filter in during the day.


| Lodging                                       | Day  | Meal | Drink |
| --------------------------------------------- | ---- | ---- | ----- |
| Comfortable - shared room + shared amenities  | 9 sp | 5 cp | 3 cp  |
| Moderate - private room + private bath access | 3 gp | 3 sp | 1 sp  |

***Prices are Per Person**

### Patrons

>[REDACTED]