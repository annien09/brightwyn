---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Elandra Nightshade.webp
pronounced: Eh-lan-dra
aliases:
  - The Mistress of Revels
  - High Cleric
ancestry: Elf
heritage: Ancient Elf
gender: Female
pronouns: She/Her
age: Mature Adult
sexuality: Bi/Pan
alignment: Chaotic Good
language:
  - Common
  - Elven
  - Sylvan
  - Undercommon
occupation:
  - High Priest
  - Spy
organization:
  - "[[Veil of Shadows]]"
ownedlocation:
  - "[[The Red Door]]"
location:
  - "[[The Red Door]]"
  - "[[Ilayas]]"
  - "[[The Port District]]"
condition: Healthy
party1relation: Unmet
quest:
  - "[[Investigating the Jade Gate]]"
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
> **The Mistress of Revels: Elandra Nightshade, High Priestess of Calistria**
In the heart of [[The Red Door]], presiding over the delicate balance between the sacred and the sensual, stands Elandra Nightshade. As the Mistress of Revels, Elandra is an elven woman of timeless beauty, grace, and a captivating air of mystery.

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

## Description
### Physical Appearance

Elandra is of moderate height, her lithe figure moving with a fluidity that echoes both elven elegance and the sensuality of her chosen profession. Cascading waves of black hair frame a face adorned with delicate elven features – almond-shaped eyes of blue hue and high cheekbones.

### Attire

Her attire is a careful fusion of ceremonial elegance and enticing allure. She wears flowing robes of crimson and gold, embroidered with intricate symbols sacred to Calistria. A sheer veil, adorned with gemstones, conceals just enough to leave an air of enchantment.

### Symbol of Calistria

Elandra proudly wears the symbol of Calistria – three daggers arranged in a circle, equidistant from each other, forming a perfect triangle within the circle – as a pendant around her neck. The wings of the butterfly seem to shimmer in response to the ebb and flow of the passions that traverse her domain.

### Demeanor

Elandra exudes an aura of confidence and charisma, her voice a melodic blend of honey and silk. Her laughter, as rare as it is delightful, dances like the wind through the chambers of [[The Red Door]], carrying with it an invitation to revel in both pleasure and reverence.

### Clerical Abilities

As a cleric of Calistria, Elandra is versed in both the sacred rites of her goddess and the mystical arts that enhance the experiences within [[The Red Door]]. She possesses a keen intuition that allows her to guide patrons to experiences that align with their deepest desires.

### Wisdom and Discretion

Known for her wisdom, Elandra is a confidante to many. Those seeking advice or solace find a sympathetic ear in the Mistress of Revels. Her discretion is unwavering, and tales of those who have sought her counsel are whispered like secrets through the corridors of [[The Red Door]].

### Balancing Act

Elandra effortlessly navigates the intricate dance between the divine and the carnal. She is both a spiritual guide, leading worshipers in rituals of devotion, and a custodian of earthly pleasures, ensuring that the desires of her patrons are met with care and respect.

### The Moonlit Balcony

Elandra often retreats to the moonlit balcony overlooking the harbor, where the gentle lapping of the waves serves as a backdrop to her contemplations. There, she finds solace in the rhythmic pulse of the city and the ever-present embrace of the goddess Calistria.



## Aspirations
Elandra Nightshade, the Mistress of Revels, stands as a beacon of enchantment within [[The Red Door]], embodying the essence of Calistria's teachings — a delicate dance between passion, revenge, and the pursuit of one's desires.

## Conversation

>Elandra: Welcome to The Red Door, honored guests. I am Elandra Nightshade, the Mistress of Revels. Your presence brings a unique vibrancy to our sanctuary. How may I guide you through the pleasures that await?

>Elandra: (Nodding with understanding) Ah, a celebration of life's mysteries and joys. You've chosen wisely. Our temple offers a tapestry of experiences — each chamber, a canvas for desires to be painted upon.

>Elandra: (Her eyes glint with anticipation) We offer a wide array of services - **DESCRIBE THE PLEASURE SERVICES [[The Red Door]]**

During the festival a celebration is underway in honor of the moon's dance with the sea. Dancing, music, and shared revelry await those who wish to partake. Or, if you prefer a more intimate encounter, our private chambers offer a haven for personal celebrations.

#### SECRETS [[The Red Door]]

>Elandra: (Leaning in, her voice a velvet whisper) In addition to the pleasures The Red Door provides, we offer a unique service for those seeking discretion and insights into the tapestry of Ilayas' secrets. Patrons may inquire about our "Veil of Shadows" services.

>Elandra: (A knowing smile) The Veil of Shadows is a delicate art, a service dedicated to the weaving of secrets and the preservation of confidentiality. Should you seek knowledge that lies in the shadows of Ilayas, our discreet network can provide you with insights, rumors, and whispered truths.

>Elandra: (Pausing for emphasis) The secrets of [[Ilayas]] are as diverse as the city itself. From the clandestine dealings of noble houses to the silent machinations within the city's shadows. We can offer glimpses into the intricacies of the noble families, revealing alliances, rivalries, and the hidden affairs that dance beneath the surface.

**LIST OF PRICES**

#### Access to Secrets

>Elandra: (Extending a delicate hand) Accessing the services is a simple matter. When the moon is high and the tapestries of [[The Red Door]] whisper with the night's secrets, approach the Shrouded Altar in the main atrium. Leave a discreet **but suitable** offering, and a representative from our temple will contact you with the information you seek. The Veil of Shadows is discreet, ensuring that your inquiries remain private.


## Notes





