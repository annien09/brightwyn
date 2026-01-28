---
tags:
  - Quest
art: z_Assets/Locations/Portals.jpg
whichparty: "[[Party]]"
adventure: "[[Unleash the Planes]]"
status: ✅
location:
  - "[[Ilayas]]"
quicknote: Quest leading to Rifts
NPC:
  - "[[Elenor Vale]]"
aliases:
  - Opening the Rifts
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
> A low, incessant hum emerged 5 days ago (20 Desnus), stirring whispers among the townsfolk. At first, it was dismissed as the wind whistling through the thickets or the echoes of some natural phenomenon. But as days passed, the hum grew in intensity and persistence, resonating like a haunting. Additionally, 1-2 days after the hum started, there have been disappearances in the outskirts of the City.

> [!metadata|characters]+ Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(quest, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC


## About

No one could pinpoint its origin. Some claimed it came from the heart of the [[Wynsend Forest]] , while others insisted it echoed from the outskirts of the city. As the hum persisted, odd occurrences began to manifest. People vanished without a trace, leaving behind only fragmented memories and a sense of unease among those who knew them. Each disappearance seemed connected to the strange hum, as witnesses recalled the sound intensifying moments before someone vanished into thin air. Some claimed it was a vengeful spirit seeking retribution for ancient wrongs, while others spoke of a rift between realms causing individuals to slip into an alternate reality.

**Duchess Leonora Emberwood** - the Councilman charged with the Protection of Wynsend Forest, has sanctioned a quest to investigate the strange occurrence after a team of researchers with the help of a local druid who is familiar with the landscape could not find the source. Sir Percival Berrenard - Commander of the City Watch, has increased the guards activity around the outskirts of the town to try and thwart the disappearances. 

We've had a few independent applicants, but our main two guild which would be charged with such thing, their members who would be capable of taking such an endeavor are currently occupied. The adventurer's guild (called The Guild of Valiant Explorers) has it's members busy with hunting a beast (a black dragon), and the Pathfinder Society does what the society usually does and their members are on various endeavors to look for artifacts and whatnot. 

**Speaking with folks on the outskirts they are taken to Selara** NPC names - Gerrard, Notti, Ryleigh

Gerrard is looking for his mother - Rosetta - describes an old woman with long white hair, 5'4", she liked to carry a basket with fruit and freshly cooked pastries for the children running around.

## The Tale of the Fey Weaver's Lament

Long ago, nestled within the heart of the Wynsend Forest there existed a realm where the boundaries between the mundane and the ethereal were thin. It was said that within this mystical realm lived the Fey Weaver, a being of immense power and wisdom, who spun the threads of magic that wove through the forest.

The Fey Weaver's songs echoed through the trees, enchanting the creatures of the woods and nurturing the vibrant life that thrived within. Their melodies were whispered secrets, known only to the most attuned spirits and the chosen few who communed with nature's essence.

However, an insidious darkness began to encroach upon the realm. A malevolent force sought to subvert the Fey Weaver's melodies, corrupting the harmonious symphony that sustained the balance between realms. The once-peaceful songs turned discordant, and the forest echoed with a haunting hum—a lament that foretold of impending imbalance.

Desperate to restore harmony, the Fey Weaver embarked on a quest to seek ancient artifacts hidden within the Wynsend Forest. But as the darkness grew stronger, the realm twisted, and the boundaries between realities became frayed. Legends tell of the Fey Weaver's disappearance, leaving behind an echo of sorrow that manifested as the haunting hum heard throughout the woods.

Some say the Fey Weaver's essence lingers, trapped within the heart of the forest, seeking brave souls to aid in restoring the lost melodies and quelling the discordant hum that reverberates through the woods and that they are now behind the abductions.

## Speaking with a Druid - Selara Norter
Druids are attuned to the natural energies of the land. They might sense disruptions in the ley lines or magical flows, expressing concerns about an unnatural disturbance affecting the forest's lifeforce. They could hint at a growing imbalance or an aberrant energy source.

Selara is a venerable Druid who has spent a lifetime attuning herself to the rhythms and energies of the Wynsend Forest. Her wrinkled visage and gnarled staff are a testament to her deep connection with nature, and she is revered among the locals for her wisdom and insight.

When approached by the party, Selara nods gently, her piercing green eyes shimmering with an ancient wisdom. As the party inquires about the strange hum and the energetic disturbances, she settles herself on a moss-covered stone, surrounded by a circle of vibrant wildflowers.

	"The balance of nature," Selara begins, her voice carrying the weight of centuries, "is a delicate song—a symphony woven by the ley lines that pulse beneath our feet. But these recent disturbances... they're not merely a disruption, they're a discordant note in nature's melody."

With a gentle wave of her hand, Selara gestures toward the Wynsend Forest.

	"Can you feel it?" she asks, her eyes closed in deep concentration. "The ley lines, once tranquil and harmonious, now ripple with erratic energy. It's as if the very threads that bind this land are fraying, caught in a chaotic whirlwind."

She opens her eyes, fixing them upon the party with a knowing gaze.

	"Such shifts in the ley lines aren't mere happenstance. It speaks of a disturbance rooted deep within the woods—a disruption that not only affects our realm but echoes through the ethereal planes. There's a nexus, a convergence of these lines, where the energies are in turmoil. It's there that you'll find the heart of this discord."

Selara's weathered fingers trace invisible patterns in the air, as if following the unseen paths of the ley lines.

	"Be wary," she cautions. "As you venture closer to this nexus, the lines between realities might blur. The boundaries that separate our world from others grow thin. The forest's whispers might grow louder, and visions of past and future may entwine. But in this chaos lies the key to restoring the balance—a relic, perhaps, or a forgotten ritual that once bound these energies."

She leans forward, her voice barely above a whisper, yet carrying an unwavering certainty.

	"Seek the heart of the convergence, for there, amidst the swirling energies, lies the source of our strife and the hope for our salvation."
"Deeper into the forest where the mist shrouds the ancient oaks, lies the entrance to the Path of Serenity," Elara instructs, her voice carrying an otherworldly resonance. "Follow the luminescent lilies that line the pathway—they shall guide you through the twilight-dappled grove."

She describes a route that meanders through the dense foliage, a path often overlooked by those unfamiliar with the forest's secrets. The party must navigate through patches of shifting illusions, where reality bends and mirrors play tricks on the eye.

"Stay vigilant," she advises, her gaze fixed on the party with unwavering intensity. "The woods are alive with enchantments, and the boundary between what is and what seems may blur. Trust your instincts, for the forest listens to the whispers of your hearts."



## Location
1. **Luminescent Flora**: The forest is adorned with flora that glows softly, emitting hues of ethereal blues, greens, and purples. Flowers, vines, and fungi seem to shimmer with an otherworldly radiance, guiding the party along the path.
    
2. **Shifting Illusions**: The woods occasionally morph into surreal displays—trees that seem to sway in a dance despite the absence of wind, phantom lights that flicker in the distance, and mirages of creatures that vanish upon closer inspection.
    
3. **Twilight Canopy**: The sunlight filters through the dense foliage, creating a soft, dappled glow that bathes the forest in a perpetual twilight. Shadows play tricks, elongating and contorting in strange, almost sentient patterns.
    
4. **Arcane Runes and Symbols**: As they draw nearer to ley line convergence points, faint arcane symbols and sigils etched into tree trunks or scattered along the ground become more prevalent, pulsating with latent magical energy.
    

### Auditory Experience:

1. **Whispers on the Breeze**: Faint whispers and murmurs drift through the air, carrying echoes of ancient languages or fragments of conversations. They seem to offer cryptic guidance or warnings, guiding the party or leading them astray.
    
2. **Melodic Hum of Magic**: The pervasive, gentle hum that the players have been tracking grows in intensity as they draw closer to the convergence points. It's a melodic, resonating sound that seems to harmonize with the pulse of the ley lines.
    
3. **Rustling Leaves and Echoing Steps**: The underbrush rustles with life—mysterious creatures, unseen to the eye, moving in tandem with the party's steps. Even their own footfalls echo differently, creating an eerie symphony of sounds.
    
4. **Temporal Echoes**: Occasional echoes of past events or distant laughter resonate through the forest, causing brief moments of disorientation as the players momentarily feel transported to another time or place.

## Journey
As the players gather their wits after the fierce encounter with the scythe trees, they sense a restless energy urging them forward.
1. **The Enchanted Clearing**: Their path leads them through a serene clearing, where shafts of sunlight pierce through the canopy above, casting a golden glow upon the forest floor. 
	In the enchanted clearing, the subtle enchantment manifests as a soft, ethereal glow that suffuses the air, imbuing everything it touches with a sense of tranquillity and wonder. As the players step into the clearing, they feel a gentle warmth wash over them, easing the tension in their muscles and calming their racing hearts.

	The light dances upon the vibrant foliage, painting the leaves in hues of shimmering gold and emerald green. Flowers of every colour dot the landscape, their petals unfurling in graceful arcs as if reaching towards the heavens. A gentle breeze carries the scent of wildflowers and fresh earth, mingling with the distant melodies of birdsong.

	Yet, beneath the surface of this idyllic scene lies a deeper magic, one that whispers of ancient secrets and untold mysteries. Those attuned to the natural world might sense the presence of the leylines energies lingering in the air, their subtle influence weaving through the very fabric of the forest.

	You follow the narrow trail that winds its way through the forest, bathed in the warm glow of sunlight filtering through the canopy above, until you reach a fork in the path, which splits into 2 directions. 
	A. To the left you see a cluster of ancient trees standing sentinel, their branches swaying gently in the breeze. The air around them seems to hum with a faint energy, as if the trees themselves are whispering secrets known only to the forest. The path appears overgrown and untamed.
	B. To the right, you spot a hidden path thatveers off into the underbrush, obscured from view by a thick tangle of foliage. The path appears less traveled than the others but you see branches of trees that were broken off and never grew back.
    
2. **The Whispering Woods**: As they journey deeper into the heart of the forest, the trees around them seem to come alive with murmurs and whispers. The very air vibrates with an otherworldly energy, as if the ancient spirits of the woods are speaking to them in hushed tones. Though the whispers grow louder with each passing moment, the players steel themselves against the eerie sensation, their determination unshaken as they continue their quest.
	The towering trunks of ancient oaks and slender birches loom overhead, their branches swaying gently in the breeze. Sunlight filters through the dense canopy above, casting shifting patterns of light and shadow upon the forest floor. The ground beneath their feet is soft with a thick carpet of moss and fallen leaves, muffling the sound of their footsteps as they tread deeper into the woods.

	[Arcana/Nature] As they progress, the whispers grow louder, filling the air with an eerie chorus of voices that seem to speak in a language older than time itself. Though the words are unintelligible, the players can sense a faint undercurrent of urgency and warning, as if the forest itself is trying to communicate some hidden truth.
	[Perception] Strange shapes flit between the trees, darting out of sight before they can be fully glimpsed. Shadows seem to dance and shift in the corner of their vision, leaving the players with a sense of unease that prickles at the edges of their consciousness.
### **The Forgotten Tomb**
As the players decide to venture down the hidden path leading to the glade, they find themselves immersed in a world of untamed beauty and mystery. The narrow trail winds its way through the dense underbrush, the foliage pressing in on all sides like curious onlookers eager to reveal their secrets.
	The forest seems to close in around them, the canopy overhead casting the path into shadow as shafts of sunlight filter through the dense foliage. The air is cool and damp, heavy with the scent of earth and moss, punctuated by the occasional chirp of hidden creatures and the rustle of leaves in the breeze.
	The path twists and turns unpredictably, leading the players deeper into the heart of the forest with each step. Roots protrude from the forest floor like gnarled fingers, threatening to trip the unwary traveler, while tangled vines hang from the trees like curtains drawn across the path.
	As they journey deeper into the forest, the players can't shake the feeling that they are being watched, as if unseen eyes are following their every move. Yet, with determination in their hearts and curiosity driving them forward, they continue along the hidden path and you start hearing running water, like the sounds of a small river or a creek. 
	As the players emerge from the dense undergrowth, they find themselves standing in the heart of the hidden glade, a place steeped in both beauty and mystery. Before them lie the remnants of a forgotten place in the world, reclaimed by nature and shrouded in the embrace of time.

1. **The Ancient Stones**: Massive stones rise from the forest floor, their weathered surfaces bearing the weight of centuries. Carved with intricate symbols and runes, hinting at the rituals and ceremonies that once took place within the glade.
    
2. **The Overgrown Statues**: Two statues stand sentinel at the edge of the clearing, their forms partially obscured by creeping vines and moss. One depicts a female mage, her outstretched hands crackling with arcane energy, while the other portrays a dwarven warrior, his axe raised in a defiant stance. Despite the passage of time, their features remain remarkably well-preserved, a testament to the craftsmanship of their creators.
    
3. **The Forgotten Tents**: As you approach, you also see remnants of forgotten tents, their fabric tattered and torn, their frames bent and broken. Nature has begun to reclaim these makeshift shelters, with vines and ivy snaking their way through the fabric and moss creeping up the weathered poles.
	As the players approach the skeleton lying amidst the forgotten tents, they can't help but feel a sense of solemnity wash over them. The figure is clad in weathered leather armor, its surface cracked and worn with age. A rusted axe lies nearby, its blade dulled by time and neglect. It's clear that this unfortunate soul met a tragic end in this secluded glade.
	As the players ponder the significance of the letter, their attention is drawn to a curious object lying beside the skeleton: a white marble funerary baton, its surface smooth and unblemished despite the passage of time. Upon closer inspection, they realize that the baton is more than just a simple piece of stone—it's a key of some sort, its intricate carvings hinting at a hidden purpose.

Upon closer inspection, the players discover a weathered backpack slung over the skeleton's shoulders. Inside, they find a collection of mundane items, including a few scraps of dried rations, a waterskin long emptied of its contents, and a tattered bedroll.

However, nestled within the inner pocket of the leather jacket, they uncover a fragile piece of parchment, its edges yellowed with age. Carefully unfolding it, they find themselves holding an old letter, its faded ink barely legible after years of exposure to the elements.
    
4. **The Stone Circle**: At the center of the glade lies a circle of weathered stones, their surfaces worn smooth by the passage of time. Eight pillars stand at intervals around the perimeter, their tops adorned with faded runes and symbols. Despite their age, the stones remain standing.
    As the players explore the weathered pillars surrounding the stone circle, their eyes catch sight of faded symbols and intricate carvings etched into the stone surfaces. Despite the ravages of time and the encroaching elements, the remnants of a family crest can be discerned, its once-proud design now obscured by cracks and weathering.
    The crest depicts a shield adorned with symbols of lineage and heritage, though many of the details have been worn away by centuries of exposure to the elements. Bits of ivy and moss cling to the crevices of the stone, further obscuring the intricate carvings and adding to the sense of mystery and intrigue.
    Though the crest remains partially hidden and fragmented, the players can still make out certain elements—a lion rampant, a fleur-de-lis, and a motto that reads: "For Honor, Valor, and the Eternal Flame". (House Adellas)
5. **The Tomb and Braziers**: In the center of the stone circle stands a solitary tomb, its stone surface worn and weathered by the elements. Three inactive braziers surround it, their flames long extinguished, yet their presence still casting a sense of solemnity and reverence over the scene. It's clear that this tomb holds significance, though its true purpose remains shrouded in mystery.
	As the players approach the solitary tomb at the center of the stone circle, their attention is drawn to the imposing figure of the coffin within. Carved from weathered stone and adorned with ancient symbols, the coffin bears the unmistakable emblem of a medusa—a fearsome creature with snakes for hair, its gaze said to turn any who meet its eyes to stone.
	The medusa symbol is intricately detailed, its serpentine form winding sinuously across the surface of the coffin. Though the passage of time has worn away some of its finer details, the emblem still retains an aura of malevolence and power.
	Upon closer inspection, the players notice something unusual about the mouth of the coffin. Set into the stone is a recessed indentation, shaped like a large keyhole. As they examine the keyhole more closely, the players realize that it's not just any ordinary lock—it's designed to accommodate a large, ornate key, perhaps one with a specific shape or design. An examination of the hole in the medusa’s mouth reveals that it seems to match the tip of the funerary baton (Tomb of the Iron Medusa). 

The iron carving radiates strong transmutation magic. If the PCs insert the funerary baton into the hole, a loud metallic “click” sounds and the metal covering the medusa’s eyes slides back, exposing eyes made of polished white marble, with painted black pupils glaring menacingly. By rotating the funerary baton, the PCs turn the eyes in their metal sockets. When the eyes are crossed, the medusa’s jaws gape open and a cold blue light shines forth. The creature that turned the baton and all other creatures within a 5-foot spread are lifted off their feet and sucked into the yawning mouth, shrinking and spiraling down to nothingness as the iron face seems to swallow the targets whole. Despite the dramatic appearance, this is a teleportation effect
that can be resisted with a DC 25 Will save.

Without a funerary baton, a character can activate one of these medusa heads with a DC 25 Use Magic Device check made as a full-round action.

>[!info]- Adellas Family
>The notorious Alonian aristocrats of House Adella died out nearly two hundred years ago. After rising to prominence during the crusade against the Whispering Tyrant, the Adellas were especially famous for their contributions to the Grand Campaign against the undead armies. Known to produce scions with extraordinary talent for swordplay and sorcery, the house grew in influence, wealth, and notoriety before collapsing under the weight of its own arrogance in the 46th century ar. The Adellas were so despised by the time of their demise that all public record of the family was stricken from imperial annals, and anyone tainted by its blood was stripped of aristocratic status.

>[!info]- Warding Magic
> As the players utilize their magical abilities to detect magic within the underground necropolis, they find themselves enveloped in a swirl of potent transmutation energies that permeate the very fabric of the complex. The air crackles with arcane power, and their senses are inundated with the subtle vibrations of magic that pulse and thrum through the surrounding stone and earth. The tomb and the entire necropolis radiates with a powerful aura of transmutation magic, warding area within from scrying and magical observation. This effect creates a shimmering barrier that shields the necropolis from prying eyes, rendering it invisible to divination spells and effects.

>[!info]- Stone Doors
>Stone Doors: All doors in the necropolis consist of large rectangular stones that bear no obvious method of opening. Each side of the doors bears a carved medusa head of varying design. If an open palm is placed against such a carving, the stone block descends into the ground over the course of a full round, after which passage through the portal is possible. These doors remain open for 5 minutes, after which the door slides shut in a single round. A
character who attempts to leap through a closing doorway must make a DC 15 Reflex save to do so successfully as part of a move action. A creature or object crushed by a door takes 10d6 points of bludgeoning damage—if this damage fails to kill or destroy the blockage, the door is propped open an appropriate amount. These doors have hardness 8, 300 hp, and can be broken down or forced open with a DC 40 Strength check. 
>[!info]- Grave
>Not all of the dead are buried in vaults or urns—many of the lesser servants or allies of the Adellas were instead buried in the hundreds of graves that
lie between the mausoleum buildings themselves. Most of these graves are marked by crumbling limestone or rotting wood—little can be gleaned from them. 

>[!info]- The Dead 
>The bodies of the Adellas and their servants fill the hundreds of stone sarcophagi or funeral urns found in the necropolis. Unless otherwise indicated, tampering with any of these bodies exposes the would-be grave-robber to  the Adella curse. Sarcophagus lids are mortared in place, and must be chiseled open (this takes 2d6 rounds of work with the proper tools). The sarcophagi contain skeletal remains, with a 20% chance of 4d6 gp worth of jewelry or other treasure. Funeral urns contain ashes and pulverized bones, but do not contain any objects of value. 

>[!info]- Illumination 
>Inside the actual necropolis (not simply the ruined echo of the site that exists in the real world), it is eternally night; a full moon in a cloudless, star-flooded sky provides the only illumination. Time still flows normally inside the necropolis—the sun simply never rises over this haunted realm.

#### Crematorium Entry
This dull gray granite building looms in the center of the necropolis. Its entrance has a domed ceiling that rises to a height of twenty feet, and is decorated with intricate geometric designs. In the center of the chamber’s floor, a carved medusa crest stares endlessly upward. To the north, a pair of stained-glass windows depicting a handsome man and a beautiful woman look on. A motto engraved around the circumference of the medusa engraving on the floor reads, “A Blade Answers Even the Most Vexing Question.” The antechamber to the north is empty—the stained-glass windows depict Aroden and Arazni as they appeared while they were human. 
#### Crematorium 
The walls of this domed and oval-shaped formal chamber are covered in complex geometric patterns of green and gold. It appears to be used for funerary rites, with marble tables to the north and south and two elaborate wheeled wooden biers at the center. To the east, the wall is made up of a huge iron oven with a closed door three feet square and two feet off the floor, with a shelf sticking out beneath it like the tongue of a huge, taunting beast.

As the players cautiously enter the crematorium room, they are met with a stifling wave of heat that washes over them, suffusing the chamber with an oppressive atmosphere. The air is thick with the scent of smoke and charred remains, and the dim light of flickering torches casts eerie shadows across the walls.

Suddenly, from the depths of the infernal oven at the center of the room, a rumbling growl reverberates through the chamber, followed by the sound of shifting earth and crackling flames. With a burst of fiery energy, three towering figures emerge from the flames, their forms wreathed in flickering fire and molten lava.

"Interlopers!" roars one of the elder fire elementals, its voice a guttural growl that echoes off the stone walls. "You dare trespass in our domain? Prepare to face the wrath of the flames!"

The other two elementals join in the chorus of aggression, their fiery eyes blazing with fury as they advance menacingly towards the players. With each step, the heat in the room intensifies, and the players can feel sweat beading on their brows as they prepare for battle.

Amidst the chaos and aggression of the fire elementals, a fourth figure emerges from the flames—a noble efreeti named Bebulec. His once-proud demeanor has been twisted by centuries of imprisonment, his eyes wild with madness as he lashes out at the players with a roar of frustration and rage.

"Foolish mortals!" he bellows, his voice tinged with madness. "You will pay for the sins of your ancestors! Prepare to face the fury of Bebulec the Unbound!"

With a ferocious roar, the fire elementals and Bebulec launch themselves at the players, their attacks fueled by centuries of pent-up anger and resentment. The chamber erupts into chaos as flames dance and flicker amidst the swirling melee, and the players find themselves locked in a desperate struggle for survival against the wrath of the imprisoned elementals.

### Getting Close
As the players stand on the precipice of the ley lines convergence, a palpable sense of anticipation fills the air. The boundaries between realities begin to blur, and the very fabric of the forest seems to warp and shift before their eyes.

1. **Ethereal Realm**: Ghostly wisps of mist drift through the trees, obscuring the familiar landscape and replacing it with an ethereal vision. Colors in the ethereal realm take on a muted, surreal quality. The vibrant greens of the foliage appear washed out, as if seen through a veil of mist, while the browns of the tree trunks and earthy terrain seem almost translucent, as if made of smoke. The sky above is a pale, ethereal blue, with wisps of shimmering clouds drifting lazily across the heavens. Shadows dance and flicker, their edges blurred as if caught between worlds. The air feels charged with arcane energy, tingling against the skin and leaving an ephemeral sensation in its wake.
	- **Skill Checks**: Players need to make Arcana or Occultism checks to attune themselves to the ethereal energies surrounding them, allowing them to perceive and interact with the ethereal realm and move through the plane.
	- **Transition**: - With a collective effort of willpower and concentration, the players feel a shift in the fabric of reality around them. The misty veil of the ethereal realm begins to dissipate, revealing the familiar sights and sounds of the material plane once more. But then it changes again.
    
2. **Fire Plane**: Suddenly, the air grows stiflingly hot as flames erupt from the earth, licking at the trees and casting an infernal light upon the surroundings. The forest is transformed into a fiery hellscape, with charred branches and smoldering embers littering the landscape. The players can feel the intense heat pressing against their skin, the crackling of flames echoing in their ears. 
	Despite the hostile environment, life stubbornly persists in the Fire Plane's forest. Strange and alien creatures roam amidst the charred ruins of trees, their forms adapted to withstand the intense heat and flames that engulf their surroundings. Fire elementals drift through the air like living embers, while salamanders and other fire-dwelling creatures stalk the fiery undergrowth in search of prey.
	The sounds of the forest are a cacophony of crackling flames and hissing steam, punctuated by the occasional roar of distant infernos and the screech of creatures adapted to thrive in the fiery depths.
	- **Skill Checks**: Occultism or Nature checks may be needed to attune themselves to the unique energies of the First World, allowing them to navigate the transition safely.
    - **Transition**: The intense heat of the Fire Plane begins to recede, replaced by a sense of weightlessness and euphoria. They feel as if they're being drawn towards a shimmering portal that flickers on the edge of their perception, beckoning them into the vibrant realms of the Feywild. 
    
3. **First World (Feywild)**: As quickly as the flames appeared, they are extinguished, replaced by a verdant, surreal landscape straight out of a faerie tale. The colors of the forest become vivid and exaggerated, with flowers blooming in hues unseen in the mortal realm. The air is filled with the melodious laughter of unseen fey creatures, their voices carrying on the wind like music. The players feel a sense of wonder and awe wash over them as they behold the beauty and magic of the Feywild.
	- **Skill Checks**: Survival or Occultism checks will be necessary to reorient themselves and navigate the transition back to the material plane.
	- **Transition**: - Drawing upon their inner reserves of strength and determination, they focus on their connection to the material plane, anchoring themselves in the reality of their surroundings. As they do, they feel a gentle tug at the edges of their consciousness, pulling them back towards the material plane. With a sense of anticipation and resolution, they step through the shimmering portal that marks the boundary between worlds, emerging once again amidst the familiar sights and sounds of the Wynsend forest.
    
4. **Luminescent Lilies**: Looking around them, the players catch sight of luminescent lilies dotting the forest floor, their petals glowing softly in shades of iridescent blue and silver. The flowers seem to pulse with a gentle radiance, casting an enchanting glow that illuminates the path ahead. Though they are small and delicate, the lilies exude an otherworldly beauty, hinting at the wonders that await in the heart of the ley lines convergence.

## Scenario: Ley Line Flux

**Description**: The party enters a clearing bathed in a soft, ethereal glow. They sense the convergence of ley lines nearby, marked by a series of arcane light illuminating the ground, which appears to be shimmering with faint light. As they approach, the ground begins to undulate, and the ground flares brightly in patterns of colours. There is fire erupting from the ground, ice forming in other areas while the ground bends and a green fog gathers in the holes formed. In some places, the time seems to slow - You move half your speed.

**Challenge**: The party must navigate through a series of ley line surges that cause the terrain to shift and change. The convergence point emits pulses of magical energy that alter the landscape unpredictably.

**Terrain Distortions**: The ground warps and shifts with each pulse of energy. The party needs to make quick decisions on where to step or risk falling into unstable terrain.
**Surge Waves**: Waves of magical energy pulse through the area periodically. Characters must make Reflex saves to avoid being knocked prone or pushed off unstable ground as the surges pass through.

**Resolution**: To overcome the ley line instabilities and reach the other side of the clearing, the party must navigate the shifting terrain while avoiding obstacles and disruptions caused by the surges. They might need to work together, using their skills and magic to stabilize the ground, decipher patterns, or time their movements to coincide with the moments of relative stability between surges.

Every round the areas on the ground glow in a certain colour
- 1 - Red - Players take 1d6 fire damage; the damage increases by a 1d6 every time they step on red during the same round
- 2 - Blue - Players take 1d6 cold damage; the damage increases by a 1d6 every time they step on red during the same round
- 3 - Purple - Players who step onto a purple light are slowed down.
- 4 - Green - Players take 1d6 acid damage; the damage increases by a 1d6 every time they step on red during the same round

## Notes

As they traverse deeper, they'll encounter the Mellifluous Cascades—a serene waterfall that emits a soft, melodic hum echoing the strange resonance they've been tracking. Here, the enchantments of the woods grow stronger, the air thrumming with latent magic.

Beyond the cascades there is a cave where the PCs can find the cultist, bodies of a dozen people, and next to them a pile of discarded items. Among them you find a basket turned over and sweet rolls and apples scattered on the ground.




## Notes