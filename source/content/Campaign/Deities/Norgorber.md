---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Norgorber.png
aliases:
  - The Reaper of Reputation
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

## God of greed, murder, secrets, and poison
Alignment: NE

Domains: Death, secrecy, trickery, wealth

Favoured weapon: Shortsword

Little is known of Norgorber’s life in Absalom before he ascended to godhood through the Test of the Starstone. Members of his debased faith go to great lengths to keep his life a secret, using murder if necessary to obscure Norgorber’s origins. Some believe that if the Reaper of Reputation’s true nature were discovered, he would be undone. Of the known Ascended gods, he is the only evil one.

Norgorber’s cult splits itself into four groups, with each focusing on one of his aspects and ignoring the others. They often wear masks both as a symbol of this devotion and to keep their identities a secret (even in Absalom, where their faith is marginally allowed). Some worshipers even carry additional masks to portray different emotions or signals, holding them in front of a simplified mask they only remove in private.

Despite the division in the faith, Norgorber’s followers still work together in some regards, taking careful actions meant to shape the future, all according to some secret plan. Those who call him the Reaper of Reputation venerate him primarily as the god of secrets and are typically spies or politicians. Thieves’ guilds often venerate him as the Gray Master, and look to his skills as a thief more than anything else. Many alchemists, herbalists, and assassins know him as Blackfingers and see his work in every poisoned meal and venomous beast. Yet his most notorious, and most dangerous cultists are the madmen, murderers, and maniacs. These cultists know him as Father Skinsaw, and believe that with every murder, the future is sculpted according to their dark god’s unknowable plan.

Ceremonial colours are black and brown, and ceremonial clothes themselves usually follow current fashion so the wearer can blend in with those outside the faith. Elaborate masks, often with coloured lenses and hinged jaws, are used to invoke the mysteries of the divine in Norgorber’s various aspects. Temples dedicated to Norgorber are often hidden in other businesses, transformed at night so the faithful can plot and pray. His clerics are master imitators, stealing others’ identities and using them to cover up dark deeds or to destroy other organizations from within.

## Notes

