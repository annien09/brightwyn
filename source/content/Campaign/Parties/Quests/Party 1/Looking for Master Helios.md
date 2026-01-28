---
tags:
  - Quest
art: z_Assets/People/Master Helios Staven OG.webp
aliases:
  - Master Alchemist
quicknote: Finding the master Alchemist
adventure: "[[Nezoh]]"
whichparty: "[[Party]]"
status: ⏳
NPC:
  - "[[Master Helios Staven]]"
location:
  - "[[Ilayas]]"
---

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
>> **Aliases** | `INPUT[list:aliases]` |
>> **Quick Notes** |  `INPUT[textArea:quicknote]`
>> **Adventure** | `INPUT[Null][suggester(optionQuery(#Adventure AND !"z_Templates"), useLinks(partial)):adventure]` |
>> **Which Party** | `INPUT[Null][suggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Status** | `INPUT[Status][:status]` |
>>  **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>>  **NPC** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):NPC]` |

> [!infobox]
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> #### Quest Info
>  |
> ---|---|
> **Adventure** | `VIEW[{adventure}][link]` |
> **Status** | `VIEW[{status}]` |
> **NPC** | `VIEW[{NPC}][link]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`**
> [!recite]+ Introduction
> [[Eltane Gestal]] helped Nezoh with information on possible leads to Nezoh's goal.

> [!metadata|characters]+ Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(quest, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC


## Overview
Two or three year back during a council meeting that Alinya attended, the topic of Master Helios Staven's departure and his rumored quest to create a new city in the Mana Waste surfaced briefly. The discussion revolved around the potential impact of his actions on the magical community and the broader implications for Teseon's governance.

### Key Points of the Discussion

**Speculation and Concern**: Some council members expressed skepticism about the feasibility of Master Helios' ambitious endeavor. They questioned the practicality of establishing a city in such a harsh, magic-deprived environment, citing concerns about resources, sustenance, and the actualization of such a visionary goal.

**Magical Understanding:** Others were intrigued by the possibility that Master Helios might have uncovered ancient magical secrets that allowed him to use magic in the Mana Wastes. They deliberated on the potential impact of such discoveries on Teseon's magical practices and whether it could challenge conventional wisdom.

**Ethical Considerations:** Discussions also touched on ethical considerations—whether Master Helios' pursuit aligned with principles of cosmic balance or if his actions bordered on reckless experimentation that might disrupt the natural order. Some council members debated the responsibility of pursuing such ventures within the confines of ethical magic use. 

Also talks about what the foundation of a city on a land that belongs to the nation means, how that might affect the sovereignty granted to Alkenstar as well. 

### Rumor

There was also a rumor running around, but if it can be truly attributed to Master Staven or not, who can say.

Whispers have circulated among members of magical academies that have traveled to the Mana Wastes regarding a mysterious figure sighted inside barren lands. The rumor suggests the existence of a reclusive hermit or a solitary mage dwelling deep within the wasteland, shrouded in secrecy and rumored to possess peculiar magical abilities.

**Key Elements of the Rumor:** According to the rumor, a few individuals claim to have glimpsed a cloaked figure wandering the fringes of the Mana Waste, seemingly able to call upon magic that should not be possible. Some describe fleeting encounters with a mysterious, hooded figure engaged in mystical rites or communing with native aggresive creatures.

**Whispers of Unusual Magic:** The rumor further speculates that the enigmatic hermit might possess unique magical abilities—talks of a new school of magic, possible divination magic, or an uncanny connection with the lands devoid of magic. However, the details of these alleged abilities remain vague and embellished through speculative tales.

## About 
### Characters


### Creatures



### Locations



### Random Encounters



## Notes