---
tags:
  - Quest
art: z_Assets/People/Eltane Gestal.webp
aliases:
  - Eltane Gestal
quicknote: Edi's quest 1
adventure: "[[Nezoh]]"
whichparty: "[[Party]]"
status: ✅
location:
  - "[[Aetherian Hall]]"
  - "[[Ilayas]]"
NPC:
  - "[[Eltane Gestal]]"
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
> Nezoh is in search for the Philosopher Stone.

> [!metadata|characters]+ Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(quest, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC


## Overview
Eltane, having studied at the prestigious magical academy Arcanamirium and possessing a foundation in magical studies, despite not progressing to higher ranks, possesses theoretical knowledge about transmutation spells and their principles. However, the specifics of transmuting dirt into gold remains beyond his grasp due to the complexity and advanced nature of such spells.

He has a rudimentary understanding of transmutation magic's fundamental concepts, such as altering the fundamental properties of substances or objects. This knowledge encompasses the theory behind changing the composition of materials, albeit on a much simpler scale, like changing the color or texture of an object.

Eltane may know that transmutation spells altering elements or substances can be intricate and resource-intensive, requiring precise incantations, specific components, and deep mastery of magical theory. However, the specifics of transmuting an abundant and basic substance like dirt into a valuable and complex element like gold would eludes his level of expertise. This level of transmutation typically involves high-level, advanced spells beyond what he might have encountered during his studies.

##### The [[philosophers-stone]] 
[[Eltane Gestal]] asks the party to give him a 2-3 days to do some research because he recalls something about a former member of The Three (Council of Teseon), who is it said that has crafted the Philosopher's Stone [[Master Helios Staven]]. He can send word to where the party is staying once he has some info.

>[!note]+ Read Aloud
>Something that might be interesting though, is the compelling story of Master Helios Staven, an esteemed alchemist who was once a member of The Three within the ruling council of Teseon. Driven by a unique vision and a quest for new horizons, Master Staven shocked the political elite by abruptly departing from the capital city and leaving his position to Iranez of the Orb, roughly 100 years ago.
>
>The book chronicles Staven's intended departure into the [[Mana Waste]], setting out on a daring endeavor to establish a new city. The book ends with a bold proclamation: *"If life can flourish in the Barren Lands, I shall fashion a city from its dust."* 

##### "The Arcane Legacy: Alchemy, Transmutation, and the Sage of the [[Mana Waste|Barren Sands]]"
"The Arcane Legacy" is a renowned tome chronicling the profound realm of alchemy, penned by the enigmatic sage, Master Helios Staven. This scholarly work delves deep into the esoteric art of transmutation, exploring theories and speculations on the creation of the mythical Philosopher's Stone. It elucidates alchemical principles, the transformative power of elements, and the symbolic significance of the stone in mystical lore.

The book is divided into sections, with the initial chapters elucidating the history of alchemy, its evolution across civilizations, and the philosophical underpinnings of transmutation. It then delves into **theoretical** frameworks for the creation of the Philosopher's Stone, incorporating alchemical symbolism and mystic interpretations. And while illustrative diagrams and ancient texts cited throughout the book lend credence to its scholarly authority, no one other than master Staven is said to have had the power to create it.


##### Possible Leads
> [!note]+ Read Aloud
> The sage's departure became legendary, and his journey into the inhospitable desert remains a subject of intrigue and speculation among scholars and occultists. Actually, I believe that there's a book or at least research notes by a professor here at the "Aetherium Academy of Mystic Arts", Professor Astrid Vayne, who researched the work of Master Staven. I'm afraid I don't know the name of the book though, but if you're looking for someone who might know more, you could look for Professor Vayne. She wrote a book about Master Helios' life and research. The Astrum Archives should have the book, as well as the other 3 I mentioned though if you're looking for reasearch material.
> 
> Or.. _he chuckles_.. I saw Lady [[Alinya Vilicus]] drop in an out of the [[Aetherian Hall]], and apart from Professor Vayne, she might be the only person to know something else. But I doubt she'll have time to see you.

**If the PCs ask about where they could find her**

> [!note]+ Read Aloud
> Not sure, she's here on a diplomatic mission with the Council and is staying for the Celestial Night festival, although her Warder seems to be interested in more than just council business. What that is, I'm not sure, but she hasn't always accompanied Lady Vilicus during her visits. 

##### "The Enigma of Master Helios: Disputing the Mirage of the Barren City" (250 pages - approx 7h reading time)
"The Enigma of Master Helios" presents a compelling counter-argument to the widely romanticized tale of the alchemist's ambitious departure into the [[Mana Waste]]. Authored by the skeptic scholar, Professor Astrid Vayne, this contentious book challenges the notion of Master Helios Staven's grandiose venture to establish a city in the barren sands.

The book methodically dismantles the glorified narrative surrounding Master Helios Staven's disappearance, scrutinizing the supposed feat of creating a new city in the unforgiving Mana Waste. Professor Vayne employs rigorous research, historical scrutiny, and logical deduction to assert the implausibility of such a venture.

Using meticulous examination of historical records and absence of credible witnesses, Vayne contends that the lack of information about Master Staven's supposed city is glaring. No substantiated reports, no travelers' tales, and no returning emissaries from [[Alkenstar]] have validated the existence of this enigmatic city.

Furthermore, the professor underscores the conspicuous absence of any news or sightings of Master Helios himself, casting doubt on the fate of the esteemed alchemist. The lack of any verifiable information about his whereabouts or survival fuels Vayne's argument that the alchemist might have perished in the harsh, inhospitable expanse he sought to conquer.

In essence, "The Enigma of Master Helios" serves as a skeptical and critical appraisal, challenging the romanticized myth of an alchemist's audacious quest. It questions the credibility of the fabled city's creation, shedding light on the lack of tangible evidence and the probable fate of Master Helios Staven, shrouded in the mysterious allure of the Mana Waste.


## Events

- Asking for info around the town, Society DC 20 reveals that [[Eltane Gestal]] is an assistant in the service of The Council of Ilayas and can be found most likely at the [[Aetherian Hall]].
- Ask the party what they are wearing, NPCs will say that they might be underdressed or that they may want to clean themselves if they want to be taken seriously.

## Questions 
1. **How much do you know of transmutation?** Eltane: "I have a foundational understanding of transmutation magic, having studied at Arcanamirium. While I possess theoretical knowledge about the principles of transmutation spells, my expertise lies more in the fundamentals rather than intricate applications."
    
2. **Do you know how to transmute dirt into gold?** Eltane: "Transmuting dirt into gold? That's quite an ambitious endeavor. While transmutation magic can indeed alter the properties of substances, the complexity of turning something as abundant as dirt into a precious metal like gold is beyond my level of expertise. Such feats typically require mastery of high-level, advanced spells and intricate understanding of alchemical principles."
    
3. **How about copper/silver into gold? Would that be easier?** Eltane: "Transmuting copper or silver into gold might seem like a more attainable goal, given their proximity on the elemental scale. However, it's important to understand that even such a seemingly simpler transmutation is still a formidable task. The conversion of one metal into another involves complex magical processes and precise control over magical energies. It's not impossible, but it certainly falls into the realm of advanced transmutation magic."
    
4. **How about any other plentiful material?** Eltane: "Certainly, transmuting other abundant materials into more valuable substances is a common pursuit among alchemists and transmuters. However, the ease of such transmutations can vary depending on the specific materials involved and the intricacy of the desired transformation. Basic alterations like changing the color or texture of materials might be within reach with the right spells and techniques, but significant transformations often require considerable skill and magical prowess."
   
1. **Can you recommend any specific texts, scrolls, or sources of knowledge where I could learn more about transmutation magic and its applications?**
    
    Eltane: "For a self-taught mage like yourself, I'd recommend seeking out texts on basic alchemy and magical theory to lay a solid foundation. Look for works by renowned alchemists and transmuters, such as the 'Tome of Transmutation' by Archmage Varian or 'The Alchemist's Primer' by Master Alistair. These texts often contain valuable insights into the principles and practices of transmutation magic."
    
2. **Are there any legendary or historical figures known for their expertise in transmutation magic that I could study or learn from, even if indirectly?**
    
    Eltane: "Indeed, there are many legendary figures whose mastery of transmutation magic is well-documented. One such figure is **Master Helios Staven** who is considered a **Trailblazer in Arcane Exploration:** Eager to delve deeper into the arcane arts, Master Helios diverted from traditional dwarven pursuits to explore the untapped potential of transmutation magic. His relentless quest for knowledge drove him to unlock the secrets of transformative alchemy. His treatises on transmutation magic are still studied by scholars today. 
    
3. **In your opinion, what are the most critical principles or concepts I should focus on understanding to advance my understanding of transmutation magic?**
    
    Eltane: "Understanding the fundamental principles of alchemy and magical transmutation is key. Focus on mastering concepts such as the Law of Equivalent Exchange, the principles of elemental manipulation, and the nature of magical resonance. Additionally, honing your skills in visualization and concentration will greatly enhance your ability to manipulate magical energies."
    
4. **Are there any rituals, exercises, or practical experiments I could undertake to develop my skills in transmutation magic, even if they are basic or introductory in nature?**
    
    Eltane: "Certainly! Practice simple transmutation exercises, such as changing the color or texture of small objects, to develop your control over magical energies. Experiment with basic alchemical reactions to gain a deeper understanding of the properties of different materials. And don't underestimate the power of meditation and mental discipline in refining your magical abilities."
    
5. **Given my limited formal training, do you have any advice or recommendations for honing my magical abilities specifically toward the goal of transmutation?**
    
    Eltane: "Focus on practical experimentation and hands-on experience. Don't be afraid to make mistakes – learning from failure is an essential part of the journey. Seek out opportunities to observe or assist experienced transmuters, and don't hesitate to ask questions or seek guidance from those more knowledgeable than yourself."
    
6. **Are there any known limitations or risks associated with attempting transmutation magic, particularly for someone without extensive formal training?**
    
    Eltane: "Transmutation magic can be unpredictable and potentially dangerous, especially for those without proper training and experience. Attempting to transmute complex or volatile substances without understanding the underlying principles can lead to unintended consequences, such as magical backlash or unstable transformations. Proceed with caution, and always prioritize safety and responsibility in your magical experiments."
    
7. **Beyond traditional spellcasting, are there any alternative methods or approaches to transmutation that I should explore or consider, such as alchemical techniques or divine intervention?**
    
    Eltane: "Absolutely. Alchemical techniques, such as potion brewing and metallurgy, offer alternative avenues for exploring the principles of transmutation. Additionally, seeking guidance from divine sources, such as gods or powerful spirits associated with transformation or wealth, may provide unique insights or assistance in your quest for transmutation mastery."
    
8. **Have you encountered any anecdotes or legends regarding unconventional or unconventional methods of transmuting materials, particularly those that might be accessible to someone without formal magical training?**
    
    Eltane: "There are indeed tales of unconventional transmutation methods, ranging from ancient rituals to mystical artifacts. However, such stories are often shrouded in mystery and myth, making them difficult to verify or replicate. Proceed with caution when exploring such avenues, as they may lead to unexpected consequences or dangers."
    
9. **Are there any specific components, reagents, or rare materials that are commonly used in transmutation spells, and where might I acquire them or learn more about them?**
    
    Eltane: "Many transmutation spells require rare or exotic components, such as powdered gems, elemental essences, or alchemical catalysts. These can often be found in specialized magical shops, alchemical laboratories, or even in the natural world – though acquiring them may require resourcefulness, negotiation, or even adventuring. Consult with experienced alchemists or transmuters for guidance on acquiring and utilizing these materials."
    
10. **Given the complexity of transmutation magic, do you believe it's possible for someone like me, without formal training, to eventually master the art of transmuting materials like dirt into valuable substances like gold? Or would such feats remain beyond my reach without extensive study and experience?**
    

Eltane: "While mastering the art of transmutation may indeed be a challenging journey, I firmly believe that dedication, perseverance, and a thirst for knowledge can overcome even the greatest of obstacles. With patience and practice, I have no doubt that you can achieve remarkable feats of transmutation magic – perhaps even the legendary transformation of dirt into gold. Never underestimate the power of determination and the human spirit in the pursuit of magical mastery."
>[!note]+ Read Aloud
>"Eltane: Ah, so you and your eidolon are already acquainted with the principles of transmutation. That's quite advantageous in your pursuit. With your shared understanding, I would recommend delving deeper into the intricacies of transmutation magic, exploring its more esoteric aspects and perhaps seeking out specialized knowledge that may not be readily accessible to those without a summoner's connection to the arcane.
>
>Consider expanding your repertoire of transmutation spells and techniques, leveraging your eidolon's innate abilities in your magical endeavors. Additionally, delve into the history and lore surrounding transmutation magic, seeking out ancient texts or hidden tomes that may contain secrets and insights into its mysteries.
>
>Furthermore, do not underestimate the value of experimentation and practical experience. Continue to push the boundaries of your understanding, testing new theories and refining your techniques through hands-on practice. And remember, while transmutation magic offers great potential, it also carries inherent risks. Be cautious in your explorations, and always prioritize safety and responsibility in your magical endeavors."
## Books
**1. Tome of Transmutation:** 
_Author:_ Archmage Varian Thorne is a renowned figure in the arcane community, known for his unparalleled mastery of transmutation magic. Born into a family of esteemed wizards, Varian displayed a natural aptitude for magic from a young age. After years of dedicated study at the prestigious Arcanamirium, he rose to prominence as one of the foremost experts in the field of transmutation, earning the title of Archmage and penning the seminal work, the Tome of Transmutation.
_Description:_ The Tome of Transmutation is a revered text among scholars and practitioners of transmutation magic. Written by the esteemed Archmage Varian, the book delves deep into the theory, practice, and history of transmutation magic, offering a comprehensive guide for aspiring transmuters.

_Contents:_ The book begins with an exploration of the fundamental principles of transmutation, such as the manipulation of elemental energies, the transmutation of matter, and the laws governing magical transformation. It then delves into various branches of transmutation magic, including alchemy, shape-shifting, and the creation of magical constructs. Historical examples of legendary transmuters and their feats are interspersed throughout the text, providing inspiration and insight into the possibilities of transmutation magic.

_Concrete Learning:_ After reading the Tome of Transmutation, the character gains a deeper understanding of the underlying principles and mechanics of transmutation magic. They learn practical techniques for manipulating magical energies, refining their control over elemental forces, and conceptualizing complex transmutations. Additionally, they may glean insights into specific spells or rituals for transmuting materials, as well as cautionary tales about the risks and limitations of such magic.

**2. The Alchemist's Primer:** 
_Author:_Master Alistair Blackwood is a legendary alchemist and transmuter, revered for his groundbreaking contributions to the study of alchemy. Born into a humble family of herbalists, Alistair's passion for alchemy led him on a lifelong journey of discovery and experimentation. Through tireless dedication and innovative research, he mastered the art of transmutation, earning the title of Master and writing the definitive guide, The Alchemist's Primer, which has inspired generations of aspiring alchemists.

_Description:_ The Alchemist's Primer is a foundational text in the study of alchemy and transmutation. Written by the renowned Master Alistair, the book serves as a practical guide for novice alchemists and aspiring transmuters, offering step-by-step instructions for mastering the art of magical transformation.

_Contents:_ The book begins with an overview of alchemical principles, including the properties of different materials, the transmutation of base elements, and the preparation of alchemical reagents and catalysts. It then presents a series of hands-on exercises and experiments designed to develop the reader's skills in alchemical transmutation, such as potion brewing, metallurgy, and elemental manipulation. Throughout the text, Master Alistair emphasizes the importance of precision, patience, and intuition in the practice of alchemy.

_Concrete Learning:_ After reading The Alchemist's Primer, the character gains practical knowledge of alchemical techniques and methodologies for transmuting materials. They learn how to identify and gather rare reagents, how to prepare and mix alchemical concoctions, and how to conduct experiments to test the effects of different transmutation processes. Additionally, they acquire a repertoire of basic alchemical recipes and formulas, allowing them to begin experimenting with simple transmutations in their own practice.



## Notes