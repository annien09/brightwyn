---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Locations/Arcanamirium.webp
poitype:
  - Mage Tower
location:
  - "[[Teseon]]"
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
> The Arcanamirium is not only the largest and oldest school in Teseon, but quite possibly the most prestigious arcane magic academy in the entire continent of Ailira.

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
### Structure

The school is overseen by the First Spell Lord, **Archdean Darchana of House Madinani**, who also holds one of the lesser seats on the Council of Nine. A strict hierarchy within the student body ensures that pupils are not only divided by ability and experience, but that apprentices serve journeymen in their efforts to learn as well as pay the often steep tuition. (Ranks: Novice, Apprentice, Acolyte, Mage, Master of Arcane, Grand Master of the Arcane(incld Archdean), Archmage)

Every tenured teaching spellcaster employed by the school is allowed to sponsor one student each year. These students are given basic living quarters and secondhand equipment, but they receive their education free of charge. Similarly, traveling members of the school faculty have been known to pay (up front) for the education of a particularly promising student found abroad.

Archdean Lady Darchana personally grants her annual scholarship to students who demonstrate a talent in teleportation.

### Academics

Admission to the Arcanamirium is a multistep process beginning with an annual open exam. Applicants journey from all across Brightwyn to partake in this test, which not only proves their mettle as an arcanist but also ranks them as a Novice, Apprentice or Acolyte. Arcanamirium docents (teaching staff immediately below professorial rank) occasionally travel to other cities to scout for and recruit arcane talent to the school, but regardless of how one gains entry into the university, magical talent is an absolute requirement.

Unlike many comparable arcane institutions, the Arcanamirium promotes universal study over specialization, shying further from the schools of illusion and necromancy than the other schools. Any form of magic is also encouraged, and students who have the inclination are supported in mixing magic with martial skills, stealth, divine rituals, and even mundane talents, resulting in a student body well-versed in "practical magic," the ability to use spells and magic tools to accomplish direct, measurable results in the material world.

Classes are arranged toward goals rather than theoretical concepts, with programs including Artifice and Enchantment, Battle Magic, Fabrication, Magical Theory, Magical Transportation, Performance Magic, and Relic Studies. The Arcanamirium is also known for its dueling fields, at which many students hone their magical combat abilities.

### Arcanists

Several members of the Arcanamirium are arcanists, who blend the techniques of wizards and sorcerers. One professor is believed to be an arcanist, and Lady Darchana holds that arcanists and wizards should work together more, in order to help commoditize their magic and explore its effects on society.

### Alumni

Grandmage Alinya Villicus, Archamage Devati Vilicus, Lady Isolde Ravenshrew, etc.

## Current Events


## History
The Arcanamirium was established by the Arclords of Nex not long after they had formed a power block to fill the void left by their departed lord Nex. In the centuries since, it has become a mainstay of the city's Wise Quarter and one of the most influential non-governmental bodies in all of Teseon.

## Notes

