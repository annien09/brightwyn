---
tags:
  - Quest
art: z_Assets/People/Krel.jpg
NPC:
  - "[[Krel Ianven]]"
  - "[[Alinya Vilicus]]"
  - "[[The Gatekeeper]]"
status: ✅
adventure: "[[Aelwynn]]"
whichparty: "[[Party]]"
quicknote: Aelwynn asked Alinya to scry on his brother
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
> A script for the GM to read when the party arrive to this location for the first time.

> [!metadata|characters]+ Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(quest, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC


## Overview

### Ritual Preparations
In the dimly lit chamber, Alinya meticulously prepares for the scrying ritual, her movements deliberate and precise. With a solemn air, she gathers the necessary components upon a polished wooden table, arranging them with care. Arcane reagents and carefully selected herbs, while Isiril lights fragrant incense that fills the room with a faint, lingering scent as Alinya works.

Once the space is cleansed and purified, Alinya focuses her intent, closing her eyes to center herself. She breathes deeply, drawing upon her inner reservoir of magical energy and attuning it to the task at hand. With practiced hands, she reaches out to receive the piece of clothing/item provided, a tangible link to the subject of the scrying—Krel.

A cloak, dark as midnight, is offered—a garment worn by Krel, its fabric imbued with traces of his essence. Alinya accepts it reverently, recognizing its significance in establishing the sympathetic connection required for the spell. With a nod of acknowledgment, she drapes the cloak/lays the item over/on the table, positioning it within the circle of candles and symbols that adorn the ritual space.

With preparations complete, Alinya focuses the scrying mirror in the middle of the table—a polished surface of obsidian set within an ornate frame. She gazes into its depths, her reflection staring back at her with a knowing intensity. Taking a deep breath, she channels her magic, her fingertips tracing patterns of arcane energy along the mirror's edge.

She starts to speak an incantation:

>[!read out loud]+
>"Ex umbram et aetheria, lux et tenebrae,  (From shadow and ether, light and darkness)
>Spiritus aeternum, adeste nobiscum.  (Eternal spirits, be with us.)
>Per astra et obscurum, per viam astralem,  (Through the stars and the void, through the astral path,)
>Pharasma revelare secreta, veritatem ostendere." (Pharasma reveal the secrets, show forth the truth.)

As the incantation is finished, the mirror shimmers with ethereal light, the surface rippling like the surface of a pond disturbed by a stone. Visions begin to coalesce within its depths, swirling and shifting as they take form—glimpses of Krel's whereabouts and activities, revealed to those gathered around.

Alinya's brow furrows in concentration as she maintains the connection, her focus unyielding despite the strain of channeling such potent magic. She peers into the mirror, and you with her.
#### Failing 
As Alinya concentrates on the spell, she furrows her brow and feels a subtle resistance, like trying to push against an immovable barrier. Despite her best efforts, Krel's willpower proves too strong, thwarting her attempt to peer into his whereabouts and activities.

The scrying mirror, which started to shape into a shimmering portal into Krel's world, returns to its original opaque state, its surface devoid of any images or visions. 

The room falls silent, the candles flickering faintly as Alinya's concentration wavers. She attempts to redouble her efforts, channeling more magical energy into the spell in a desperate bid to breach Krel's defenses. However, if he continues to resist, the scrying mirror remains stubbornly unyielding, its surface reflecting only the mage's own frustrated gaze.


### Scrying 
As Alinya focuses her magic on scrying on Krel, the image begins to coalesce in the scrying mirror, revealing a dimly lit chamber adorned with arcane symbols etched into the walls. You see a figure standing at the center, his demeanor tense and determined. Across from him, cloaked in shadows, stands the enigmatic figure (Gatekeeper). Their presence exudes an aura of mystery, their form obscured by a billowing cloak and a mask concealing their features. Only the faint glint of their eyes hints at any semblance of humanity beneath the mask. [perception: on the clothes they are wearing there’s a symbol, one that you recognize as the symbol of the Jade Gate. It’s dark colour on black cloak so you can barely make it up]

 - A voice echoes through the chamber, a voice that Aelwynn recognizes as Krel’s voice, but it has a hint of something foreign in the tone. You all hear a mixture of desperation and conviction in the voice as speaks: "I've done everything you've asked, (Gatekeeper). What do you need next?"

- The masked figure's response is measured, each word laden with calculated intent. “Good. Rest now and regain your power. I will have much need of you soon.”

- There’s a longer moment of silence, before Krel's voice breaks the silence: "Are all the relics in place, then? Have we secured the threads necessary for the upcoming convergence?"

- The response he receives is cryptic, each word laden with hidden meaning. "The relics have been placed with care. We have operatives posted to ensure they stay untouched."

- Krel nods, a flicker of relief crossing his features. "And what of the Lady? Is she prepared for the ritual? Her condition worsens with each passing day."

- A low murmur emanates from beneath the mask, carrying a sense of foreboding. "The Lady's fate hangs in the balance, but we cannot lose hope.”

- Krel nods, his brow furrowing with determination. " Will her pregnancy come to fruition as planned?"

- It takes the masked figure a moment to answer, but when they do, their voice is tinged with solemnity. "The Lady is prepared to give all for our cause, but her safety is paramount until she come to term. The sire of the offspring sees value in her continued well-being. We must ensure she remains protected until the time is right."

- Krel's gaze hardens, a hint of defiance in his voice. "We cannot afford to falter now! The Prince of Undeath's influence wanes with each passing moment. We must seize this opportunity before it slips through our grasp."

- A subtle nod from the Gatekeeper, their eyes gleaming with hidden knowledge. "Rest assured, Krel. Our allies in the shadows move with purpose, their machinations aligning with our own. I’m certain that they’ll hold their end of the deal."

- “Then have we made progress in locating the other vessels? Are the other four within our grasp?"

- The masked figure’s response is measured, their tone betraying a hint of uncertainty. "The search continues. Our agents scour the realms for signs of their presence, but the vessels remain elusive. Patience is paramount, for their acquisition is key to our success."

- A contemplative silence lingers between them before Krel speaks again, his mind already turning to the next step in their agenda. "And the other vessel? Do we have leads on their whereabouts?"

- The Gatekeeper nods, a glimmer of anticipation in their eyes. "Indeed, Krel. The bard known as Harlow the Uninspired may hold the key to Jubilex's vessel. You can join the search or leave it to the others. But rest assured, they shall be found, and our plans shall come to fruition."

With that cryptic assurance, the scrying fades, leaving you all to ponder the implications of everything that you’ve witnessed. 

As the scrying draws to a close, Alinya gently releases the magic, allowing the mirror's surface to return to its natural state. The room falls silent once more, the lingering echoes of the ritual fading into the ether.

With the scrying complete, Alinya takes a moment to collect herself, her expression thoughtful as she reflects upon the insights gleaned from the ritual.

As whispers of dark alliances and clandestine machinations echo in the recesses of the mind, the true extent of their ambitions begins to take shape, shrouded in the shadows of deceit and treachery.
### Aftermath

## Scenes & Actors
### Characters


### Creatures



### Locations



### Random Encounters



## Notes