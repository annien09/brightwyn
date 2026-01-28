---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Urgathoa.png
aliases:
  - The Pallid Princess
alignment: Neutral Evil
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


## Goddess of disease, gluttony, and undeath
Alignment: NE

Domains: Indulgence, magic, might, undeath

Favoured weapon: Scythe

Some claim that Urgathoa was a mortal once, but when she died, her thirst for life turned her into the Great Beyond’s first undead creature. She fled from Pharasma’s endless line of souls and back to Brightwyn, bringing disease with her to the world.

She appears as a beautiful, raven-haired woman from the waist up, but below that her form begins to rot and wither, until only blood-covered bones remain at her feet. Urgathoa is worshiped by undead as well as by dark necromancers and those hoping to become undead. As such, her clerics must often keep their activities a secret. Some who are sick with the plague make offerings to the Pallid Princess in hopes of alleviating their illness, though most turn to Sarenrae. The occasional gluttonous prince might make offerings to Urgathoa as well, be it for more food, women, or other carnal pleasures. She and Calistria vie for control of their overlapping interest, with the elven goddess representing lust and the undead one representing physical excess.

Ceremonial clothes in her church consist of a loose, grey, floor-length tunic with a bone-white or dark grey shoulder-cape clasped at the front. Traditionally, the lower half of the tunic is either shredded or adorned with strips of cloth or tassels to give the overall appearance of increased damage as it approaches the floor, mirroring the goddess’s own decay. Because most ceremonies involve indulging in large amounts of food and wine, these garments are usually stained from spills.

Her temples are built like feast halls, with a large central table serving as an altar and numerous chairs surrounding it. Most temples are adjacent to a private graveyard or built over a crypt, often inhabited by ghouls (which embody all three of the goddess’s interests). Her sacred text is Serving Your Hunger, penned by Dason, her first undead knight-commander. Urgathoa sometimes rewards female clerics who serve her particularly well by transforming them after death into hideous undead creatures called the daughters of Urgathoa. She has also been known to lend support to the daemon Horsemen from time to time, for many of their goals closely match her own.

## Notes

