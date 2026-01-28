---
tags:
  - Organization
art: z_Assets/Misc/PlaceholderImage.png
aliases:
  - Mog-Lathar’s Chosen
  - The Silent Weavers
organizationtype:
  - Cult
head:
  - "[[Mog-Lathar, the Fossilised Idol]]"
steward:
  - "[[Myra Lombroso]]"
worship:
  - "[[Mog-Lathar, the Fossilised Idol]]"
hq: "[[Ilayas]]"
location:
  - "[[Dimension of Dreams]]"
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
>> ###### `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
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
The **Brotherhood of the Spider** is a hidden cult centered around the fossilized corpse of Mog-Lathar, a powerful Leng spider slain after Earthfall and reawakened as an idol. The cult combines nightmare-worship, planar esoterica, and criminal enterprise, primarily through its control of the shiver trade in Ilayas.

What began as a philosophical experiment in lucid dreaming turned dark as Myra Lombroso and Nahum Caligaro fell to Mog-Lathar’s whispers. Now, the Brotherhood operates as both a religious order and a narcotic cartel—funding dream rituals and immortality research by fueling Ilayas’ shiver epidemic.

The Brotherhood believes that dreams are the truest realm—and Mog-Lathar, guardian of eternal vision, is its rightful god. Their rituals involve sleep-deprivation, drug-induced trance states, and dream-offering sacrifices.

Those granted Mog-Lathar’s favor (often dreamwalkers and alchemists) receive immortality—free from hunger, breath, and aging—but their bodies become subtly inhuman, with whispering eyes and residual spider features.


## Current Events


## History


### ⚪ Tier 1: Surface-Level Rumors (Easy to Obtain)

**Sources:**

- Tavern talk in The Shingles
    
- Addicts muttering in Fever Dream Alley
    
- Superstitious coinboys and lucid sleepers
    
- Failed shiver detox patients
    

**Revealed Info:**

- "There’s a cult that worships the spiders in the forest."
    
- "Some people take shiver and never wake up the same."
    
- "Eyes in the dark. Eyes that don’t close. They’re always watching in the dream."
    
- "Once you stop shiverin’, the spiders come for you."
    
- "They say there’s a _web beneath the city_, and it pulls you in."
    

**Accuracy:** Partial truths mixed with street myths and hallucination-fueled babble.

---

### 🟡 Tier 2: Informed Whispers (Moderate DC to Uncover)

**Sources:**

- Veil of Shadows agents (with successful Diplomacy/Bribery/Contacts)
    
- Barvasi’s runners (under interrogation or influence)
    
- A priest at the **Sanctum of the Final Veil** who's noticed dream-tainted deaths
    
- Lore books on forbidden cults or nightmares (e.g., in the Astrum Archives)
    

**Revealed Info:**

- “There’s a group funding the shiver flood in Ilayas. Not just smugglers—zealots.”
    
- “They believe the spider dreams grant you immortality if you surrender yourself.”
    
- “One of their high-ranking members was once a Teseon-trained physician—Lombroso.”
    
- “They worship a fossil found in the Wynsend crater. Say it speaks in dreams.”
    
- “They’ve made some kind of _deal_—their top priests don’t eat, sleep, or age anymore.”
    

**Accuracy:** Stronger leads, but still distorted by secrecy and fear. Some reports confuse the cult with the Jade Gate or other planar factions.

---

### 🔴 Tier 3: Firsthand Accounts (Hard to Access, Dangerous to Acquire)

**Sources:**

- Capturing or questioning Frell Tann or another lucid sleeper
    
- Infiltrating the cult’s rituals via dreamwalking or shiver use
    
- Exploring Mog-Lathar’s fossil site in the **crater deep in Wynsend Forest**
    
- Recovering Myra Lombroso’s lost journal
    
- Succeeding on a high-level **Occultism**, **Religion**, or **Dream Lore** check
    

**Revealed Info:**

- The cult calls itself **the Brotherhood of the Spider** and answers to a being named **Mog-Lathar**.
    
- Mog-Lathar is a **fossilized Leng spider** idol, capable of granting immortality through dreams.
    
- The Brotherhood uses **shiver** not just as a drug but as a **rite of passage**—it allows them to walk the dream realm, evade detection, and conduct ceremonies in lucid reality overlays.
    
- The Brotherhood’s inner circle are no longer truly mortal. They **feed the dream**, sometimes through human sacrifice, but more often by spreading despair.
    
- Their ultimate goal is to _awaken Mog-Lathar fully_—not just as an idol, but as a **god** who will consume the Dream Dimension and rewrite reality.
    

**Accuracy:** This is the truth. It will either terrify the party or challenge their moral boundaries—especially if dreamwalking grants power or insight.


### [[Alinya Vilicus]] - Dreamwalking


## Notes



