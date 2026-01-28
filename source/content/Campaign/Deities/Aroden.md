---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Unsorted/Aroden.png
aliases:
  - The Last Azlanti
alignment: Lawful Neutral
deitypower: Greater God
condition: Dead
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
> **Current Location** | `VIEW[{location}][link]` |
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

## Patron Deity of Humanity
**Aroden** (pronounced AIR-oh-den) was the immortal Azlanti human who raised the _Starstone_ from the bottom of the Inner Sea in 1 AR, founded the city of Absalom, and became the patron deity of humanity. He was once prophesied to lead humanity into an Age of Glory, but on the day of his supposed return, he apparently died of mysterious causes, catapulting Golarion into an uncertain future and the Age of Lost Omens.



## History

### Azlanti Empire

Aroden was born in the tumultuous final days of the Azlanti Empire. According to legends, he was an unrivalled blacksmith and Azlant's premier swordmaker, and personally wielded many of his swords to defend Azlant from the chaos of its last decades. He was a follower of Acavna, the Azlanti moon goddess, and Amaznen, god of magic. His most famous creation during this time was the _Azlanti Diamond_, a clear jewel-bladed sword intended to be the weapon of the next Azlanti emperor. When the then-emperor failed to choose a successor from a pool of unimpressive candidates, he asked Aroden to decide for him, and Aroden took it upon himself to keep the _Azlanti Diamond_. Many believe this decision provoked the veiled masters to call down Earthfall to destroy Azlant in -5293 AR.

Following the destruction of his homeland, Aroden led the Azlanti survivors east to the empire's colonies in Avistan and tried to salvage the empire's vast cultural legacy, especially its unparalleled magical developments. During this period, Aroden somehow became immortal even as his contemporaries intermarried with the locals, had children, grew old, and died. Over time he acquired the titles of the "Last of the First Humans" and the "Last Azlanti" because he was ostensibly the last fully High Azlanti to die by several thousand years.

---

### Absalom and Ascension

More than 5,000 years after the destruction of Earthfall, the mortal Aroden was called to the Inner Sea, where he found the _Starstone_ and was subjected to the Test of the _Starstone_ upon contact with it. After succeeding, he became a god, and his first act as a god was to raise the _Starstone_ from the watery depths he found it in, along with the surrounding earth, to form the Isle of Kortos.

In order to bring life to the slime-covered Isle of Kortos, Aroden stole five life-giving orbs from the Orvian vault of Vask, which he called _aeon orbs_, believing that they could be put to a better use aiding humans than supporting Vask's native xulgaths. He placed each _aeon orb_ on a mudbrick Aeon Tower and linked their magic to his own essence, quickly turning the islands green, particularly around the towers. Unknown to Aroden, the sole _aeon orb_ he left in Vask was insufficient to maintain its ecosystem; soon enough, the vault was transformed into a lifeless waste of black sands by the radioactive crystals on its ceiling.

Aroden transferred the _Starstone_ to its current resting place in the Starstone Cathedral at the center of Absalom, the city he established on the coast of the Isle of Kortos.

---

### Aroden's Fate

Since Aroden's death, clerics no longer receive his spells. Countless theories exist about how he might have died, including a battle with Rovagug or Asmodeus, a journey beyond the Outer Sphere, or reincarnation into a mortal man to save humanity. The gods might know his true fate, particularly Pharasma, but if they do, they have not revealed it to mortals.



## Notes

