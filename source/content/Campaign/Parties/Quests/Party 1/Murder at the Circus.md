---
tags:
  - Quest
art: z_Assets/Locations/Twilight Spectacle Circus.webp
NPC:
  - "[[Seline Delayne]]"
location:
  - "[[Ilayas]]"
  - "[[The Upper District]]"
adventure: "[[Ilayas Job Board]]"
whichparty: "[[Party]]"
status: ⏳
aliases:
  - Murder at the Circus
quicknote: The Veridanes find a scapegoat for murder
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
> A fun celebration during the Celestial Night festival turns bloody.

> [!metadata|characters]+ Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(quest, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC


## Overview
## Start of Festivities

Circus folk hold a parade that marches through town in a spectacle of sights, music, and drumming. Banners and streamers herald a procession of clowns, stilt walkers, and tumbling acrobats, all of whom wave to the townspeople. Carnival barkers call out to people on the streets, promising thrills, chills, and delights for people of all ages (at the modest price of a gold coin). The entire procession is a formal declaration of the carnival’s opening, and seeks to draw out the curious and idle to follow along to the procession’s end, the parade grounds.

## Parade

The circus parade winds its way through the bustling city streets, bringing a burst of vibrant colours, lively music, and a sense of anticipation. As the day before the grand opening, the performers and magical creatures that make up the circus eagerly showcase their talents to the eager onlookers.

### Floats and Spectacular Displays

Elaborate floats showcase different aspects of the circus. A float featuring acrobats flipping and twirling through the air captures the attention, while another displays magical illusions, leaving the crowd in wonder. Giant puppets operated by skilled performers add a touch of whimsy to the procession, creating an otherworldly atmosphere.

### Marching Bands and Melodies

Enthusiastic musicians, adorned in colourful costumes, march alongside the circus floats, playing catchy tunes that fill the air with joy. The rhythmic beats of drums, the cheerful jingles of bells, and the triumphant blasts of horns create an infectious energy that has onlookers tapping their feet and clapping to the music.

### Creatures and Performers

Alongside the floats, creatures from the circus parade through the streets. Lions, graceful unicorns, and mischievous pixies captivate the audience, as their handlers guide them through the procession. Acrobats perform daring stunts on mobile platforms, adding an element of danger and excitement to the spectacle.

### Street Performers Interact with the Crowd

Clowns, jesters, and other roving performers move through the crowd, engaging with spectators. They juggle, dance, and perform sleight-of-hand tricks, bringing laughter and amazement to both children and adults. Some even hand out colourful trinkets, adding to the festive atmosphere.

### Culmination at Festival Square

The parade concludes at the heart of the city, at Festival Square. Here, the circus sets up a temporary stage for a preview performance, giving the audience a taste of what's to come during the week. The air is filled with excitement and anticipation for the upcoming festivities, building up to the grand celebration of Angel Night Festival.

The stage dims, leaving only a few flickering torches to illuminate the performance area. The air is charged with anticipation as the fire dancers make their entrance, adorned in costumes that seem to catch fire themselves. The beat of drums intensifies, setting the rhythm for the mesmerizing display.

The lead fire dancer steps forward, twirling a staff ablaze with orange and red flames. With each pirouette, trails of fire trace mesmerizing patterns in the night. The dancer moves with a perfect blend of grace and danger, the flames seemingly an extension of their body. The crowd is drawn into the hypnotic dance, their faces illuminated by the warm glow.

As the intensity builds, more dancers join in, each wielding flaming hoops or spinning poi in intricate patterns. The scent of burning fuel mingles with the excited murmurs of the audience. The flames seem to respond to the rhythm of the music, leaping higher and intensifying in colour, creating an awe-inspiring spectacle that holds the entire square in a state of collective wonder.

### Grand Finale Extravaganza

With the echoes of the fire dancing still lingering in the air, the stage transforms into a kaleidoscope of lights and colours for the grand finale. The ringmaster takes centre stage, his top hat glinting in the spotlight. He raises his arms, signalling the ensemble of performers to converge for the climactic conclusion.

The illusionist reappears, casting a spell that transforms the stage into a dreamscape. Ethereal projections, illusions, and bursts of glittering sparks envelop the performers. Acrobats somersault through illusions, appearing to defy the laws of physics. The clowns add their comedic flair, creating a whimsical backdrop for the magical spectacle.

The fire dancers return for the finale, this time incorporating their flaming props into the overall display of magic. Trails of fire intertwine with illusionary creatures, creating a harmonious blend of danger and enchantment. The crowd is on the edge of their seats, caught in a sensory overload of sight and sound.

As the performance reaches its zenith, a crescendo of music and pyrotechnics accompanies the grand reveal. A breathtaking display of fireworks explodes overhead, painting the night sky with vibrant hues. The audience erupts in cheers and applause as the performers take their bows, their faces aglow with the satisfaction of having witnessed an unforgettable spectacle.

### Inviting the Audience

With the stage bathed in the afterglow of the grand finale, the ringmaster steps forward once again, his presence commanding attention. He extends a heartfelt thank you to the audience, expressing gratitude for their enthusiastic participation in the preview performance. With a theatrical flourish, he invites everyone to join the circus festivities throughout the upcoming week.

## The Midway

The midway offers a multitude of games of chance, each costing 3 sp per play.

The proprietor of the Twilight Circus, Seline Delayne, is observing the crowd at the midway. If the PCs ask around, carnival crew won’t hesitate to identify her, but they also add that Seline often watches the midway in her spare time.

### A1. Midway Entrace

|A path runs east here from the midway toward the traveling zoo. To the south are booths with pavilion tent tops that provide shade for the games of skill and chance played beneath. Behind them are circus wagons, some clearly only for transportation and equipment, while others are attractions and portable shops for merchants. To the north is a gigantic tent erected on tall poles with a stage curtain pulled shut across its front.|

This busy area leads into the midway, with its attractions in a small tent and stands that promise exciting games and diversions. After the PCs explore the carnival, the “baby dragon” from area A6 gets loose.

### A2. King of the Carnival

| A heavy, long-handled mallet leans against a 3-foot-wide and 12-foot-high wooden tower crowned with a stuffed lion’s head. At the base is a lever attached to a puck that slides up and down a pole running the length of the tower up to the lion’s head.|

This is a classic high-striker game with a twist. The game is run by Narthi Vangkot (CG male human commoner 3), a Norggheim strongman with a talent for calling out and challenging passersby. Narthi invites carnival-goers to demonstrate their “power and passion” to him by “taming the savage beast on yonder pole.”

Players grasp a heavy mallet and strike the lever to send the puck to the top of the pole with a Strength check. Instead of a bell ringing, the lion head animates and responds to how high the puck reaches. Success against a DC of 18 makes the lion roar, winning the game. If the result of the Strength check is 22 or higher, the lion’s thundering roar can be heard across the entire carnival. Narthi (who takes the game quiteseriously) presents the player with an additional prize, a paper crown identifying the victor as a “King or Queen of the Carnival.”

If the player fails the Strength check, the lion head merely meows and licks its lips. Should the mallet be seized as a weapon of opportunity, treat it as a greatclub.

Story Award: The PCs earn 40 XP if they get the lion to roar, and an additional 40 XP for a thunderous roar. The paper crown grants the owner a 50% discount on admission to big top performances and the sideshow.

### A3. The Lovely Madame Masque

| Three raised runways meet at a point like an arrow beneath a brightly colored pavilion tent. Where the runways meet sits a tall, rectangular box covered in mirrors. Off to one side is a raised speaker’s podium. Posters on makeshift signs depict an attractive woman in a provocative gown and silver mask, with the words “The Lovely Madame Masque” in bold print.|

This game of chance challenges the skill of Perception.

Unlike most midway games, multiple people play this one together, forming a betting pool. The winner takes half of the proceeds (an average of 10 sp) and the circus keeps the other half. A carnival barker recruits passersby until a minimum number of players are gathered. He then introduces Madame Masque, who emerges from the tent to wave silently at the crowd.

Madame Masque is a shapely woman in a provocative Varisian costume gown of red and black silk held together by ribbons. She is adorned with all manner of scarves, necklaces, earrings, and other decorative costume pieces, but her face is concealed by a finely crafted silver mask showing only her playful brown eyes. She remains mute, but nods and waves to the crowd.

The game is simple but challenging, calling on the power of observation. Madame Masque struts down the center runway and poses for 1 minute, flirting silently with the crowd. She then saunters to the mirrored cabinet, steps inside, and closes it behind her. After a flourish from the barker, the cabinet is opened to reveal three different Madame Masques.

Each figure walks down a different runway, while four guards (N human warriors 2) prevent anyone from grasping at them. Each Madame Masque wears an entirely different costume from the original, but one wears a single piece of jewelry, item of clothing, or flower only the original wore. All three are illusions. The crowd has 1 minute to call out the matching item, and the first to correctly guess wins—or the players run out of time and the house keeps the pot.

 A successful DC 18 Perception check permits the PCs to spot the item, with the highest result indicating the first PC to guess correctly. After guesses are made and a winner (if any) declared, two of the illusions vanish. The remaining image walks back to the mirrored cabinet where the real Madame Masque reemerges. Both compare the item in question, demonstrating the game is not rigged.

If the winning result is 25 or higher, the PC can name the trinket quickly and with great confidence, capturing the attention of Madame Masque herself. She walks on the runway toward the winner and slowly pulls a single scarf or ribbon from her costume, allowing it tumble into the winner’s grasp. Onlookers regard such a winner with envy, and Madame Masque gives the winner a final flirtatious over-the-shoulder glance before disappearing into the tent. Beneath her mask, Madame Masque is played by Ika. Madame Masque’s game is never run while Darshan is performing or making an appearance in her special cage.  For more information on Ika, see page 15.

Story Award: If the PCs win, they earn 40 XP, and they earn an additional 40 XP if they’re given the ribbon. If the ribbon is worn prominently, the owner gains a +5 bonus on all Diplomacy checks with carnival crew and performers.

### A4. Madame Fate

A mysterious tent veiled in ethereal fabrics where Madame Fate performs tarot readings and divinations for the curious visitors. Her tent, adorned with rich tapestries and twinkling lights, beckons those seeking answers from the unseen.

#### Appearance

> [!warning]- Photo
> ![[Madame Fate.webp]]

An older woman, her age difficult to discern due to an otherworldly quality that seems to defy time.

Dressed in flowing robes adorned with symbols of the cosmos, stars, and intricate patterns that seem to shift and shimmer in the faint light.

Her piercing eyes hold a depth that seems to see beyond the mundane, often leaving visitors feeling like she can glimpse into their very souls.

#### The Tent

Inside her tent, the ambiance is a blend of incense, fragrant herbs, and a soft, mystical glow from candles arranged around the room.

Velvet cushions and embroidered tapestries create a cozy yet mysterious atmosphere for visitors seeking guidance.

#### Abilities and Readings

Madame Fate possesses a deep understanding of divination and oracle practices, using tarot cards, scrying bowls, and other arcane tools to reveal insights into the future.

Her readings are known for their accuracy, though often veiled in symbolism and riddles, requiring seekers to contemplate the meanings behind her words.

#### Role in the Circus

She acts as both an attraction and a guide, drawing in visitors with promises of glimpses into their destinies.

People from all walks of life visit her tent, seeking advice, reassurance, or merely out of curiosity, making her a sought-after figure within the circus.

#### Mysterious Aura

Madame Fate's origins are a subject of speculation among circus-goers; rumours whisper of a past filled with ancient prophecies and encounters with powerful beings.

Some claim she has foretold significant events within the circus and beyond, earning her a reputation for being an oracle of remarkable insight.

#### Scrying Readings

**Setup and Environment:**

Madame Fate's scrying readings take place in a secluded, dimly lit area within her tent.

A large, ornate scrying bowl sits atop an intricately carved pedestal, surrounded by candles and crystals emitting a faint, otherworldly glow.

**Process:**

Seekers sit opposite Madame Fate as she gazes into the scrying bowl, allowing her visions to unfold.

She chants incantations and focuses her energy, inviting glimpses of the past, present, or potential futures to manifest within the reflective surface.

**Interpretation:**

Madame Fate guides visitors through the visions, interpreting the symbolic imagery and scenes that appear in the scrying bowl.

Her readings are often cryptic, requiring seekers to reflect on the symbolism and messages conveyed in the visions.

#### Tarot Card Readings

Madame Fate employs a unique, ancient deck of tarot cards adorned with intricate illustrations representing archetypes, elements, and cosmic energies.

A small, velvet-covered table serves as her workspace, where she lays out the cards in intricate spreads.

### A5. The traveling Zoo

A portable fence of wooden posts and rope cordon off this section of the circus. Several wagons constructed to serve as animal cages line the perimeter, with an occasional haystack piled between them. In the center of the area is a large tent whose wall flaps have been lifted up and tied off to allow easy viewing.

**Lion performance**

The entrance to the traveling zoo is sectioned off from the rest of the carnival. Guests are free to enter but exit the same way, which permits the animal handlers a final opportunity to proposition visitors for tips.

Some creatures are never brought out of their cages, except in rare instances underneath the big top. This includes the “baby dragon,” and the manticore whose tail spikes have been surgically removed.

### A6. Baby Dragon Cage

This heavy metal cage is labeled “Baby Dragon,” but actually houses a monitor lizard. It’s currently kept toward Darshan the front of the traveling zoo area to impress potential visitors. Some of the Monchellos’ thugs set the monitor lizard free on the first night of the carnival. See the Uncaged Dragon encounter below.

### A7. The Lair of the Sphinx

|This enormous tent is dwarfed only by the big top itself. The southern side has no wall, just a tall curtain pulled across its front. A sign posted outside advertises that this area has been set aside for meeting the sphinx at limited times throughout the day. Just inside is a large metal cage with no floor and bars running across the top. A single large door is set on the north corner of the west face, secured by a heavy lock. Strewn about the grass beneath the cage are silk sheets and piles of cushions and satin pillows.|

The neatly painted sign advertises times when Darshan the sphinx is available to meet the curious and wonderstruck. Two guards are stationed here during Darshan’s appearances. Visitors are not permitted to enter early. Once they are inside, any attempt to interact with the sphinx physically is prohibited.

Ika conceals herself within the shadowy folds of the tent with her cloak of elvenkind, casting ventriloquism and minor image. The guards work as her active partners, keeping visitors under control and Darshan’s appearances on time and brief, then clearing the tent before Ika must drop the illusion.

Darshan’s only appearances besides the evening show are for a few minutes after **midday** (12:00-12:30) and again at **midafternoon** (18:00-18:30). She lounges in the center area with no regard for humanoid taboos concerning her state of undress. Visitors are free to walk around and speak with her. Provided they’re friendly or polite, she replies in kind.

The rest of the time this area is empty, and guards aggressively discourage snooping around the tent when it is not in use.

### A8. Murder Site

This is the spot where the body of Sister Esrelda Woodmere is discovered later in the adventure. See The Second Murder.

### Uncaged Dragon

After the PCs have opportunity to explore the circus, they are drawn by the sudden screams of townspeople fleeing from the midway.

Creature: As the start of their plot to undermine the circus, the Gilded Hands are causing trouble—starting with the monitor lizard the circus calls a “baby dragon.” First, one of them wearing a disguise paid a gold piece to the panotti Phardaen to put on a show outside the beast tent. He was flying and doing tricks using his massive ears, unwittingly distracting the crowd while the thugs snuck in and freed the lizard. Now the beast scurries around the midway, hissing at the fleeing carnival-goers and snapping its jaws at anyone who gets too close.

Tactics: The lizard is confused by all the commotion of the circus. It’s rarely set free within such a busy area. If it’s reduced to 11 hit points or fewer with nonlethal damage, it tries to submit to its attackers as though it were fighting for territory in the wild. If it’s reduced with lethal damage, it fights until knocked unconscious or killed.

Phardaen: After he saw that the lizard had been set free, Phardaen rushed toward the scene. He’s not quite brave enough to try bringing the creature under control himself, and he’s afraid of hurting the lizard. When the PCs arrive, he begs them not to kill the “baby dragon.” As long as the PCs deal nonlethal damage or just try to trap the lizard, he stays out of the way. If it seems like they might kill it, Phardaen attacks them, flying overhead and using his ears for wing attacks while pleading for the PCs to go easy on the lizard. He only draws his short sword if he’s afraid for his own life.

Development: Once the fight is over, Berthold Flavion, the circus’s Master of Beasts, arrives, winded and flushed. Some members of the crew carry the lizard back to its cage, and others help calm Phardaen down and take him back to the sideshow (described in Appendix 2).

If the PCs go to talk to Phardaen afterward, he tells them that someone paid him a gold piece to put on a show. He says it was someone with a big red beard, but nobody else remembers seeing anyone like that. Phardaen has a history of dishonesty, particularly when threatened, though he claims he’s telling the truth this time.

Treasure: Berthold rewards the PCs with 25 gp for preventing innocents from being harmed. If they brought the lizard under control without unduly hurting it (meaning it retains at least 50% of its hit points or was subdued using nonlethal damage), he gives them an additional 25 gp.

## DM Notes

This murder happens after the PCs first night at the circus, and the body is found in the morning.

### The First Murder

After sowing the seeds of mistrust with the escaped monitor lizard, the Gilded Hands begin the next phase of their frame-up after the opening night’s final show. Highest on their list for robbery and murder is Archivin Walder— local moneylender and pawnbroker, and proprietor of the Locked Box.

Through clever use of alchemy, the thieves’ guild stages Walder’s murder to make it look as though Darshan is responsible. The Captain of the Guards, Kyra Feldane (LG female human expert 4), confronts Seline Delayne first thing the following morning. Seline, knowing the sphinx did not murder anyone—and also knowing the locals are unlikely to assist or trust her predominantly Varisian crew—decides to find a third party to represent the circus and clear its name without needing to divulge its secrets.

> [!warning]- Photo
>![[Kyra Feldane.webp]]

### Summons

The PCs receive a message midmorning via a carnival crew member. Mistress Delayne requests the PCs return to the circus in order to discuss a potential job opportunity.

When the PCs arrive at the circus, the carnival has not opened for the day’s business yet. Seline waits beside a large private wagon with an adjoining canopy, and chairs are arranged around a nearby campfire. She greets them kindly but with a businesslike air, and after a brief introduction gets to the reason for her invitation.

“I appreciate your efforts yesterday in the regrettable incident with our dragon. I fear I could also use your help with another matter. You may have heard there was a murder in town last night. The circumstances, I am told, implicate people from my circus—something I find very hard to accept. I’d like to contract you to represent the Umbra Carnival to determine who is really responsible and preserve our reputation.”

If the PCs ask questions or press Seline for more information, she responds as follows.

Choosing the PCs:

> [!warning]+ Message
> “Your performance yesterday showed me that you’re capable people. And honestly, we don’t have many friends to choose from here.”

The Captain’s Investigation: 

> [!warning]+ Message
>  “I don’t believe captain Feldane is an unjust woman, but I think she’s under greater pressure to keep the peace than to find the guilty. After all, my people aren’t her first concern. My belief is a thirdparty investigation stands a better chance of clearing our good name than the local constabulary.”

The Circus’s Needs: 

> [!warning]+ Message
> “This isn’t just about lost revenue or personal reputation, or even protecting who they accused. We rely on being able to buy provisions in the towns we visit. I can’t let allow our ability to perform and obtain supplies to become compromised.”

Accepting the Job: If the PCs accept, Seline grants them access to most areas of the circus. She also draws up a signed, sealed letter to captain Feldane, identifying the PCs as her chosen third-party investigators. Finally, she recommends that the party make visiting the Captain one of their first stops in their investigation.

Treasure: Seline offers the PCs 200 gp if they find conclusive proof as to the identity of persons responsible.  She’s prepared to double that if the PCs can do so without divulging the truth about Darshan but won’t explain that during this initial meeting.

## The Locked Box


## Notes