---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/The Red Door.webp
aliases:
  - Red Door
poitype:
  - Temple
dominion:
  - "[[Veil of Shadows]]"
owner:
  - "[[Elandra Nightshade]]"
organization:
  - "[[Veil of Shadows]]"
location:
  - "[[Ilayas]]"
  - "[[The Port District]]"
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
>> **Pronounced** |  `INPUT[textArea:pronounced]`
>> **Aliases** | `INPUT[list:aliases]` |
>> **Type** | `INPUT[POIType][inlineListSuggester:poitype]` |
>> **Dominion** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):dominion]` |
>> **Owners** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):owner]` |
>> **Assistant** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):assistant]` |
>> **Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{poitype}][text]` |
> **Dominion** | `VIEW[{dominion}][link]` |
> **Owners** | `VIEW[{owner}][link]` |
> **Assistant** | `VIEW[{assistant}][link]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>


> [!recite]+ Introduction
> The Red Door - Temple of Passion and Pleasure in the Port District
Nestled discreetly within the vibrant tapestry of Ilayas' Port District, The Red Door stands as a unique establishment that seamlessly merges the worlds of passion and spirituality. More than just a brothel, it is also a Temple of Calistria, the Pathfinder goddess of lust, revenge, and trickery.

> [!metadata|map]- Map
> ```leaflet
> id: TBD
> image: [[PlaceholderImage.png]]
> height: 600px
> width: 640px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 2
> zoomDelta: 0.5
> unit: meters
> scale: 1
> darkMode: false
> ```

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "POI")
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview 
### Exterior

The Red Door's exterior is a study in subtle opulence. A crimson-hued door, adorned with ornate carvings and gold trim, marks the entrance. A discreet sign, featuring the symbol of a wasp, hints at the clandestine delights that await within.

### Entryway

As visitors pass through The Red Door, they are enveloped in a sensual ambiance. Dimly lit lanterns cast a warm glow over richly draped curtains, creating an air of mystery and allure.

### Temple Atrium

The main atrium, adorned with tapestries depicting scenes of passion and joy, serves a dual purpose. It is a sanctuary for worshipers of Calistria seeking spiritual fulfillment and a haven for those seeking earthly pleasures.

### Chambers of Ecstasy

Private chambers, elegantly appointed with luxurious furnishings, offer a range of experiences tailored to individual desires. Skilled courtesans, chosen for their artistry and empathy, provide companionship that transcends the mundane.

### Sacred Pool

At the heart of The Red Door lies a sacred pool, its waters adorned with floating candles and fragrant petals. Devotees of Calistria often partake in rituals of purification and rejuvenation, embracing the dual aspects of pleasure and spiritual release.

### Shrouded Altar

Tucked away in a discreet alcove, a shrouded altar is dedicated to the goddess Calistria. Devotees and courtesans alike pay homage, and those seeking revenge may whisper their desires to the goddess in the quiet moments of reflection.

### Apothecary Corner

Adjacent to the main atrium, an apothecary corner offers exotic oils, perfumes, and potions said to enhance the senses. These carefully crafted concoctions are available for purchase, allowing patrons to carry a hint of The Red Door's allure with them.

### The Mistress of Revels

At the helm of The Red Door is [[Elandra Nightshade|the Mistress of Revels]], a charismatic and enigmatic figure known for her discretion and wisdom. She ensures that the delicate balance between spiritual reverence and sensual indulgence is maintained.

### Harborside Balcony

An intimate balcony overlooking the harbor provides patrons with a breathtaking view of the city's bustling waterfront. It serves as a sanctuary for quiet reflection or shared moments under the moonlit sky.

## Regulations
Guests are reminded that within The Red Door, consent, respect, and discretion are paramount. The Temple of Calistria's teachings emphasize the freedom to explore one's desires within a safe and consensual environment.

The Red Door is a haven where the divine and the carnal coalesce, offering a sanctuary for both spiritual seekers and those in pursuit of earthly delights along the shores of Ilayas' Port District.

## Events
Periodically, The Red Door hosts various events.

### Divine Entertainments Night
What: skilled performers and musicians take the stage to celebrate the arts (kink), pleasure, and the divine mysteries of Calistria.
Price Range: 10 to 30 gold pieces per person, inclusive of performances, beverages, and light refreshments.

### Sacred Pool Ritual
What:
Price Range: 15 to 40 gold pieces for a private session.

### Rituals of Devotion
What:
Price Range: Varies based on the complexity and personalization of the ritual; starting from 50 gold pieces.

# Services
## The Chambers of Ecstasy
Tucked away within the veiled corridors of The Red Door, the Chambers of Ecstasy are private sanctuaries designed to cater to the diverse desires of its patrons seeking a diverse array of sensual experiences. These elegantly appointed chambers are adorned with luxurious furnishings, draperies in rich hues, and strategically placed candles casting a soft, flickering glow. The air is scented with exotic fragrances, creating an atmosphere of intimacy and indulgence.

Price Range: 20 to 200 gold pieces, depending on the service, the level of intimacy and duration.

### Private Companionship

Description: A dedicated companion provides undivided attention and companionship for the duration of the visit.

Price: 20 to 50 gold pieces, depending on the chosen companion and the duration.

### Couples' Rendezvous

Description: Tailored experiences for couples seeking to explore and deepen their connection within the privacy of the Chambers.

Price: 40 to 80 gold pieces, depending on the level of customization and duration.

### Exotic Massages

Description: Skilled masseuses and masseurs offer sensual massages using aromatic oils and techniques designed to heighten pleasure.

Price: 30 to 60 gold pieces, depending on the chosen therapist and duration

### Art of Seduction Lessons

Description: Experienced instructors guide patrons through the nuances of the art of seduction, enhancing their interpersonal skills.

Price: 50 gold pieces for a private session.

### Fantasy Exploration

Description: Patrons can request the realization of specific fantasies in a safe and consensual environment, with carefully selected companions.

Price: 50 to 100 gold pieces, depending on the complexity and duration.

### Extended Intimacy Retreats

Description: Overnight or extended stay packages for those seeking prolonged connection.*

Price: 100 to 200 gold pieces, inclusive of accommodations and personalized services.

### Female Companions

Seraphina: A sultry elven enchantress with a penchant for storytelling and a gentle touch.

Sylveas: A vivacious human dancer, known for her captivating performances and grace.

Lyria: A skilled tiefling masseuse who specializes in exotic massage techniques.

Mirabelle: A half-elven artist, offering companionship and artistic exploration.

### Male Companions

Thorne: A charismatic human companion with a talent for conversation and making patrons feel at ease.

Eirik: Adwarven escort known for his sense of humor and unwavering discretion.

Caelum: An elven musician and poet, bringing an air of refinement and creativity to the chamber.

Dorian: A charming tiefling companion, well-versed in the art of seduction and attentive to patrons' desires.

The Red Door emphasizes choice and consent, and patrons are encouraged to communicate their preferences openly to ensure a satisfying and comfortable experience.


## Veil of Shadows

### Whispered Rumors

Price Range: 10 to 30 gold pieces for basic information.

### Insights into Noble Houses

Price Range: 30 to 80 gold pieces, depending on the depth and sensitivity of the information.

### City Intrigues and Affairs

Price Range: 20 to 60 gold pieces, with additional fees for particularly sensitive or high-risk inquiries.

### Veil of Shadows Membership

Price Range: 100 gold pieces or more for exclusive access to ongoing information and updates.

## Hidden Details - SECRETS
### Jade Gate

>[REDACTED]
### House Veridane

>[REDACTED]



## Notes

