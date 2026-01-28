---
tags:
  - Organization
art: z_Assets/Misc/PlaceholderImage.png
head:
  - "[[Josef Barvasi]]"
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
> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Type** | `INPUT[OrganizationType][inlineListSuggester:organizationtype]` |
> **Hierarchy** | `INPUT[Null][suggester(optionQuery("Campaign/Organizations/Hierarchies"), useLinks(partial)):hierarchy]` | 
> **Head** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):head]` |
> **Steward** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):steward]` |
> **Parent Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Worship** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):worship]` |
> **HQ** | `INPUT[Null][suggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):hq]` |
> **Operating Areas** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> ###### `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{organizationtype}][text]` |
> **Hierarchy** | `VIEW[{hierarchy}][link]` |
> **Head** | `VIEW[{head}][link]` |
> **Steward** | `VIEW[{steward}][link]` |
> **Parent Organization** | `VIEW[{organization}][link]` |
> **Worship** | `VIEW[{worship}][link]` |
> **HQ** | `VIEW[{hq}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!recite]+ Introduction
> A script for the GM to read when the party arrive to this location for the first time.

> [!metadata|geography]- Geography
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Geography") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Settlement") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|district]- Districts
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "District") AND econtains(organization, this.file.link)
> SORT districttype ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE contains(tags, "POI") AND econtains(organization, this.file.link)
> SORT poitype ASC, file.name ASC

> [!metadata|organizations]- Child Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "Organization") AND econtains(organization, this.file.link)
> SORT organizationtype ASC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(organization, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview
Barvasi’s Band is a **ruthless, unaffiliated gang of enforcers and smugglers** operating in Bridgefront. Originally muscle-for-hire, they became **entangled in the cult war** between the excommunicated and loyalists of Mog-Lathar after being hired by **Myra Lombroso** to protect Brotherhood interests. Their theft of sacred items ignited the final collapse of the cult and accelerated the nightmare plague.

## Culture
The Band operates like a **street-level syndicate**, running illicit protection rackets, enforcing shiver deals, and intimidating anyone who threatens their turf. They value **strength, loyalty, and pay**, but have no real ideology—**greed and survival** motivate them more than belief.

They mock the cult’s obsession with dreams and avoid the Hook Street House, calling it **“the Spider’s Mouth.”**
## Acquaintances

- **Josef Barvasi** (Leader): A brutal young man and son of the infamous Devargo Barvasi. Josef sees reclaiming the shiver trade as his birthright.
    
- **Moses Greeley**: Myra’s handler for drug operations; employed the Band.
    
- **Frell Tann**: Former associate who betrayed the Band and stole the Paginarum Lethargica.
    
- **Nahum Caligaro (enemy)**: The Band inadvertently offended Nahum by stealing from his failed ritual site.

## Dialogue

> “We’re not cultists. We’re cleaners. You leave a mess, we take it out—and we don’t ask which god bled on it first.”  
> — _Eisen, Barvasi thug, moments before surrendering_

## Current events

- The Band stole the **Clavis Somnus** and **Paginarum Lethargica**, unknowingly crippling the Brotherhood’s dream-ritual.
    
- Now **hunted in their sleep** by **Nahum’s dreamspawned cult**.
    
- Most members are either **dead**, **killed in their dreams**, or **fleeing the city**.
    
- One of their safehouses—**Rook’s Roost**—became the site of a massacre.
## History

- Formed in the wake of **Devargo Barvasi’s death** and the collapse of the Cerulean Society’s monopoly.
    
- Took advantage of the power vacuum to muscle in on the **shiver trade**.
    
- Myra hired them for strength and plausible deniability, but they betrayed her by trying to ransom the stolen cult relics.
    
- Their actions triggered **Nahum’s vengeance** and contributed to the rise of the **nightmare plague**.

## Notes

- Their gang symbol is a  **broken bottle wrapped in wire**.
    
- Known for using **spider-leg sickles** soaked in dream poisons.
    
- Superstitious thugs claim that **“dreams remember your name if you steal from gods.”**

## Interrogation

Name: Eisen Winoli

### 🧍 “We were hired muscle. That's all.”

- “Boss Barvasi said we were guarding cargo. Drugs, mostly. Some books. Weird gear. Old junk with spider symbols.”
    
- “We kept our mouths shut, we got coin. Simple.”
    
- “Greeley ran the shipments. We guarded him, kept the coinboys in line, and made sure the Night Market stayed ours.”
    

---

### 📕 “Frell stole something. That’s when things went bad.”

- “This guy Frell—fancy shirt, too many teeth—he lifted some relic from the old house. A big book and a weird key.”
    
- “He tried to sell it, but got sliced up. We dumped what was left of him in the Roost pig pen.”
    
- “Then something... _came after us._ People started waking up screaming. Some didn't wake up at all.”
    

---

### 💉 “The dreams ain't just bad—they’re _real._”

- “We started hearing things. About people dying in their sleep. Faces locking up, eyes open, skin like ash.”
    
- “One of our boys started ranting about a _woman made of spiders_. Another slit his wrists in a dream—and bled out while snoring.”
    

---

### 🕷️ “Barvasi don’t believe in the cult—he just wants his cut.”

- “He don’t kneel to no spider. But he played the cult for gold.”
    
- “He took that book and key from Greeley’s people. Said he’d _sell it to someone who knew what to do with it_.”
    
- “He was gonna ransom the whole cult. Idiot thought he could out-deal priests and nightmares.”
    

---

### 🕳️ “The Hook Street House? We don’t go there.”

- “We were told _never_ to step inside the old compound.”
    
- “One guy did, once. Heard voices, saw a kid with no eyes. He bit his tongue off in his sleep that night.”

### Trying to explain:

> “We thought it was just a con. A spooky name, a creepy house, big payday. We didn’t know we were _stealing from a goddamn nightmare._”

### 😱 Real fear:

> “They come in dreams now. Barvasi’s hiding because they’re hunting us. And if you’re here... they probably know your name, too.”