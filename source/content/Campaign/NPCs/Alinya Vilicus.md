---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Alinya Vilicus.webp
pronounced: A-lee-nee-a
aliases:
  - Alinya Vilicus
ancestry: Human
heritage: Versatile Heritage
gender: Female
pronouns: She/Her
age: Adult
sexuality: Straight
alignment: 
language:
  - Common
  - Elven
occupation:
  - Mage
  - Noble
organization:
  - "[[The Kenay Order]]"
  - "[[Sanctum of the Final Veil (Org)]]"
  - "[[Ilayas Council]]"
location:
  - "[[The Lunar Radiance Inn]]"
  - "[[Aetherian Hall]]"
  - "[[Ilayas]]"
condition: Healthy
party1relation: Ally
quest:
  - "[[Magical Research during Celestial Night]]"
  - "[[Scrying on Krel]]"
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
> Alinya's background is shaped by her lineage, devotion to magic, and unwavering dedication to the teachings of Pharasma, particularly within the domain of Fate.

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
Alinya carries an air of elegance and confidence. Her presence commands attention—a tall, poised figure with long, flowing light-blonde hair. Her eyes, reminiscent of stormy seas, hold a depth of wisdom and determination. She dresses in robes adorned with intricate celestial patterns, symbolizing her connection to cosmic forces.


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
### Demeanor and Temperament

Alinya possesses a calm and composed demeanor, even in the face of adversity. She radiates an aura of grace and empathy, her voice carrying a soothing quality that belies her inner strength. She's known for her strategic mind, diplomacy, and a willingness to seek peaceful solutions.

### Lineage and Council Involvement

Born into the esteemed family of the Archmage Devati Vilicus, one of The Three - the highest echelon of Teseon's ruling council-, Alinya grew up amidst the intricacies of political governance and magical heritage. Her upbringing in the capital city immersed her in the circles of influence and responsibility that come with noble lineage. Alinya holds sway in Teseon's council, advising on matters of magic, destiny, and governance. Her counsel is highly valued, and she strives to bridge divides and foster unity.

### Magical Aptitude and the Kenay Order

From a young age, Alinya displayed remarkable magical aptitude, drawing attention for her innate talent and dedication to honing her arcane prowess. Her affinity for magic led her to [[the Kenay Order]], a revered faction dedicated to Pharasma's teachings of Fate, prophecy, and the threads that weave destiny. As a member, she delved deep into the mysteries of Fate, seeking to understand the intricate tapestry of life's twists and turns. She wields formidable arcane power, specializing in divination and fate manipulation. Her spells are precise and potent, reflecting her years of dedicated study and practice.

### Alignment and Devotion to Pharasma

Alinya's attitude with her beliefs in maintaining a balance between order and compassion. Her devotion to Pharasma is unwavering, rooted in the belief that Fate's intricacies should guide individuals toward paths of benevolence and fairness. She sees herself as a guardian of destiny, striving to use her magical abilities for the betterment of others and the preservation of cosmic balance.

### Advocacy and Council Influence

Though not holding a seat herself, Alinya's influence within Teseon's council is palpable. Her counsel on matters concerning magic, destiny, and ethical governance is highly regarded. She advocates for policies that prioritize fairness, individual agency, and the respect of Fate's role in the lives of the citizens.

### Personal Traits and Convictions

Alinya is known for her empathy and wisdom, traits instilled by her upbringing, teachings, and personal experiences. Her decisions are guided by a sense of duty to both her family's legacy and the moral compass she developed through her devotion to Pharasma's teachings.

>[REDACTED]

## Acquaintances
### Family:
Archmage Devati Vilicus holds a prominent position as one of The Three—the highest-ranking counselors within Teseon's ruling council. He is a respected figure known for his wisdom, astute political acumen, and dedication to preserving the stability and prosperity of Teseon. Devati is recognized for his contributions to magical governance, advocating for fairness, and balancing the council's decisions with ethical considerations. He shares Alinya's world view, often striving to ensure that the council's decisions align with principles of justice and compassion.

### Friends:
#### [[Isiril Adren]] - Warder
As followers of Pharasma, Isiril and Alinya share not only a common faith but a profound understanding of the mysteries of fate and the interconnectedness of all things. Their shared devotion to the goddess strengthens their connection, fostering a sense of spiritual kinship that goes beyond mere friendship.

However, their relationship takes a distinctive turn with Isiril serving as Alinya's Warder. As a Warder, Isiril takes on the responsibility of guarding and supporting Alinya, forging a bond that transcends the ordinary realms of friendship or mentorship.




#### [[Siramin Adren]]


## History


## Notes





