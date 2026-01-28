---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/Lower Market.webp
pronounced: Lower Market
aliases:
  - Lower Market
poitype:
  - Shop
  - Shop [General]
location:
  - "[[The Port District]]"
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
> The Pier Market in Ilayas is a lively and enchanting hub of commerce, situated at the heart of the Port District. It is a bustling marketplace where travelers, merchants, and locals converge to explore a diverse array of goods, from exotic magical artifacts to fresh seafood.

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

### Layout and Atmosphere

The Pier Market is an expansive, open-air market, stretching along the waterfront of the Ilayas Pier. The market is covered by a series of billowing, translucent canopies that shield shoppers from the elements while allowing the soft, diffused light to filter through. The canopies are adorned with enchanted wind chimes that tinkle in harmony with the gentle lake breezes, creating a melodious, magical ambiance.

### Stalls and Booths

A labyrinth of stalls and booths lines the market, each offering a unique assortment of goods. Colorful awnings and vibrant banners flutter above these makeshift shops, making it a visually stimulating experience. The stalls are constructed from a variety of materials, from reclaimed driftwood to intricate wrought iron, each bearing the mark of the vendor's personality.

### Merchants and Vendors

The market is populated by a diverse group of merchants, from seasoned traders to local artisans. Characters may encounter mystical potion sellers, enchanters peddling spell scrolls, sellers of rare herbs and spell components, and even practitioners of local magical arts. Fishmongers and seafood vendors also offer fresh catches from Tamlem Lake, their stalls adorned with shimmering fish scales.

### Magical Trinkets and Artifacts

One section of the market is dedicated to magical trinkets and artifacts. Visitors can find everything from enchanted jewelry to mystical crystals, spell-imbued garments, and even curious curiosities from distant lands. The market is known for its collection of rare and powerful magical items, some of which have fascinating histories.

### Fresh Seafood Stands

Seafood stalls and eateries are scattered throughout the market, offering a mouthwatering assortment of fresh catches from the lake. Visitors can indulge in grilled fish skewers, oyster platters, and clam chowder. The tantalizing aroma of sizzling seafood fills the air.

### Local Artisans

Local artisans, weavers, and craftsmen offer their wares, including handwoven textiles, pottery, and wooden carvings. These items often bear the mark of the Pier District's unique culture and are appreciated for their quality and authenticity.

### Aroma of Spices and Herbs

The market is filled with the tantalizing scent of spices, herbs, and incense. Fragrant stalls offer exotic blends of spices and magical herbs, adding an enchanting dimension to the sensory experience.

## Wares 

### **Magical Trinkets and Artifacts:**

- Spell-infused crystals
- Protective amulets and talismans for seafarers
  
|**Item Name**|**Item Level**|**Price**|**Description**|
|---|---|---|---|---|
|Aqua Ward Amulet|5|160gp|This amulet, adorned with intricate wave patterns, provides resistance 5 against water-based attacks or effects, offering protection against aquatic creatures or magical assaults related to water.|
|Arcane Resonance Shard|4| 80gp|When held, this crystal resonates with the Arcane energies, faintly vibrating when spells are cast within 30 feet of it. It doesn't amplify or disrupt spells but serves as a subtle indicator of magical presence.|

### **Herbs and Spell Components:**

- Rare and exotic herbs
- Alchemical ingredients
- Spell reagents like whale's blood resin and sea algae
  
|**Item Name**|**Item Level**|**Price**|**Description**|**Uses**|**Existing Item in Pathfinder 2e**|
|---|---|---|---|---|---|
|Starbloom Petals|3|3 gp|These rare petals, harvested under moonlight, possess faint magical properties, often used in potion brewing.|Crafting potions, enhancing medicinal properties|New item|
|Voidroot Extract|4|8 gp|Extracted from deep caverns, this essence has shadowy properties, vital in concocting elixirs of darkness.|Crafting elixirs, creating shadowy effects|New item|
|Luminescent Lichen|2|3 gp|A glowing lichen found in secluded caves, prized by alchemists for its ability to produce faint light for hours.|Crafting glow potions, creating light sources|New item|
|Phoenix Feather|5|15 gp|A feather obtained from a rare phoenix, it possesses regenerative properties, crucial in potent healing elixirs.|Crafting powerful healing potions|New item|
|Fey-Infused Crystals|6|20 gp|Crystals imbued with traces of Fey magic, used in advanced alchemical formulas to enhance magical potential.|Crafting high-level magical elixirs|New item|

|**Potion Name**|**Recipe**|**Effect**|**Price**|
|---|---|---|---|
|Elixir of Starlight|Starbloom Petals + Luminescent Lichen|Grants darkvision for 1 hour, allowing sight in darkness as if it were dim light.|11 gp (craft: 3 gp + 3 gp)|
|Elixir of Shadow Veil|Voidroot Extract + 2xLuminescent Lichen|Grants brief concealment, providing a bonus of +4 to Stealth checks for 1 minute.|30 gp (craft: 8 gp + 2x3 gp)|
|Phoenix's Revival Elixir|Phoenix Feather|Restores significant health instantly (e.g., 3d6+6)  and gain +1 item bonus to saving throws against diseases and poisons for 10 minutes.|30 gp (15 gp) (Elixir of Life (Lesser))|
|Potion of Strength| Fey-Infused Crystals + Giant's toe| When you drink this potion, you gain a +2 to Athletics checks for 1 hour.| 100 gp|
|Fey-Infused Mana Draught |Fey-Infused Crystals + Arcane Essence|This mana draught crafted using crystals from the Fey realm is often cobalt-blue and is used by spellcasters to restore focus. When you drink this potion you recover levels of expended spells equal to the listed number. This potion has no effect on characters with no spellcasting feature. Potions do not stack; if multiple potions are being consumed take the higher effect.|Varies (see below)| 
- Type Minor - Lv3 - Price 12gp 
This portion restores 1d4 levels worth of spell slots.
- Type Lesser - Lv6 - Price 80gp 
This portion restores 2d4 levels worth of spell slots.
- Type Moderate - Lv12 - Price 500gp 
This portion restores 3d4 levels worth of spell slots.
- Type Greater - Lv16 - Price 2500gp 
This portion restores 4d4 levels worth of spell slots.
- Type Major - L19 - Price 15000gp 
This portion restores 5d4 levels worth of spell slots.

### **Local Artisans' Crafts:**

- Handwoven textiles and tapestries
- Pottery and ceramic works
- Wooden carvings and sculptures
  
|**Item Name**|**Item Level**|**Price**|**Description**|**Mechanical Effect**|
|---|---|---|---|---|
|Celestial Veil Shawl|-|15 gold pieces|A shimmering handwoven shawl made from rare, silken threads infused with faint celestial patterns.|No|
|Tapestry of Elemental Harmony|-|40 gold pieces|A grand tapestry depicting intertwining representations of elemental planes, handwoven with vibrant threads.|No|
|Emberglow Vase|-|8 gold pieces|A ceramic vase adorned with intricate patterns resembling flickering flames.|No|
|Aquatic Serenity Bowl|-|12 gold pieces|A beautifully crafted bowl depicting scenes of serene underwater life, glazed with calming hues.|No|
|Forest Guardian Totem|-|25 gold pieces|A wooden sculpture intricately carved to represent a guardian spirit of the forest.|No|
|Stargazer Sculpture|-|18 gold pieces|A delicately carved wooden sculpture of an individual gazing at the stars.|No|

### **Spices, Herbs, and Incense:**

- Exotic spices and seasonings
- Herbal teas and potions
- Aromatic incense and mystical herbs

**Exotic Spices and Seasonings**

|**Item Name**|**Item Level**|**Price**|**Description**|
|---|---|---|---|
|Elysian Saffron Threads|3|10 gold pieces (gp)|Threads of saffron harvested from Elysian fields, known for their vibrant color and rare, rich flavor.|
|Zephyr Salt|4|8 gold pieces (gp)|Fine-grained salt harvested from the windswept cliffs of Zephyr Peaks, lending a unique taste and aroma.|
|Emberwood Spice Blend|5|12 gold pieces (gp)|A blend of exotic spices found near volcanic regions, adding a smoky, fiery flavor to dishes.|

**Herbal Teas and Potions**

|**Item Name**|**Item Level**|**Price**|**Description**|
|---|---|---|---|
|Tranquil Serenity Tea|3|6 gold pieces (gp)|A calming herbal tea that soothes the mind and grants a bonus against mental stress for a short duration.|
|Draught of Euphoria|4|15 gold pieces (gp)|A potion brewed from rare herbs inducing a state of euphoria, providing a temporary boost to morale.|
|Verdant Vitality Elixir|5|18 gold pieces (gp)|An elixir brewed with rejuvenating herbs, granting a temporary increase to stamina and energy levels.|

**Aromatic Incense and Mystical Herbs**

|**Item Name**|**Item Level**|**Price**|**Description**|
|---|---|---|---|
|Celestial Harmony Incense|3|8 gold pieces (gp)|Incense crafted from mystical herbs, used for meditation and calming, providing a serene atmosphere.|
|Moonlit Sage Bundle|4|10 gold pieces (gp)|Bundles of sage harvested under moonlight, known for their purifying properties and mystical aura.|
|Astral Dreamweed|5|20 gold pieces (gp)|Rare herb with soporific properties, aiding in vivid dreaming and enhancing one's dream recall.|

### **Fresh Seafood:**

- Grilled fish skewers
- Oyster platters
- Clam chowder
- Freshly caught catches from Tamlem Lake
  
|**Dish**|**Description**|**Price**|
|---|---|---|
|Grilled Fish Skewers|Skewered pieces of freshly caught fish, marinated in aromatic herbs and grilled to perfection.|3 silver pieces (sp)|
|Oyster Platters|Freshly shucked oysters served on a bed of ice, accompanied by lemon wedges and various zesty sauces.|5 silver pieces (sp)|
|Clam Chowder|A hearty soup filled with tender clams, potatoes, and vegetables simmered in a creamy, flavorful broth.|7 silver pieces (sp)|
|Freshly Caught Catches|Assorted catches from Tamlem Lake, including trout, catfish, and perch, served grilled or fried.|Varies based on catch|

### **Magical Art:**

- Paintings, sculptures, and art imbued with enchantments
- Portraits and images that move or change
  
### Moving or Changing Portraits and Images

|**Artwork**|**Description**|**Price**|
|---|---|---|
|Portrait of Animated Memories|A portrait that subtly shifts, displaying memories or scenes related to the viewer's past or desires.|70 gp|

### **Handmade Jewelry:**

- Unique rings, necklaces, and bracelets
- Jewelry imbued with magical properties
- Custom-designed pieces with personal significance

|**Item Name**|**Item Level**|**Price**|**Description**|**Mechanics**|
|---|---|---|---|---|
|Seraphic Star Necklace|3|80 gp|A delicate necklace adorned with a star-shaped gem, granting a minor bonus to Perception checks.|Grants a +1 item bonus to Perception checks.|
|Crest of Eternity Ring|4|100 gp|A ring featuring an eternal loop design, offering a small bonus to saving throws against enchantments.|Provides a +1 item bonus to saving throws against enchantments.|
|Amulet of Arcane Insight|3|120 gp|An amulet granting a bonus to Arcana checks, attuned to the wearer's affinity with magical energies.|Provides a +1 item bonus to Arcana checks.|
|Enchanter's Ruby Ring|4|140 gp|A ring adorned with a ruby that enhances spell potency, increasing spell DC for specific spell schools.|Increases the DC of chosen spell schools by 1.|
|Ancestral Signet Ring|3|120 gold pieces (gp)|A ring bearing family insignias, offering a bonus to checks related to Society.|Grants a +1 item bonus to checks related to Society.|New item|

### **Local Cuisine and Street Food:**

- Unique culinary creations using magical ingredients
- Enchanted desserts and sweets
- Elemental drinks and beverages

|**Dish**|**Description**|**Price**|**Mechanics**|
|---|---|---|---|
|Ethereal Essence Soup|A mystical broth brewed from enchanted ingredients, shimmering with ethereal hues and offering clarity of mind.|10 gp|Grants a +1 item bonus to saves against mental effects for 1 hour.|
|Astral Flame Grilled Steak|A perfectly seared steak infused with astral essence, emitting a faint glow and providing a warm, invigorating feeling.|25 gp|Provides resistance 5 to cold for 10 minutes.|
|Feywild Forest Salad|A vibrant salad featuring enchanted greens and fruits from the Feywild, providing a surge of energy and vitality.|12 gp|Grants a +5-foot status bonus to Speed for 1 hour.|
|Celestial Confectionery|Heavenly candies crafted from celestial honey and infused with radiant energy, providing a subtle healing effect.|12 gp|Restores 1d8 Hit Points when consumed.|
|Ember Ale|A fiery ale infused with elemental fire essence, warming the drinker from within and leaving a hint of ember.|15 gp|Grants a +1 item bonus to Fortitude saves against cold for 1 hour.|
|Zephyr Breeze Cocktail|A refreshing cocktail made with elemental air essence, creating a cooling sensation and a slight levitation effect.|15 gp|Provides a +5-foot status bonus to your next Jump for 1 hour.|
|Crystal Clear Spring Water|Pure spring water imbued with elemental earth essence, offering clarity of mind and a grounding effect.|30 gp|Grants a +1 item bonus to Will saves against mental effects for 1 hour.|


## Notes

