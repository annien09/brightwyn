---
tags:
  - "#Location"
  - "#Geography"
art: z_Assets/Misc/Tirion logo.png
pronounced: Tee-ree-oh-n
aliases:
  - Kingdom of the Elves
terrain:
  - Hills
  - Plains
  - River
  - Forest
  - Mountains
  - Coastline
  - Urban
  - Ocean
dominion:
  - "[[Siramin Adren]]"
  - "[[Isiril Adren]]"
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
> [!recite]+ Introduction
> Tirion is the traditional home of the High Elves, and possibly the first landing place of the elves arriving from their ancient homeland.

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
> https://docs.google.com/spreadsheets/d/1jKQxktYSUFcCJhEkAAPr1wMVBTqUdpEfA5XveUXI17I/edit?usp=sharing
> ```


> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Settlement")
> SORT nation ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)", join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "POI")
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

## Current Events


## History
The elves came to Brightwyn during the Age of Legend when humanity was nothing more than barbaric tribes and the fey inhabited the land. As the elven population grew, they explored past where their fey friends, who stayed connected to the nature, advanced, reaching other corners of the world. In their exploration they discovered other sentient and civilized races who preferred to stay secluded, one of those races being the algollthus.

It was the algollthus that brought down a star to destroy the human kingdom of Azlant whom they brought up from barbarism, and it was due to the elves, and especially their queen, that not all of the world was sunken beneath the waves or destroyed by the star.

Queen Nylanna Adren, ever since her birth was thought to be destined for greatness. She was widely considered the most beautiful of high elves and swiftly became the most beloved monarch in elf history. Strong-willed, charismatic, and incomparably beautiful, Nylanna possessed far more magical talent than almost any other elf. As one of the Highborn and sole heir to the throne, she had a strong sense of duty towards her people.

When the Starstone struck Brightwyn and sunk the entire continent of Azlant, colossal wave rose forth and rushed for the patches of land which still stood. Nylanna, aware that her kingdom, her people and every other living soul on Brightwyn were threatened to be wiped by the massive waves rose to the highest point in her palace and wove a magical shield around herself and stopped the rushing water, saving the continent from being crushed by the colossal waves. As she was holding the anger of the oceans at bay, she commanded her son, Kaellevor, to gather the people and teleport along the coast and through the rest of the continent and create bubbles of protective magic in an attempt to keep the world afloat.

An elite order of magic users remained by her side, charging her with their own life force in order to buy enough time for the queen’s orders and evacuation plans to be executed. As Nylanna was maintaining the shield she could see a strange and dark algollthus magic seeping through and starting to twist and corrupt the land beneath her feet, encompassing the entire elven capital. Knowing what she had to do in order to stop it, Queen Nylanna connected her consciousness with that of her eldest son and relayed to him her plans for the future of the elves and charged him with containing the Blight in case her plans failed. After which, she willed the last of her powers to control the oceans and contain the Blight in what is known today as The Badlands. Her show of force was so great that it cracked the land beneath her feet and created the fjords within the Badlands.

Kaellevor fulfilled his mother’s vision of creating a new and safe nation for all the elves and protect the rest of civilization, and founded what is now the Kingdom of Tirion where the high elves still reside. He also allowed his people who preferred living with the fey to settle in the woods of Cai Edhil and form their own nation, as well as reinforced the elves who stayed behind in the Badlands to see that their queen’s sacrifice was not in vain.

Queen Nylanna’s line survives and leads the elves even today, the current king of Tirion being King Ferenthyl Adren.


## Notes

