---
tags:
  - "#Location"
  - "#Geography"
art: z_Assets/Locations/Teseon Logo.png
pronounced: Tess-eh-on
aliases:
  - Monument to Magics
terrain:
  - Hills
  - Plains
  - Urban
  - River
  - Forest
  - Mountains
location:
  - "[[Ilayas]]"
  - "[[Improck]]"
organization:
  - "[[Ilayas Council]]"
  - "[[Sanctum of the Final Veil (Org)]]"
  - "[[Veil of Shadows]]"
  - "[[The Kenay Order]]"
  - "[[The Jade Gate]]"
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
> **Terrain** | `INPUT[Terrain][inlineListSuggester:terrain]` |
> **Dominion** | `INPUT[inlineListSuggester(optionQuery(#Character OR #Organization AND !"z_Templates"), useLinks(partial)):dominion]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Terrain** | `VIEW[{terrain}][text]` |
> **Dominion** | `VIEW[{dominion}][link]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>


> [!metadata|map]- Map
> ```leaflet
> id: Teseon
> image: ![[Teseon + Oshad 1.png]]
> height: 600px
> width: 600px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 2.5
> zoomDelta: 0.5
> unit: meters
> scale: 1
> darkMode: false
> https://docs.google.com/spreadsheets/d/1jKQxktYSUFcCJhEkAAPr1wMVBTqUdpEfA5XveUXI17I/edit?usp=sharing
> ```

> [!metadata|county]- Counties
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "County")
> SORT nation ASC, file.name ASC

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Settlement")
> SORT nation ASC, file.name ASC

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
> WHERE contains(location, this.file.link) AND contains(tags, "Organization")
> SORT organizationtype ASC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview 

The Teseon Empire is run by the Council of Three and Nine. The council is currently dominated by the Three rather than the Nine. An agreement between any two of the Three is sufficient to veto any proposal agreed on by the Nine. In contrast to the Nine, the composition of the Three has not changed for over 100 years.

The Three

- Archmage Devati Vilicus - leader of the Arclords of Teseon
- Iranez of the Orb - a powerful witch
- Elder Architect Oblosk - castellan of the castle at Inazzur’s Hold

The Nine

- Master Alchemist Borume - representative of the Hel Ra Citadel
- Dunn Palovar - representative of the Cephorah Tower
- Master Phade - representative of Inazzur Hold’s
- Archdean Darchana of House Madinani - First Spell Lord and leader of [[Arcanamirium]]
- Elemion - representative of Alkenstar
- The high cleric of Nethys
- The high cleric of Pharasma
- A representative of the nation's Merchant's League
- A politician serving one of the many other factions (changes constantly)

## Current Events

The Angel Day festival in [[Ilayas]].

## History

The technologically and magically adept expansionistic nation known as the Jistka Imperium (today Teseon Empire) was the first major human civilization to emerge after Earthfall and the subsequent ash-clouded Age of Darkness. Though it endured for a mere 700 years before its decline, the empire was highly influential in bringing humanity back to the surface of Brightwyn—albeit through conquest and dominion—and at its peak Jistka’s borders spanned from current-day Tirion to the south, to the eastern shores of the Abecean Ocean. The rise of Ancient Osirion eventually spelled the downfall of Jistka in –2764 AR, and after that the ancient kingdom focused on consolidating the already owned territories and expanding their scientifical and magical knowledge.

Teseon boasts one of the most cosmopolitan and refined cities of Ailira, with the capital at Inazzur’s Hold rivaling the extravagance of Auridon in Tirion or Ragn-Thar in the era of the legendary God-Kings of Osirion. Monumental palaces and impossible spires crowd the city’s chaotic streets, which also wind past hanging gardens, open-air mazes, and bustling souks. The statue of powerful wizards and the ancient heroes who traveled far and wide and helped forge the empire look out upon the city’s roofs and balconies, a constant reminder of those who made Innazur’s Hold and the surrounding land their own.

The mages of Teseon Empire established important tenets of magical theory that remain influential today, and vastly enriched their nation through adventures and the judicious application of wish-level magics. Territorial ambitions and disagreements on how to use their magical knowledge drove two factions (Geb and Nex) into conflict with one another, until one of them split and formed the Kingdom of Oshad. The conflict spanned for centuries, with each nation employing more and more powerful spells which turned the once-green fields to the south into a wasteland (known today as the Mana Wastes), but it also altered how magic works in the region. The devastation created areas devoid of magic—pockets where magic simply does not work at all. In other areas, the laws of reality themselves have been damaged, and magic becomes dangerously wild and unpredictable. This is known as primal magic, and it sometimes lashes the land with spontaneous waves of raw magical energy. These areas are not stable, often alternating between states of dead magic, primal magic, and normal magic, although the primal magic state is the most common.

## Notes

