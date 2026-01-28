---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Seline Delayne.webp
aliases:
  - Master of Ceremonies
ancestry: Human
heritage: Versatile Heritage
gender: Female
pronouns: She/Her
age: Adult
sexuality: 
alignment: 
language:
  - Common
  - Varisian
occupation:
  - Entertainer
organization:
  - "[[Twilight Circus]]"
location:
  - "[[Ilayas]]"
  - "[[The Upper District]]"
condition: Healthy
party1relation: Unmet
quest:
  - "[[Murder at the Circus]]"
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
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Party 1 Relation** | `INPUT[Party1Relation][:party1relation]` |
>> **Quest** | `INPUT[inlineListSuggester(optionQuery(#Quest AND !"z_Templates"), useLinks(partial)):quest]` |

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
> Leader of the Twilight Spectacle Circus.

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


## Summons

The PCs receive a message midmorning via a carnival crew member. Mistress Delayne requests the PCs return to the circus in order to discuss a potential job opportunity.

When the PCs arrive at the circus, the carnival has not opened for the day’s business yet. Seline waits beside a large private wagon with an adjoining canopy, and chairs are arranged around a nearby campfire. She greets them kindly but with a businesslike air, and after a brief introduction gets to the reason for her invitation.

“I appreciate your efforts yesterday in the regrettable incident with our dragon. I fear I could also use your help with another matter. You may have heard there was a murder in town last night. The circumstances, I am told, implicate people from my circus—something I find very hard to accept. I’d like to contract you to represent the Twilight Circus to determine who is really responsible and preserve our reputation.”

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

Treasure: Seline offers the PCs 200 gp if they find conclusive proof as to the identity of persons responsible. 

## Notes





