---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Calistria.png
aliases:
  - Calistria, The Savoured Sting
alignment: Chaotic Neutral
deitypower: Greater God
ownedlocation:
  - "[[The Red Door]]"
NPC:
  - "[[Elandra Nightshade]]"
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


## Goddess of revenge, lust, and trickery
Alignment: CN

Domains: Pain, passion, secrecy, trickery

Favoured Weapon: Whip

Calistria is a goddess of many faces and guises, including lust and revenge. Some favour her as a trickster goddess, while others appreciate her lustful, audacious spirit. Ever scheming and planning her next conquest, Calistria is always manoeuvring to attain a more advantageous position. Spies, prostitutes, and thrill seekers are often followers of Calistria. Iconography of the faith depicts her as the ideal of elven beauty, dressed in revealing gowns and having long, graceful ears, slender limbs, and a suggestive smile playing across her lips. Giant wasps, her favoured creatures, commonly appear beside her; unlike bees, wasps can sting again and again without dying—which represents Calistria’s vindictiveness.

Temples to Calistria often host a lively community of sacred prostitutes, each with his or her own contacts in the community. The resulting hotbed of gossip, double-dealing, and opportunities for revenge assure the cult’s growing popularity. In elven lands, her temples are more like thieves’ guilds, catering to suspicious lovers seeking evidence and wealthy folk wishing to escalate feuds, and only secondarily serving as a place for carnal release. Formal clothing is very scant, typically yellow silk that covers little and conceals even less, often augmented with henna dyes on the palms of the hands and in narrow bands on the arms. Her holy text is The Book of Joy, a guide to many passions.

Calistria’s promiscuity is well documented in many religious texts (including her own), but often these accounts seem to be at odds, indicating that some of her supposed trysts may be little more than wishful thinking on the parts of other gods and goddesses. Some tales preach that Cayden Cailean got drunk and took the Test of the Starstone after Calistria rebuffed his advances, claiming that no mortal could enjoy her charms and survive.

Calistria shows her favour by granting sudden runs of luck in worshipers’ attempts to find companionship, while those who displease her often find themselves plagued by wasps with an unerring ability to sting in sensitive places.

## Notes

