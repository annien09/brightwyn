---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Isiril Adren.webp
pronounced: Ee-see-reel
aliases:
  - Isiril
ancestry: Elf
heritage: Ancient Elf
gender: Female
pronouns: She/Her
age: Adult
sexuality: Gay
alignment: 
language:
  - Common
  - Elven
  - Undercommon
occupation:
  - Diplomat
  - Royal
  - Warder
organization:
  - "[[The Kenay Order]]"
  - "[[Sanctum of the Final Veil (Org)]]"
location:
  - "[[The Lunar Radiance Inn]]"
  - "[[Sanctum of the Final Veil]]"
  - "[[Aetherian Hall]]"
  - "[[Ilayas]]"
  - "[[Tirion]]"
condition: Healthy
party1relation: Ally
quest:
  - "[[Magical Research during Celestial Night]]"
  - "[[Becoming a Paladin]]"
  - "[[The Veridane Ball]]"
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
>> **Ancestry** | `INPUT[Ancestry][suggester:ancestry]` |
>> **Heritage** | `INPUT[Heritage][suggester:heritage]` |
> **Creature Type** | `INPUT[textArea:ancestry]` |
> **Creature Sub-Type** | `INPUT[textArea:heritage]` |
>> **Gender** | `INPUT[Gender][:gender]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]` |
>> **Age** | `INPUT[Age][:age]` |
>> **Sexuality** | `INPUT[Sexuality][:sexuality]` |
>> **Alignment** | `INPUT[Alignment][:alignment]` |
>
>> [!metadata|metadataoption]- NPC Info
>> #### NPC Info
>>  |
>>---|---|
>> **Languages** | `INPUT[Language][inlineListSuggester:language]` |
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):religion]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):ownedlocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>> **Condition** | `INPUT[Condition][:condition]` |
>> **Quest** | `INPUT[inlineListSuggester(optionQuery(#Quest AND !"z_Templates"), useLinks(partial)):quest]` |
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
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Ancestry** | `VIEW[{ancestry}]` |
> **Heritage** | `VIEW[{heritage}]` |
> **Gender** | `VIEW[{gender}]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Age** | `VIEW[{age}]` |
> **Sexuality** | `VIEW[{sexuality}]` |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Languages** | `VIEW[{language}][text]` |
> **Occupations** | `VIEW[{occupation}][text]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |
> **Quest** | `VIEW[{quest}][link]` |


# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>
> [!recite]+ Introduction
> Isiril Adren is a striking contrast to her elder brother, [[Siramin Adren]], both in appearance and chosen path. Her shoulder-length light-blonde hair, divided by a distinctive undercut, symbolizes the duality within her nature — a balance between tradition and rebellion, honor and individuality. The braids intricately woven into the undercut carry a symbolism of her dedication and commitment to her calling as a champion.

> [!metadata|quest]- Quests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(status, ", ") AS Status
> FROM "Campaign"
> WHERE econtains(NPC, this.file.link) AND contains(tags, "Quest")
> SORT tags DESC, file.name ASC

> [!metadata|letters]- Letters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|literature]- Literature
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Literature")
> SORT file.name ASC

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

## About
Raised in the royal halls of Auridon alongside her brother, Isiril felt drawn to a different calling than the expected path of governance. Her fervent devotion to the goddess Pharasma guided her steps toward a life of service and protection. Her decision to become a paladin of Fate within Pharasma's order was a testament to her belief in the interconnectedness of all things and the guiding hand of destiny.

Leaving the comforts of Tirion behind, Isiril ventured to the neighboring nation of [[Teseon]], seeking to broaden her understanding of the world and her faith. There, she found herself in the company of the [[Alinya Vilicus]], drawn together by a shared sense of duty and a desire to bring about positive change.

As a Champion, Isiril embodies a sense of unwavering conviction and determination, tempered by compassion and a deep understanding of the complexities of fate and free will. Her experiences as an adventurer and a servant of Pharasma have honed her combat skills and granted her insight into the intricacies of destiny.

Despite her departure from Tirion, Isiril remains deeply connected to her roots and her family. She occasionally undertakes visits back home.


## Acquaintances
### Family:
#### [[Siramin Adren|Siramin]] - Elder Brother

### Friends:
#### [[Alinya Vilicus|Alinya]]
As followers of Pharasma, Isiril and Alinya share not only a common faith but a profound understanding of the mysteries of fate and the interconnectedness of all things. Their shared devotion to the goddess strengthens their connection, fostering a sense of spiritual kinship that goes beyond mere friendship.

However, their relationship takes a distinctive turn with Isiril serving as Alinya's Warder. As a Warder, Isiril takes on the responsibility of guarding and supporting Alinya, forging a bond that transcends the ordinary realms of friendship or mentorship.


## Notes





