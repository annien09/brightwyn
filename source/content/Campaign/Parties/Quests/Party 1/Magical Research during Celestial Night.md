---
tags:
  - Quest
art: z_Assets/Misc/Moonwort.webp
aliases:
  - Picking Flowers
status: ✅
adventure: "[[Ilayas Job Board]]"
location:
  - "[[The Lunar Radiance Inn]]"
  - "[[Ilayas]]"
NPC:
  - "[[Alinya Vilicus]]"
  - "[[Isiril Adren]]"
whichparty: "[[Party]]"
quicknote: Picking Flower Quest
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
> [[Alinya Vilicus]] is on a visit to [[Ilayas]] for a couple of weeks and staying for the upcoming Celestial Night Festival, including attending the Celestial Ball party. She needs help with research material.

> [!metadata|characters]+ Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(quest, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview
### Conflict Resolution within the Council

Given her wisdom and alignment with neutrality and compassion, Alinya is on a mission to mediate disputes and offer counsel on contentious matters between factions within Ilayas. Her diplomatic skills and adherence to fairness might aid in resolving conflicts amicably.

### Magical Research on the Celestial Night Festival

This year’s occurrence of the festival during a full moon holds significant implications for magical research, particularly for Alinya's investigation into Fate and divine magic in alignment with celestial events and plant alignments.

#### Plant Alignments and Lunar Influence

Around the Angel Day festival, the alignment of celestial bodies influences the natural world, including plant life. Certain plants are believed to respond to lunar phases, blooming, growing, or exhibiting heightened magical properties during specific celestial alignments.

#### Observational Studies

Alinya could observe the behavior, growth patterns, or magical resonance of these plants during the full moon, documenting any observable changes. She might investigate if these plants exhibit heightened responses during rituals related to divination or attempts to unravel Fate's threads.

#### Comparative Studies

Alinya might compare the effects of these lunar-aligned plants during the full moon with their behavior during other lunar phases. This comparative analysis could shed light on how celestial alignments, particularly the full moon, impact the magical properties or influences of these plants in relation to Fate-focused rituals or divine magic.

#### Moonwort

Moonwort is a legendary herb steeped in mystical lore, believed to possess magical properties associated with the moon's phases. In various myths and legends, moonwort is said to have properties that allow it to interact with celestial energies, particularly those of the moon.

Moonwort is a delicate, fern-like plant with pale, silver-hued leaves that shimmer in moonlight. The plant only blossoms or grows during certain lunar phases, typically during the full moon or when touched by moonbeams.

Moonwort is associated with enhancing magical abilities or facilitating access to mystical realms. It's rumored to aid in divination, dreamwork, or rituals that seek to harness lunar energies.

#### Angel's Trumpets (also known as Brugmansia)

Astral Projection Aid: Consuming extracts or infusions made from Angel's trumpets might aid in astral projection or out-of-body experiences. During the Celestial Night, the veil between realms might thin, allowing those using astral projection magic near these flowers to traverse planes more easily or access higher realms of consciousness.

Dream Magic: Angel's trumpets are believed to enhance dreams and visions. Ingesting or being near these flowers during the Celestial Night might induce vivid and prophetic dreams. Individuals might experience heightened intuition or receive cryptic messages through dreams when in proximity to these blooms.

#### Job Board
Due to the busy schedules of both Alinya and [[Isiril Adren]] , they have created a job announcement for the procurement of the flowers for research.
**Seeking Adventurers for Herbal Quest!**

**Description:** Embark on a magical quest to procure samples of the elusive Moonwort and mystical Angel's Trumpet! These rare plants are crucial for research on the upcoming celestial event and require skilled adventurers to gather them in their entirety.

**Task at Hand:** Retrieve samples of Moonwort and Angel's Trumpet, including their roots for replanting and freshly picked flowers. The bounty of these magical herbs is needed to prepare for the Celestial Night astrology event.

**Deadline for Completion:** The quest must be completed by the 28th of Desnus. Time is of the essence, and the timely return of these mystical botanical samples is crucial.

**Quantity Needed:**

- Moonwort: 8 complete sets (roots and flowers)
- Angel's Trumpet: 5 complete sets (roots and flowers)

**Reward:** Generous compensation of 75gp for Moonwort samples and an additional 75gp for Angel's Trumpet samples awaits the successful adventurers who procure the plants.


**Further Contact:** Interested adventurers can inquire at [[The Lunar Radiance Inn]].

## Journey
As the players approach the forest's edge, a tangible shift occurs in the atmosphere. The sounds of civilization fade into the background, replaced by the symphony of nature's melody. Towering sentinels of wood stand sentinel on either side, their leaves forming a verdant canopy overhead, filtering sunlight into scattered beams that dance upon the forest floor.

At the threshold of the forest, a sense of reverence washes over them, as if they are stepping into a realm both ancient and sacred. The air feels crisp and invigorating, carrying with it the earthy scent of moss and loam, intermingled with the delicate perfume of wildflowers. Each inhalation fills their lungs with the essence of the wilderness, awakening a primal connection to the natural world.

Before them stretches a tapestry of greens, with foliage of every hue blanketing the forest floor. Shafts of sunlight pierce through the canopy above, casting long shadows that shift and sway with the gentle breeze. The ground beneath their feet is soft yet firm, cushioned by a layer of fallen leaves and pine needles, each step a symphony of crunching and rustling.

As they cross the threshold into the forest's embrace, a hushed silence descends, broken only by the occasional chirp of a hidden bird or the rustle of a small creature scurrying through the underbrush. It's as if the very forest itself is holding its breath, awaiting their next move with bated anticipation.

Despite the serenity of their surroundings, there's an undeniable sense of mystery lingering in the air, an unspoken invitation to explore the hidden depths of the forest and uncover its secrets. And so, with hearts filled with curiosity and determination, the players step forward, their journey into the heart of the wilderness just beginning.

### Finding the Glade
The woods occasionally morph into surreal displays—trees that seem to sway in a dance despite the absence of wind, phantom lights that flicker in the distance, and mirages of creatures that vanish upon closer inspection.

Emerging from the shadows of the towering trees, they stumble upon an unassuming glade bathed in soft sunlight. In the center, a weathered campfire pit lies dormant, its stones worn smooth by the passage of time. Nearby, amidst a cluster of bushes, they spot the sought-after Moonwort plant, its delicate leaves shimmering in the gentle breeze.
Excited by their discovery, the players move closer, their eyes fixed on the prize they've been searching for. But just as they reach out to harvest the precious herb, a sudden movement catches their eye. Two towering trees, their gnarled branches twisted into cruel, scythe-like blades, emerge from the surrounding foliage with surprising speed.

Caught off guard by the unexpected threat, the players find themselves face to face with the dreaded scythe trees. Their jagged limbs poised menacingly, the trees exude an aura of primal aggression, their intent clear: to defend their territory at any cost.

## Notes