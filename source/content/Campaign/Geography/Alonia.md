---
tags:
  - "#Location"
  - "#Geography"
art: z_Assets/Locations/Alonia logo.png
aliases:
  - "Matriarchal Monarchy  "
pronounced: Ah-loh-nee-ah
terrain:
  - Hills
  - Plains
  - Urban
  - River
  - Ocean
  - Forest
  - Mountains
dominion:
  - "[[Lysandra]]"
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
> defaultZoom: 1
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

## Overview 
Álonia is a country in the heart of the Westlands. It is the largest and most populous country in the West of Ailira. After Tirion and Y’Falin, it also has the largest and most well-trained army. Formerly a province of the Empire of Thassilon, the region has suffered enormous chaos and destruction after the event of the Earthfall and for hundreds of years the area lay in ruin after the Thassilon Empire collapsed.

Aroden himself was said to walk among the people of Álonia. Álonia’s ancient Armies of Exploration established footholds for the empire throughout Brightwyn, and during the Shining Crusade, the White Lions of Álonia marched for thousands of miles to beat back and imprison the Whispering Tyrant.

### Government 

Many of Álonia's traditions were established during the early years after the collapse of the Thassilon Empire. Unlike many nobles of the time, Queen Ishara knew that no one ruler would be able to take control of the entire empire. Instead, she focused on controlling only what she could. As a result, Álonia began only with the capital city of Aviria and the small surrounding villages. Cautious expansion marked the reigns of the early queens of Álonia.

The tradition of Álonia is that only a queen must sit on the Lion Throne of Álonia, and wear the Rose Crown. However, it wasn't always intended that a queen would rule - it happened that the sons of Álonia's first two Queens were killed, and so their daughters became queens. After this it became tradition that a queen would rule. The eldest daughter is known as the Daughter-Heir, and is always sent to Ardamin to study. The eldest sibling of the Daughter-Heir is sworn to protect her with their life, and is prepared from an early age to take control of Álonia's army. They are given the title First Prince(ss) of the Sword. 

If a Queen does not have a daughter, then another successor is appointed, judged by the number of blood ties she can establish to Ishara. Four times in Álonia's history this method has been disputed, leading to the Succession Wars. The current queen of Álonia is Queen Elayne of House Trakand.

> [!Prompt]- Queen Elayne Trakand
>![[Elayne Trakand.png]]
## Current Events


## History

The first half of the Age of Enthronement was the Golden Age of Álonia. It was in this era that Álonia formed the first of its now-legendary Armies of Exploration. Composed of thousands of soldiers, scholars, diplomats, surveyors, spies, and adventurers of all specialties, the Armies of Exploration were instrumental to Álonia’s expansion throughout Ailira. The first of the Armies of Exploration began in 37 AR in Aviria and headed north along the Amstable River, eventually reaching The Adamantine Highlands and forming an outpost at its base. The Second Army used the success of the first as a stepping stone, extending up along the northern coastline of the Malmer Sea, and finally reaching the orc hordes of Shaog Blar.

The Third Army of Exploration met with the greatest success. Again, starting in Alonia, this army forged east along the southern coast of Ailira and met with one victory after the other, until it extended all the way to the easternmost edge of the Inner Sea, where the army’s General Hallin founded the city of Hallin’s Stand in what is today Marquette, and secured Álonia’s control of passage into and out of the Inner Sea. No other Army of Exploration would ever match the Third Army’s success.

## Notes

