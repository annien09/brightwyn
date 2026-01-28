---
tags:
  - "#Location"
  - "#Geography"
pronounced: Ky Ed-hill
art: z_Assets/Locations/Cai Edhil logo.png
aliases:
  - Home to Nature and Spirits
terrain:
  - Hills
  - Plains
  - River
  - Ocean
  - Swamp
  - Jungle
  - Forest
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

Cai Edhil is a densely forested, sub-tropical region that encompasses the south-eastern coastal plain of Ailira. Home to the wood elves who rejected the formal traditions of high elf culture, preferring a more romantic, simple existence in harmony with the land and its wild beauty and creatures. Other denizens include centaurs, fey and migratory trees, but also humans, halflings and any other race which enjoys the nature. It is a sea of endless green, a maze of foliage with half-hidden cities growing like blooms from a flower.

The ancient wood elves of Cai Edhil were generally disinterested in most forms of magic, viewing wizards and other arcane spellcasters with no small amount of distrust as it was the magic of the Azlant Kingdom who almost destroyed the entire world if not for the sacrifices of the elves. They were largely at ease with the ways of the primal magic used by druids, which was used to protect the wilderness and therefore had provable results. However, wood elves were not completely adverse to arcane magic and wood elven bards, sorcerers, and wizards were far from unknown, but wood elves as a whole had no particular tradition of the art.

Like their elven ancestors the wood elves largely worship the Elven Pantheon, alongside other deities on Brightwyn like Desna, Erastil, Gozreh and Shelyn. Many wood elves have a special place in their heart for the elven gods Ketephys, the god of hunting, and Findeladlara, the goddess of art that is particularly interested in its preservation and the preservation of the elven culture.

### Government 
The elves of Cai Edhil have two leaders, the **Gwaith Omah** and the **Quarlan Omah.**

The Gwaith is the Leader of the People in Cai Edhil. While often viewed by outsiders as a title for the  political representative for foreign affairs, the Gwaith is more than a mere politician. Each person who bears the title is thought of as merely the Gwaith's aspect. The Gwaith represents the People legally and physically, in contrast to the Quarlan, who is their spirituality. It is said to be the union of the two that makes Cai Edhil whole. The Gwaith reflects the state of the People in his way of thinking, his health, and even his gender. He is inseparably tied to the people, and they to him, making him supernaturally empathic and aware of their concerns. As the Leader of the People, the Gwaith has many rights which grant him great authority in Cai Edhil. For one, only the Gwaith can grant foreign building and trade contracts, meaning any foreign power which wishes to build in Cai Edhil or do business with the wood elves must deal with the Gwaith first.

The responsibilities of the Quarlan are much the same as the responsibilities of the Gwaith - the protection of the People of Cai Edhil. Unlike the Gwaith, however, the Quarlan will protect her people with far more extreme methods, especially when the Gwaith isn't around to restrain her. When hunting to keep the forests safe for the people, the Quarlan risks losing herself entirely. Fortunately, her Gwaith is capable of bringing her back.

According to the Quarlan, her memories stretch back to the Age of Creation, but no one knows exactly what her origin is. What it is clear is that her embodiment of the primal ferocity, health, strength is comparable to that of a demigod.

After the death of the previous Quarlan and Gwaith, the Council of the Elders will typically reveal the next person to carry on the role. A potential Quarlan will often display indications of such, even before their predecessor dies through near-supernatural feats. As opposed to the Gwaith, the potential to be the Quarlan seems to be something that can be passed down.

> [!Prompt]- Gwaith Gaeltan Adeus
> ![[Gwaith Gaeltan Adeus.png]]

> [!Prompt]- Quarlan Ashisae
> ![[Quarlan Ashisae.png]]


## Current Events

[[Aelwynn Ianven]] and [[Krel Ianven]] are originally from Cai Edhil.

## History

How the Gwaith and, by extension, Quarlan, came to be is shrouded in mystery. Some folktales claim that before the calamity of the Earthfall, and elven prince named Syldon was walking through all the forests of the world, looking for a place to belong. It was in the Galtara forest that from the wild came a being like no other. Her eyes were of fire, hair of wind and rain, and all who dared look upon her shook in fear. All except Syldon. Seeing that he would not shy away, the being retreated to protect her homeland, trying to lose Syldon in the dense forest, but the trees themselves made way for the elven prince to follow her to the heart of the forest. In a bright clearing by a river whose waters seemed to run silver, she faced the prince and lunged at him, but Syldon did not fight back for he did not wish to harm neither her nor her realm.

It was Syldon’s inaction that made the being look into his heart and see the purest of intentions, to protect the wonders of nature and to live as one with the elements, with her. It was there that the two became one, their union giving birth to a new kingdom, with Syldon becoming the first Gwaith, the Leader of the People, and the demigoddess became the first Quarlan, the spiritual leader and protector of the Realm. The Gwaith and the Quarlan are profoundly linked, and there must always be a pair. When one perishes, the other will soon follow.

After being named 'King of the Woodland Realm', Syldon established his capital in Gir-Val-Delle in the middle part of the forest. Cai Edhil flourished in peace with its boundaries unchanged and way of life undisturbed for over 3000 years.

## Notes

