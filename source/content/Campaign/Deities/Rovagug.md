---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Rovagug.png
aliases:
  - The Rough Beast
alignment: Chaotic Evil
deitypower: Greater God
---

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
>> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>> ---|---|
>> **Pronounced** |  `INPUT[textArea:pronounced]` |
>> **Aliases** | `INPUT[list:aliases]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]` |
>> **Alignment** | `INPUT[Alignment][:alignment]` |
>
>> [!metadata|metadataoption]- Deity Info
>> #### Deity Info
>>  |
>>---|---|
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Power** | `INPUT[DeityPower][:deitypower]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):ownedlocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>> **Condition** | `INPUT[Condition][:condition]` |
>> **Followers** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):NPC]` |
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Party 1 Relation** | `INPUT[Party1Relation][:party1relation]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ![[PlaceholderAudio.webm]]
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Followers** | `VIEW[{NPC}][link]` |
> **Condition** | `VIEW[{condition}]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|organizations]- Related Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE econtains(worship, this.file.link) AND contains(tags, "Organization")
> SORT organizationtype ASC, file.name ASC

## Overview


> [!column|2 no-title]
>
> 
>> [!metadata|ideals] Ideals
> `VIEW[{ideals}][text]`
>
>> [!metadata|flaws] Flaws
> `VIEW[{flaws}][text]`
> 
>> [!metadata|fear] Fears
> `VIEW[{fears}][text]`
>
>> [!metadata|mannerism] Mannerisms
> `VIEW[{mannerisms}][text]`


## God of destruction, disaster, and wrath
Alignment: CE

Domains: Air, destruction, earth, zeal

Favoured weapon: Greataxe

In the dawn of prehistory, Rovagug was born to destroy the world, but all the other gods stood against him, side by side. Many died in the struggle, but in the end, Sarenrae sliced open the world to imprison him within, and Asmodeus bound him there, keeping the only key. The only images of Rovagug show him as a terrible monster of unimaginable size and power.

Of all the religions, few are more despised by civilized people than Rovagug’s. In the wild lands, various monsters pay homage to him, including orcs, ropers, and troglodytes. Many of his faithful believe that Earthfall awoke their god, and that the time of his freedom is fast approaching. Foremost among the signs of his stirrings are the so-called Spawn of Rovagug, immense beasts who periodically surge from the Pit of Gormuz in between Osirion and the Waste, site of the Rough Beast’s imprisonment long millennia ago. The legendary Tarrasque is the most powerful and terrifying of the Spawn, although several others have left their mark upon history over the years.

Rovagug’s priests wear shaggy coats dyed in strange colours and hideous masks depicting horrid beasts, melted faces, or maddening shapes. His temples are banned in nearly every major city, driving his followers to erect secret shrines. The very rare temples are built in caves or dungeons and usually have some monster as the focus of worship, hand-fed by the priesthood to keep it reasonably tame except to outsiders.

Rovagug has no holy text, but his monstrous, primitive thoughts press themselves upon his worshipers, flooding them with a desire to break, destroy, and rend, as well as to find a means to end his imprisonment and bring about the end of the world. Rovagug has long railed against the other gods, but his hatred for Sarenrae eclipses all others. Even before the Dawnflower cast him down, their wars were legendary, and it is said that Sarenrae placed the fire of the sun in the core of the world to constantly burn him in his prison. Volcanic eruptions and earthquakes are held to be indications of him twisting in his sleep, and storms the evidence of his breath coursing up from the dark places of the world.

## Notes

