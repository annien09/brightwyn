---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Pharasma.png
aliases:
  - Lady of Graves
alignment: True Neutral
deitypower: Greater God
organization:
  - "[[The Kenay Order]]"
  - "[[Sanctum of the Final Veil (Org)]]"
ownedlocation:
  - "[[Sanctum of the Final Veil]]"
NPC:
  - "[[Alinya Vilicus]]"
  - "[[Isiril Adren]]"
  - "[[Aelwynn Ianven]]"
  - "[[Arioneth Duskwhisper]]"
  - "[[Acolyte Tharion Shane]]"
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

## Goddess of birth, death, fate, and prophecy

Alignment: N

Domains: Death, fate, healing, knowledge, soul, time

Favoured weapon: Dagger

Sitting atop an impossibly tall spire, Pharasma’s Boneyard awaits all mortals. Once there, they stand in a great line, waiting to be judged and sent to their final reward. Only the unworthy end up in her graveyard, their souls left to rot for all eternity.

Legends claim that Pharasma knew the death of Aroden was fast approaching and even judged him, but did nothing to warn her own followers, many of whom were driven mad by the event.

Pharasma is depicted as a midwife, a mad prophet, or the reaper of the dead, depending upon her role. Pregnant women often carry small tokens of her likeness on long necklaces to protect the unborn and to grant it a good life. Her followers are midwives, expectant mothers, morticians, and (though less so since Aroden’s death) diviners.

Pharasma’s temples are gothic cathedrals, usually located near a town’s graveyard, although a single bleak stone in an empty field or graveyard can serve as a shrine. Her faithful dress in funereal clothes for religious ceremonies, always black (regardless of the local custom) and accented with silver and tiny vials of holy water. They despise the undead as abominations to the natural order. Her holy book is The Bones Land in a Spiral; much of it was written long ago by a prophet, and many of its predictions are so vague that there is much debate about what events they foretell and whether they have already passed. Other sections were added later and deal with safe childbirth, proper disposal of the dead, methods of performing auguries, and so on.

Pharasma manifests her favour through the appearance of scarab beetles and whippoorwills, both of which function as psychopomps that serve to guide recently departed spirits to the Boneyard. Black roses are thought to bring good luck, especially if the rose’s stem sports no thorns. Pharasma sometimes allows the spirit of someone who died to send short messages to living kin to comfort them, to expose a murderer, or to haunt an enemy. Her displeasure is signified by cold chills down the spine, bleeding from under the fingernails, an unexplained taste of rich soil, the discovery of a dead whippoorwill, or the feeling that something important has been forgotten.
## Notes
