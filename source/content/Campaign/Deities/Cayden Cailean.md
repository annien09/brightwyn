---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Cayden.png
aliases:
  - The Drunken Hero
alignment: Chaotic Good
NPC:
  - "[[Gideon Wavebreaker]]"
  - "[[Gunther]]"
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



## God of bravery, ale, freedom, and winey

Alignment: CG

Domains: Cities, freedom, indulgence, might

Favoured Weapon: Rapier

The legends say that Cayden Cailean never meant to become a god. As a hired sword working out of Absalom, Cayden was renowned for taking on any job, so long as the cause was just and the coin was plentiful. One night, in an intoxicated stupor, a fellow drunk dared him to take on the Test of the Starstone. He accepted, and somehow, 3 days later, Cayden Cailean emerged from the Starstone’s sacred cathedral as a living god. Amazed that he passed the tests and unable to remember how he did it, he continued in his godly life much as he did when a mortal—fighting for just causes, enjoying various alcohols, and doing only what he wanted to do. This simple philosophy appeals to many mortals both high and low, and adventurers, philanthropists, revellers, and freedom fighters all claim him as their patron god. In art, Cayden Cailean appears as he did in life, as a bronze-skinned man carrying a tankard of ale in one hand. Some depictions of the Drunken Hero display broken shackles about his wrists, representing Cayden’s escape from the concerns of mortal life.

Members of Cayden’s faith make excellent guides and explorers, quick to smile at danger and always willing to have fun even in the direst of circumstances. His festive temples resemble common ale halls and attract members of all social classes. Formal raiment is a simple brown tunic or robe with a wine-red stole bearing his ale-mug symbol (adventurer-priests of the faith sometimes carry a magical stole that doubles as a rope). He has few buildings that function only as temples; most are actual alehouses bearing a shrine to him above the bar. His simple holy text is the Placard of Wisdom, condensing his divine philosophy into a few short phrases suitable for hanging on the wall.

The faithful of Cayden Cailean often carry tankards with them for luck, or pause before a particularly dangerous or stressful task to pour a splash of ale out upon the ground. He often shows his approval through the discovery of a fresh bottle of wine, but in cases where a mortal has instead drawn his ire, such found bottles invariably taste of vinegar or raw sewage.
## Notes

