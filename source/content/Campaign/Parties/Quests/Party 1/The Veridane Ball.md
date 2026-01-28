---
tags:
  - Quest
art: z_Assets/Misc/PlaceholderImage.png
whichparty: "[[Party]]"
status: ⏳
location:
  - "[[Ilayas]]"
NPC:
  - "[[Alinya Vilicus]]"
  - "[[Isiril Adren]]"
  - "[[Lysandra]]"
  - "[[Elandra Nightshade]]"
  - "[[Lord Ealdred Corlas]]"
  - "[[Tessa Fairwind]]"
  - "[[Aeliana Veridane]]"
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
> As the players approach the **Veridane Estate**, they are met with a **spectacle of wealth and power**. The **manor's exterior is illuminated by soft magical lanterns**, casting an ethereal glow over the **immaculate stonework** and **pristine gardens**. The air is thick with the mingling scents of **perfumed nobility, fresh roses, and fine wines** being served on silver trays by impeccably dressed attendants.
> 
> The **main entrance**, a set of **wide double doors flanked by marble columns**, is open, allowing glimpses of the **lavish interior beyond**. The **soft melody of string instruments** drifts out, setting the tone for the evening—elegant and refined, yet full of **subtle tension** beneath the surface.



> [!metadata|characters]+ Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "NPC") AND econtains(quest, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC


## Overview
### Celestial Night Festival
In Ilayas, as midnight approaches on Angel Day, the city’s energy swells with anticipation for the Celestial Night. The two celestial bodies, the Star of Aegis and the Moon of Aurelia, begin their slow alignment with Brightwyn, the world on which they live. The Star of Aegis, a pale blue light representing protection and guidance, draws closer to Aurelia, a silver moon said to bring wisdom and fortune. As they align, a soft glow spreads across the city, casting everything in a shimmering silver-blue hue.

At the stroke of midnight, a reverent hush falls over the crowd, and priests of Ilayas light a series of ceremonial lanterns along the main thoroughfares. Each person in the streets holds a candle or lantern of their own, symbolizing the hope and protection brought by this celestial alignment. When the alignment is complete, people erupt in cheers, hugging friends and strangers alike. Musicians take to the streets, playing joyful tunes as dancers perform, weaving ribbons and spells into the night air, and everyone joins in chanting blessings for the year to come.

In a final act, many write wishes on paper slips and toss them into the fountains, believing that Aurelia's wisdom will carry their desires to the heavens. The alignment signifies that for this single night, the celestial powers are watching closely, and the people's hopes, dreams, and prayers are lifted directly to them.

#### Districts
As dusk falls on Angel Day, Ilayas transforms into a vibrant tapestry of lights, colors, and sounds. Each district has its own way of celebrating the Celestial Night, with the festivities converging around the serene Tamlem Lake.

#### Upper District
In the Upper District, families and friends gather for feasts in open courtyards or rooftop gardens adorned with colorful lanterns. Musicians play traditional ballads, and storytellers share tales of heroes blessed by the Star of Aegis and the Moon of Aurelia. As night deepens, citizens release paper lanterns into the sky, each symbolizing a hope or wish for the coming year.

#### Port District
The Port District buzzes with energy as the working-class folk and sailors throw lively gatherings. Open-air taverns offer discounted drinks, and street performers—jugglers, fire-breathers, and illusionists—line the cobbled streets, dazzling the crowd. Small, enchanted fireworks light up the sky, while citizens dance and sing along to folk music. Many revelers head down to the lakeside, where they join in a rowdy water parade, illuminated by floating torches and spell-enhanced lanterns drifting on the water.

#### Military District
In the Military District, the celebrations are more subdued yet respectful. Families of military personnel host gatherings to honor those serving or lost, lighting candles by the fountains and statues that pay tribute to the city’s defenders. Veterans and soldiers share stories of bravery, and as midnight nears, a ceremonial march is held, ending with a salute to the celestial bodies aligning above.

#### Common District
The Common District, home to the city’s largest markets, transforms into a sprawling festival ground. Merchants set up colorful stalls, offering everything from roasted nuts and sweets to trinkets and magical charms. Children play games, compete in small contests, and enjoy treats as laughter fills the air. As the alignment approaches, a giant communal feast is laid out, and everyone is encouraged to join in, sharing food, stories, and cheer with strangers and friends alike.

#### Wealthy District
In the Wealthy District, the nobility hosts grandiose gatherings within their estates and along private lakefronts. String musicians play soft, ethereal music while guests indulge in rare wines, exquisite pastries, and fruits imported from afar. Many of the affluent residents hire illusionists to project images of the celestial bodies into the night sky.

#### Around Tamlem Lake
As the alignment draws close, crowds from every district converge on the shores of Tamlem Lake. The lake reflects the stars above, and spellcasters create shimmering displays across the water, illuminating it with light and color. When the celestial alignment occurs, thousands of flower petals are tossed into the lake, creating a colorful, drifting tribute. A quiet pause falls over the city, followed by cheers, blessings, and music that continue late into the night.

#### Inner City
The Inner City is an exclusive, highly-guarded enclave, its grand walls patrolled by elite guards who scrutinize each guest and allow entry only to those of noble or significant social standing. The Veridane family’s ball is the pinnacle of Angel Day festivities, held within their luxurious mansion in the heart of the Inner City. 
### Summary
**8:00 PM – Arriving at the Veridane Ball**

As the players approach the **Veridane Estate**, they are met with a **spectacle of wealth and power**. The **manor's exterior is illuminated by soft magical lanterns**, casting an ethereal glow over the **immaculate stonework** and **pristine gardens**. The air is thick with the mingling scents of **perfumed nobility, fresh roses, and fine wines** being served on silver trays by impeccably dressed attendants.

The **main entrance**, a set of **wide double doors flanked by marble columns**, is open, allowing glimpses of the **lavish ballroom beyond**. The **soft melody of string instruments** drifts out, setting the tone for the evening—elegant and refined.

### **The Players’ First Observations**

As they approach, the players notice that **several guests ahead of them** are being **stopped at the entrance** by uniformed attendants.

🔹 **Nobles and diplomats hand over their weapons without protest**, chatting amongst themselves as they are allowed through.  
🔹 A **stout merchant hesitates**, placing his jeweled dagger in a **locked glass case**, which glows softly with **arcane protection** before he is let inside.  

### **Security Measures – A Test for the Party**

As the players **step forward**, an **attendant dressed in Veridane colors** bows slightly and speaks with **practiced politeness**:

_"Welcome to the Veridane Ball. For the safety and comfort of all guests, we must kindly ask you to leave your weapons here at the entrance. Rest assured, they will be stored under an enchantment that only their rightful owner may lift upon departure."_

If the players hesitate, they observe that:

- The **storage cases shimmer with magical protection**, ensuring security.
- Several nobles retrieve their own **personal signet rings or arcane tokens**, pressing them against the cases to **verify the enchantment’s effectiveness**.
- Any **objections are met with quiet reassurances**, though **armed guards nearby remain watchful** for signs of trouble.
### **Nezoh’s Automaton – Not Allowed Inside**

As the group moves to comply, an **additional restriction is placed upon Nezoh**, whose **automaton companion is halted by a separate attendant**.

_"Apologies, my lord,_" the attendant says, eyes carefully neutral, "_but only humanoid attendants are permitted within the ballroom. We have designated accommodations where your construct may wait safely until the evening concludes."_

If Nezoh resists, the attendant **gestures subtly** toward a **well-dressed noble watching nearby**, who has also left behind a **clockwork butler** in a **similar storage area**.

### **Moving Inside – First Impressions of the Ballroom**

Once inside, the **grand hall opens before them**, an opulent space filled with **nobility, foreign dignitaries, and powerful figures of Ilayas**.

- A **marble staircase leads to the upper levels**, guarded by **two armored guards**, ensuring **no uninvited guests wander the estate.**
- The **ballroom floor gleams beneath the soft glow of chandeliers**, where guests have begun **mingling and exchanging hushed conversations.**
- **Golden-trimmed curtains sway gently** with the night breeze from the **open garden doors**, allowing glimpses of **pristine hedgerows and a blossoming cherry tree** at the center of the estate’s grounds.
- The **rich scent of roasted meats, fine wines, and exotic spices** lingers in the air as silver trays are carried by **silent, professional servants**.

### **8:10 PM – The Players Step Into the Veridane Ball**

As the players **cross the threshold** of the grand **Veridane Estate ballroom**, they are **immediately met with a shift in the atmosphere**—a subtle but undeniable ripple of attention spreading through the gathered nobility.

At first, the **warmth of chandeliers and soft candlelight** bathes the polished floors in a golden glow. The scent of **fine perfumes, roasted delicacies, and the faint spice of exotic wines** lingers in the air, blending with the distant **soft melody of piano strings**.

But as the **doorway’s shadow falls away from them**, they realize—**they have been noticed**.

### **The Moment of Recognition**

A **pause in conversation. A quick glance. A whisper behind a fan.**

Several clusters of nobles and dignitaries, once engaged in their own **political maneuvering, gossip, or flirtations**, **turn their eyes toward the new arrivals**. **Gunther River-Drinker, the newly anointed Champion of Cayden Cailean, is recognized first.**

Some guests do **nothing overt**—just a **flick of a gaze, a knowing nod, a sip of wine taken too slowly.** Others are **less subtle**.

- A **noble** murmurs something behind his gloved hand, prompting **his companions to glance over**.
- A **wealthy merchant’s eyes widen** slightly before he quickly resumes speaking to his conversation partner, though his attention is clearly **elsewhere now**.
- A **young aristocratic woman**, dressed in deep red silk, watches **Gunther openly**, before nudging her friend with an amused smirk.

### **The Conversations Shift – What the Players Overhear**

Their arrival **interrupts nothing, yet alters everything**. The **whispers** in the air take on a new flavor, speculation moving through the room like **ripples in still water.**

**Perception check**

> _"The Champion of Cayden? Here? I thought he’d be in a tavern, not a ballroom."_

> _"Is that the one who passed Cayden's test? How did the Veridanes extend an invitation already?."_

> _"No, no, I heard he was in that small town down south before his ascension. Got involved with some kind of beastly creatures. Surely someone will ask him about it."_

> _"What do you think he drinks? Probably not wine."_ _(Laughter follows.)_

But not all the attention is **mocking or idle curiosity**.

> _"Someone favored by a god? That is no small thing. Perhaps we should see what he knows…"_

> _"If he is here, it means Lord Veridane finds him useful. That, or he is about to be used."_

> _"I’d be careful if I were him. The nobility loves a spectacle, but they love a scandal even more."_


## Scenes & Actors

### **🔷 The Party’s Next Move – A Player Prompt**

🔹 The party **now stands at a crossroads**. They have been **noticed**, and the **first waves of conversation have begun**.

**[Prompt for Players]**  
_"The air around you is thick with speculation and veiled curiosity. You’ve already drawn attention, and now the first figures of influence begin to approach. Do you engage with them openly? Keep your distance?_

### **The Stakes Moving Forward**

- If **Gunther embraces the attention**, he could **cement himself as a figure of importance**—but **what expectations will that bring?**
- If the **party chooses to remain cautious**, they may **delay certain interactions**, but **risk losing control of the narrative about them**.
- The **Gatekeeper is here somewhere**, and the night is only just beginning.




## Notes

## Illusioned guests
### **. Lady Lysandra Calliswyn (Alonian Noble, Secret [[Lysandra]])**

**Illusion Used:** _Veil of Mortal Splendor_ (A permanent glamour that hides her Medusa traits, making her appear as an Aasimar noble.)

- **True Identity:** A **Medusa who once aided House Adella**, now searching for lost artifacts and noble bloodlines tied to their legacy.
- **Motive at the Ball:** Securing **access to relics from the Whispering Tyrant’s wars** and **ingratiating herself with Ilayas’ elite**.
- **Interaction:** Appears as an **elegant scholar-patron**, but those with strong magical perception may notice **slight inconsistencies in how the light catches her features.**

---

#### The Party
Among the noble guests, a woman stands with effortless poise—**Lady Lysandra Calliswyn of Alonia, a patron of the arts, a scholar of lost histories.**

As the **party approaches**, something feels… **off**. Her posture, her presence—so carefully constructed—feels **too perfect**. And then, there is her voice: **familiar, yet foreign**, slipping over words like silk, but carrying the weight of something long since buried.

Lysandra, wine in hand, turns toward them with a knowing smile.

**Lysandra Calliswyn (smiling, swirling her wine):**  
_“Ah. I was wondering if you would find me.”_

The way she says it—**not if they would recognize her, but if they would seek her out**—carries a weight of expectation.

**Party Member (narrowing their eyes):**  
_“Lysandra…?”_

Her smile deepens, just enough to **acknowledge what they already know**.

**Lysandra Calliswyn (softly, inclining her head slightly):**  
_“It has been some time, hasn’t it?”_

___________________________________________________________________________________________________
**Lysandra Calliswyn (gesturing slightly to the grand ballroom):**  
_“But we are far from forgotten tombs and old regrets, my friends. This is a social event. And here, I am **Lady Lysandra Calliswyn**—patron of history, guest of House Veridane, and a woman of fine reputation.”_

She tilts her head slightly, watching them.

**Lysandra Calliswyn (voice light, but firm beneath it):**  
_“And so, you will call me that.”_

**Why** - "I have spent too long watching the world move without me. Now, I move with it.”
**New Name** - _“Alonia is a land of nobility, of lineage, of history written and rewritten by those who know how to shape it. And history, my dear friends, is so very easy to… adjust. The name ‘Calliswyn’ is old, but not too old. Prestigious, but distant enough that no one would dare question my claim. A few forged letters, the right words in the right ears, and suddenly, I was exactly who I needed to be.”_

**Information** - _“Ilayas is a city built on influence, on carefully played hands and unspoken debts. To find what I seek, I must first understand **who truly holds power here.** Not just the nobles in their gilded halls, nor the merchants counting coin, but those who **pull the strings in the dark.**”_

_She leans back, studying them with something between curiosity and expectation._

_“I am here to listen. To watch. To weave myself into the fabric of this city until the answers reveal themselves.”_

**House Adellas Future** - _I am searching for House Adellas to **undo its name.**”_

_Her smile lingers, but there is a sharpness behind it, something colder, more deliberate._

_“They live on—hidden in their wealth, their respectability, their pretense that they were always the noble house they claimed to be. But I remember what they were before. I remember what they took from me.”_

_She exhales, leaning back slightly, fingers tapping idly against the stem of her glass._

_“Ruins do not always crumble by force. There are far more elegant ways to **watch something collapse.** A whispered scandal, a debt come due, a name stripped of its honor piece by piece until nothing remains but disgrace.”_

_Her emerald gaze flickers with something unreadable as she tilts her head slightly._

_“I promised Nezoh I would not kill them.”_ _(A pause, then a smirk.)_ _“And I do keep my promises.”_

_She lifts her glass once more, eyes gleaming in the candlelight._

_“But there are worse things than death.”_

### **2. Toren Vastra, Merchant of the Azure Consortium (Leader of the Jade Gate - [[The Gatekeeper]])**

**Illusion Used:** _Veil of False Flesh_ (A subtle glamour that adjusts facial structure and voice.)

- **True Identity:** The **elusive leader of the Jade Gate**, attending the ball under the guise of **Toren Vastra**, a "merchant with substantial investments in Ilayan trade."
- **Motive at the Ball:**
    - **Assessing Cedric Veridane’s handling of reforms** to ensure they **favor his criminal syndicate**.
    - **Watching foreign players like Tessa Fairwind & Lysandra** for threats to his influence.
    - **Identifying who might pose a danger to the Jade Gate’s operations**.
- **Interaction:**
    - Speaks **softly but with undeniable authority**.
    - Has a **perfectly crafted merchant persona**, yet **his mannerisms are too polished, too rehearsed.**
    - If observed magically, there’s a **brief flicker in his facial features**, suggesting an altered form.

---
**Company Name:** **Azure Consortium**  
**Public Face:** A **well-established trading company** specializing in **rare goods, luxury imports, and private security for merchant ventures.**

#### The party

##### **What He Tells the Party About His Business**

- **The Azure Consortium is an elite trade network** that facilitates **importing and exporting high-value goods across the Inner Sea.**
- They specialize in **discreet transactions, rare commodities, and ensuring that shipments arrive on time, unburdened by unnecessary complications.**
- **Security and efficiency are paramount**—they work with **private security firms to ensure smooth operations** in regions where trade routes are contested.
- **Their partners include Ilayan merchants, noble investors, and international trade hubs like Absalom, Katapesh, and the Shackles.**
- The **goal of the Azure Consortium** is to ensure that **Ilayas remains a thriving trade city by fostering profitable connections.**

---

##### **Why He’s at the Veridane Ball**

- **To strengthen business relationships.** House Veridane is a **major economic player in Ilayas**, and **Cedric Veridane’s reforms** could impact trade. Toren is here to **ensure the Azure Consortium’s interests align with Ilayas' future.**
- **To court new investors.** The Veridane Ball brings together **wealthy merchants, nobility, and foreign dignitaries**—the perfect setting to **expand the Consortium’s influence.**
- **To assess the political climate.** As Ilayas shifts, **he needs to know who holds real power.**
- **To enjoy the finer things in life.** (A convincing but shallow excuse—he enjoys the game more than the luxury.)

---

##### **Possible Questions the Party Could Ask & His Answers**

**1. “What exactly does the Azure Consortium trade?”**

- _A variety of goods—luxury items, rare imports, and high-value commodities._
- _They focus on **difficult-to-acquire resources** that require special handling._
- _If pressed, he keeps details vague, claiming **confidentiality agreements with suppliers.**_

**Blackwake Sentinels** – A no-nonsense private security group specializing in waterfront and trade route protection. They employ former marines and monster hunters to safeguard warehouses, docks, and merchant ships.
**Ironclad Bastion** – A veteran-led security firm that provides heavily armed escorts for caravans and high-risk individuals. They are often contracted by trade guilds moving valuable goods through dangerous territories.

**Vigilant Resolve** (Hired for the ball) – A law-abiding, reputable security guild licensed by the Ilayas Council. They focus on legal enforcement, crowd control, and protective details for nobles and major trade events like the **Celestial Night Festival**.

**2. “You mentioned private security—who do you work with?”**

- _The best that gold can buy._
- _Ilayas is **a trade city, not a battlefield**—but every smart merchant protects their investments._
- _His security forces are **independent firms, licensed and reputable** (a half-truth—many are fronts for the Jade Gate)._

**3. “How do you feel about Cedric Veridane’s reforms?”**

- _Change is inevitable; it is simply a question of **who benefits most.**_
- _A more open economy could bring **great opportunities**—but only if handled correctly._
- _He is here to ensure **trade remains profitable and well-managed.**_

**4. “What’s your history in Ilayas? I don’t recall hearing of you before.”**

- _He has been an **independent merchant for years**, slowly expanding his business._
- _His roots lie in **coastal trade hubs**, and Ilayas is **his next major expansion.**_
- _If they push further, he redirects—**a merchant’s past is less important than his future.**_

**5. “Are you involved in the political side of trade?”**

- _Politics and commerce are two sides of the same coin._
- _He does not make laws—but he ensures that **those who do understand the importance of trade.**_
- _A stable market benefits everyone._

**6. “Why are you personally here? Surely someone else could handle negotiations.”**

- _Some deals **must be made face to face.**_
- _In business, reputation is everything—people must see **who is behind the Consortium.**_
- _A man who hides behind others cannot be trusted._

**7. “And what do you get out of all this?”**

- _Prosperity. Stability. Growth._
- _A merchant's greatest success is **building something that endures.**_
- _He smiles and says nothing more—letting them wonder what else he truly seeks._

#### Tessa
**Tessa Fairwind (smirking):**  
_“Your name’s been whispered along the docks, Vastra. Seems your little Consortium is quite… efficient.”_

**Toren Vastra (casual, setting down a card):**  
_“Efficiency is a necessity in business, Captain. Uncertainty costs gold.”_

**Tessa Fairwind (raising an eyebrow):**  
_“And yet, a little uncertainty keeps things interesting, doesn’t it?”_

**Toren Vastra (chuckling, meeting her gaze):**  
_“Only if one can afford to play.”_

#### Elandra
**Elandra Nightshade (smirking):**  
_“A man in your position must have many admirers, Master Vastra. Tell me, what do you offer that your rivals do not?”_

**Toren Vastra (leaning forward, voice low and smooth):**  
_“Clarity, my lady. A world where those with vision are not hindered by lesser minds.”_

**Elandra Nightshade (chuckling, sipping her wine):**  
_“Ah, but lesser minds are so terribly entertaining.”_

**Toren Vastra (tilting his head, intrigued):**  
_“And what of your mind, Lady Nightshade? Do you prefer entertainment—or opportunity?”_

#### [[Lord Ealdred Corlas]]
**Ealdred Corlas (calm, measured):**  
_“Foreign merchants often come to Ilayas with grand ambitions. Many fail to understand the balance we maintain here.”_

**Toren Vastra (smiling, placing his hands behind his back):**  
_“On the contrary, my lord, I respect Ilayas’ balance deeply. A city thrives not by restricting ambition, but by ensuring those with it find the right paths.”_

**Ealdred Corlas (studying him carefully):**  
_“And what path does the Azure Consortium seek?”_

**Toren Vastra (chuckling, tilting his head):**  
_“One that benefits all, my lord. A rising tide, as they say.”_

#### Seraphina
At the center of the room stands an **exquisite marble statue**, sculpted with breathtaking precision—a noble figure caught mid-motion, draped in flowing robes, their outstretched hand poised as if reaching for something just beyond grasp.

Toren Vastra stands before it, his gloved fingers resting lightly behind his back. He takes in the details—the careful tension in the carved muscles, the intricate folds of the fabric, the unmistakable craftsmanship of a true master.

**Toren Vastra (softly, almost to himself):**  
_“Exquisite.”_

Behind him, **Lady Seraphina Veridane** watches with a faint smile, a half-filled glass of deep amber wine balanced elegantly between her fingers.

**Seraphina Veridane (murmuring, pleased):**  
_“You have an eye for quality, Master Vastra. Many admire, but few truly appreciate.”_

Toren tilts his head, considering the expression of the figure, the way the sculptor has captured something ephemeral—**ambition, longing, perhaps even regret.**

**Toren Vastra (smiling slightly):**  
_“A piece like this—it does not simply exist; it commands. The hand reaching forward… was the artist depicting a grasp for power, or the acceptance of fate?”_

**Seraphina Veridane (stepping closer, intrigued):**  
_“That depends, I suppose, on who is doing the reaching.”_

She sips her wine, studying Toren as much as the statue.

**Seraphina Veridane (watchful, curious):**  
_“Do you see yourself in it, Master Vastra?”_

Toren chuckles softly, shaking his head.

**Toren Vastra (turning to face her, eyes glinting):**  
_“Not at all, my lady. I much prefer to deal in certainties. The artist’s hand may have been guided by interpretation, but in the end, the marble only knows what it has been shaped into.”_

**Seraphina Veridane (arch smile, tracing a fingertip along the statue’s base):**  
_“A practical mind. You are not an artist, then?”_

**Toren Vastra (a small, knowing smirk):**  
_“Oh, I would not say that. I simply prefer my art to be… functional. A well-negotiated contract, a fleet arriving precisely on time, a new venture rising where others failed. Art is not only found in galleries, Lady Veridane. It thrives in the movements of trade, in the precision of power.”_

Seraphina watches him for a long moment, then exhales a quiet chuckle.

**Seraphina Veridane (tilting her glass toward him):**  
_“Spoken like a man who understands both commerce and beauty. A rare combination, Master Vastra.”_

Toren dips his head slightly, accepting the compliment.

**Toren Vastra (raising a brow, glancing back at the statue):**  
_“And you, my lady? Do you see yourself in it?”_

Seraphina trails her gaze over the statue’s outstretched hand, her expression unreadable.

**Seraphina Veridane (softly, almost amused):**  
_“That, Master Vastra, depends entirely on what I am reaching for.”_

A moment of shared silence. The candlelight flickers, shadows shifting across marble and silk.

Then Seraphina turns, her smile effortless once more.

**Seraphina Veridane (gesturing lightly):**  
_“Come, let us continue our conversation somewhere more comfortable. I suspect you have more to discuss than sculpture.”_

### **3. Ambassador Revahl Thornweald (Absalom Diplomat, Secret Spy)**

**Illusion Used:** _Seeming_ (Disguises his scars & true appearance, making him seem younger and more charismatic.)

- **True Identity:** An **Absalom agent**, officially in Ilayas to **observe trade agreements** but secretly collecting intelligence **on Ilayas’ shifting political power.**
- **Motive at the Ball:**
    - **Gather intelligence on Cedric Veridane’s policies** for Absalom.
    - **Identify weaknesses in Ilayas' nobility** for potential Absalomian influence.
    - **Determine whether Ilayas' instability could lead to opportunities for foreign intervention.**
- **Interaction:**
    - Highly **polished and diplomatic**, but his **smile never quite reaches his eyes.**
    - If magic is used to pierce the illusion, his **true face reveals older scars**—likely from past assassination attempts.
    - If directly questioned, **he redirects flawlessly, as if expecting to be caught in lies.**

---

#### The party

##### **What Revahl Tells the Party About His Role**

- He is **Absalom’s appointed diplomat to Ilayas**, ensuring that the **interests of the Grand Council** align with the city’s growing role in regional trade.
- His work involves **facilitating trade agreements, monitoring economic shifts, and ensuring political stability**—all under the watchful eye of **Absalom’s ever-expanding influence.**
- He is here at the **Veridane Ball** because it is **a gathering of the most influential figures in Ilayas**—and where power moves, so too must those who wish to shape it.

---

##### **Possible Questions the Party Could Ask & His Answers**

**1. “Why is Absalom so interested in Ilayas?”**

- **Trade and security.** Ilayas is a **growing economic hub**, and Absalom ensures that its interests are **protected and not undermined by external influences.**
- The city’s **political shifts could create instability**, and Absalom prefers **to be proactive rather than reactive.**
- If pressed, he acknowledges that **foreign interests have taken notice of Ilayas**, and **Absalom is not the only power watching.**

**2. “What’s your stance on Cedric Veridane’s reforms?”**

- Reform is **neither good nor bad—it is a tool.**
- Cedric’s push for **deregulation could benefit certain factions** but also **weaken Ilayas’ control over its own economy.**
- Absalom is **interested in ensuring Ilayas remains stable**, and **any disruption to trade would not be welcomed.**

**3. “You’ve been watching the Council closely. What’s your take on Ealdred Corlas?”**

- Corlas is **a seasoned politician, but even experience does not make one invulnerable.**
- He is **walking a delicate balance between stability and change.**
- **Some on the Council support him. Others wait for the moment to replace him.**

**4. “Do you believe Ilayas is in danger of collapse?”**

- Collapse? No. **Reconstruction? Perhaps.**
- Cities do not fall overnight—they are **eroded over time.**
- **If Ilayas does not control its own fate, someone else will.**

**5. “What of the criminal influence here? The Jade Gate?”**

- **A city with wealth always has shadows.**
- **What matters is not that crime exists, but who it serves.**
- **If those in power cannot keep control, someone else will fill the void.**

**6. “How well do you know Alinya Vilicus?”**

- She is **a voice of neutrality in the Council**, but **neutrality does not mean inaction.**
- He respects **her intellect and patience**, but wonders **what it is she truly seeks.**
- If pressed, he hints that **her father’s influence may still be at play in ways most do not realize.**

**7. “And what do you get out of all this?”**

- **Influence. Stability. Prosperity.**
- A **city that thrives benefits all who invest in it.**
- He smiles and says nothing more—**letting them wonder what else he might mean.**
#### **A Brief Conversation Between Revahl and Aeliana Veridane**

_Location: The Veridane Ball, Ilayas. The air is thick with diplomacy and veiled intentions as Revahl, Absalom’s appointed diplomat, stands near the edge of the ballroom, sipping a fine vintage. Aeliana Veridane, the enigmatic daughter of Lord Cedric Veridane, approaches with a knowing smile, her presence carrying the weight of quiet intrigue._

**Aeliana Veridane:** _"Ambassador Revahl, I was beginning to wonder if Absalom had abandoned its curiosity about Ilayas. You observe much, yet say so little."_

**Revahl:** _"And you, Lady Aeliana, speak much yet reveal even less. A skill, I suspect, inherited."_

**Aeliana:** _"Flattery? Or caution? Either way, my father would be pleased to know you are watching him so closely."_

**Revahl:** _"Your father is shaping Ilayas into something… different. Absalom merely ensures that regional interests remain aligned. That requires careful observation."_

**Aeliana:** _"Ah, ‘observation.’ Such a polite way of saying ‘control.’ Absalom’s reach extends far, but Ilayas is not merely another trade outpost for the Grand Council to mold."_

**Revahl:** _"Not yet."_ _He takes a sip of his wine, meeting her gaze with measured amusement._

**Aeliana:** _"Then I suppose we shall see who shapes whom first, won’t we?"_

_With a subtle curtsy, Aeliana drifts away into the crowd, leaving Revahl with a knowing smirk and a quiet thought: Ilayas is far from a settled gameboard._

#### Alinya
Ambassador **Revahl Thornweald** stands with practiced ease, dressed in **Absalom  navy and gold, the mark of a man who understands both diplomacy and appearances**. Across from him, **Alinya Vilicus**, ever poised yet distant, holds a half-filled glass of deep red wine, her gaze momentarily focused on the distant city lights of Ilayas.

**Revahl Thornweald (smoothly, watching her):**
_“Ilayas stands at a crossroads, Lady Vilicus. A city of trade, ambition, and wealth—yet one that risks being pulled in too many directions at once.”_

**Alinya Vilicus (calm, exhaling softly):**  
_“That is the nature of progress, Ambassador. The challenge is not in avoiding change but in guiding it.”_

Revahl smiles slightly, tilting his glass.

**Revahl Thornweald (measured, watching her):**  
_“That depends on who is in charge of the changes, doesn’t it?”_

Alinya exhales, finally turning to face him fully.

**Alinya Vilicus (calm, but pointed):**  
_“Absalom has always been interested in the ambitions of others. One might wonder if that interest is curiosity… or concern.”_

Revahl chuckles softly, his tone smooth as silk.

**Revahl Thornweald (raising his glass slightly):**  
_“Curiosity, Lady Vilicus, is simply the refined form of preparation. Absalom watches and listens, Lady Vilicus.”_

Alinya studies him for a long moment before speaking again.

**Alinya Vilicus (lowering her glass slightly):**  
_“And what does Absalom feel the need to prepare for?”_

Revahl swirls his wine, watching the candlelight shift in the liquid.

**Revahl Thornweald (casual, but precise):**  
_“Change. Your Lord Minister, Ealdred Corlas, is a capable man, but capable men are often surrounded by those eager to shape their future for them. Lord Veridane’s reforms, the rising interests of foreign traders, even the growing influence of—shall we say—unofficial organizations… Ilayas is becoming something new.”_

Alinya’s expression remains unreadable, but there is a flicker of something in her gaze.

**Alinya Vilicus (soft, thoughtful):**  
_“Change is inevitable, Ambassador. But not all change is welcome.”_

Revahl smiles, but his expression is sharp.

**Revahl Thornweald (leaning slightly closer, voice quieter):**  
_“Which is why those who see the change must decide whether they will shape it… or be shaped by it.”_

A pause lingers, heavy but unspoken. Then Revahl studies her more carefully, and his tone shifts—not pressing, but inquisitive.

**Revahl Thornweald (watching her closely):**  
_“Your father must have some thoughts on this.”_

Alinya’s fingers still around her glass, though her face betrays nothing.

**Alinya Vilicus (measured):**  
_“Archmage Devati Vilicus does not waste words on speculation, Ambassador.”_

Revahl chuckles softly, his gaze flicking to the city below before returning to her.

**Revahl Thornweald (thoughtful, but respectful):**  
_“No, I suppose he wouldn’t. Few men of his standing do. And yet, it is rare to see a mind as formidable as his remain absent from Ilayas' matters.”_

Alinya exhales softly, finally shifting her weight slightly against the balcony railing, gaze flicking toward the stars.

**Alinya Vilicus (careful, but revealing little):**  
_“The Grand Council of Teseon has its priorities. And not all problems require the hand of an archmage.”_

Revahl tilts his head slightly, as if considering her answer.

**Revahl Thornweald (curious, probing just enough):**  
_“But some do. Or rather, some deserve a mind capable of shaping more than just policy.”_

A long pause. Then, Alinya offers a small, almost imperceptible smile.

**Alinya Vilicus (soft, but pointed):**  
_“You assume my father does not already influence the course of things.”_

Revahl’s own smile sharpens ever so slightly.

**Revahl Thornweald (raising his glass slightly):**  
_“A fair point. But influence is like magic, Lady Vilicus—it is strongest when wielded deliberately.”_

Alinya meets his gaze, something unreadable in her eyes, before finally clinking her glass lightly against his.

**Alinya Vilicus (smoothly, amused):**  
_“And patience, Ambassador, is simply a refined form of preparation.”_

Revahl chuckles, drinking deeply.

**Revahl Thornweald (smirking, lowering his glass):**  
_“Then I suspect we are both well prepared.”_

They drink, the conversation moving on, but something remains—an **understanding between those who see the pieces moving on the board, yet choose their next steps with careful deliberation.**

### **4. Lady Vaelessa of Riddleport (Pirate Financier, Arcane Trickster)**

**Illusion Used:** _Glamer_ (Subtle illusion that hides tattoos, alters her accent, and gives her an aristocratic presence.)

- **True Identity:** A **Riddleport crime lord and fence**, attending the ball as an "independent investor" interested in **Teseon’s growing trade power.**
- **Motive at the Ball:**
    - **Secure backdoor deals with Ilayas merchants** to move smuggled goods into the empire.
    - **Test whether Cedric Veridane would accept bribes** to ease restrictions on “gray-market” trade.
    - **Assess Tessa Fairwind as a potential business partner—or threat.**
- **Interaction:**
    - Charismatic and **deliberately unassuming**, but **too careful with her words**.
    - Laughs **too easily** when questioned about her investments.
    - If her illusion falters, **her sailor’s tattoos and a faint Riddleport accent slip through.**

---
#### The party

##### **What Vaelessa Tells the Party About Herself & Her Business**

- She is a **merchant and financier**, dealing in **rare goods, private trade ventures, and strategic investments across the Inner Sea.**
- **Riddleport may be known for its less-than-lawful reputation**, but she is merely **a shrewd businesswoman who understands opportunity.**
- She is in **Ilayas to expand her network, forge alliances, and secure lucrative trade partnerships.**
- **Gold flows where trust is built**, and she prides herself on **knowing exactly where to place her bets.**

---

##### **Possible Questions the Party Could Ask & Her Answers**

**1. “What exactly do you trade in?”**

- _“Opportunities. The kind that others overlook. The kind that require a little finesse.”_
- She speaks of **luxury goods, rare imports, and discreet transactions.**
- If pressed, she **playfully evades specifics**, hinting that **the best traders never reveal their full inventory.**

**2. “Why Ilayas? You have influence in Riddleport—why come here?”**

- _“Because Riddleport is predictable, and Ilayas is changing. And I like to be where change happens first.”_
- Ilayas is a **growing trade hub**, and **where trade thrives, so does profit.**
- If certain **"restrictions” were loosened**, there could be **very lucrative opportunities.**

**3. “Are you working with Cedric Veridane’s reforms?”**

- _“I admire a man who understands that progress requires bold moves.”_
- She sees **potential in Cedric’s vision**, but **only if the right hands guide it.**
- Whether she supports him or **plans to exploit the situation is left unsaid.**

**4. “How legitimate is your business, really?”**

- _“Legitimacy is such a flexible word, don’t you think?”_
- She **smiles, unbothered**, as though the question amuses her.
- _“Every merchant worth their salt knows that rules are only obstacles to those who lack imagination.”_

**5. “Do you deal in smuggling?”**

- _“Smuggling? Oh, darling, what an uncivilized term.”_
- She refers to it instead as **“facilitating trade in difficult markets.”**
- **If pressed, she neither confirms nor denies**—but her smirk says enough.

**6. “Are you working with the Jade Gate?”**

- _“I make it a rule never to ask too many questions about my business partners. It keeps the conversations far more pleasant.”_
- She will not openly **admit to working with them**, but she acknowledges **that all cities have their shadows.**

**7. “And what do you get out of all this?”**

- _“A woman must always be thinking three moves ahead, my dear.”_
- **Wealth, power, and the ability to dictate the terms of the game.**
- She sips her drink with a knowing smile—**the kind that suggests she’s already won something they haven’t realized yet.**

#### Tessa and Davos
Lord **Davos Darquet** sits with effortless composure, dressed in tailored silks that mark him as a man of **old wealth and new ambitions**. Across from him, **Lady Vaelessa of Riddleport**, adorned in crimson and gold, swirls a glass of wine with idle amusement. **Tessa Fairwind**, a pirate who has learned to play noble when the occasion demands, lounges with the easy confidence of someone who commands respect wherever she goes.

**Opening Exchange**

**Tessa Fairwind (grinning, raising her glass):**  
_“Now here’s a gathering they won’t be writing about in tomorrow’s court gossip.”_

**Vaelessa (laughing lightly, tilting her head):**  
_“Oh, I don’t know, dear Captain. I imagine if they did, it would be quite the tale—‘A lady of trade, a lord of fortune, and the Hurricane Queen herself walk into a ballroom…’”_

**Davos Darquet (smirking, setting his glass down precisely):**  
_“And which of us, I wonder, plays the fool in this tale?”_

**Vaelessa (raising a brow, voice silky smooth):**  
_“That depends on who’s left standing by the final act, doesn’t it?”_

Tessa chuckles, eyes flicking between the two with practiced ease.

**Tessa Fairwind (mocking innocence):**  
_“You two are far too serious for a party. Come now, tell me—what is it that truly brings a pirate financier, a lord of Fortune, and a woman of… flexible morals together in the same room?”_

Vaelessa leans in slightly, intrigued.

**Vaelessa (smirking):**  
_“A lord of fortune, is it? And what fortunes does House Darquet deal in, my lord?”_

Davos chuckles, reclining just enough to seem relaxed, but never careless.

**Davos Darquet (smoothly):**  
_“The kind that ensures prosperity, my lady. Ilayas thrives not just on trade, but on the careful management of wealth. I provide the means for merchants, shipowners, and investors to expand their enterprises without unnecessary burdens.”_

**Tessa Fairwind (raising a brow, interested):**  
_“That sounds suspiciously like you make rich men richer.”_

**Davos Darquet (smiling, sipping his drink):**  
_“A common misconception, Captain Fairwind. I prefer to think of it as guiding opportunity toward those with the vision to seize it.”_

**Feeling for Business Interests**

Vaelessa taps her fingers against her knee, considering.

**Vaelessa (softly, watching him):**  
_“And what sort of opportunities are you guiding tonight?”_

Davos offers a measured smile, as if weighing his words carefully.

**Davos Darquet (calmly):**  
_“The kind that reward efficiency. Ships that arrive on time. Goods that pass through the right hands. Trade that flourishes unburdened by obstacles.”_

Tessa chuckles, shaking her head.

**Tessa Fairwind (grinning):**  
_“You make it sound almost poetic, my lord. But tell me, what happens when the wrong hands get in the way?”_

Davos tilts his head, watching her.

**Davos Darquet (with a knowing smirk):**  
_“Then, Captain, we make certain that the right hands are always holding the pen.”_

A brief silence. Then Vaelessa chuckles, lifting her glass.

**Vaelessa (toasting):**  
_“To the right hands, then.”_

**Tessa Fairwind (grinning, raising her own glass):**  
_“And to making sure none of us are the fool in this tale.”_

Their glasses clink, the foundation of future business set in motion.


### **5. Lord Davos Darquet (Teseon Noble, Cultist of Norgorber)**

**Illusion Used:** _Mask of the Living Shadow_ (Makes his eyes seem normal, hides magical markings on his hands.)

- **True Identity:** A **high-ranking cultist of Norgorber**, operating under the guise of a **noble seeking trade alliances.**
- **Motive at the Ball:**
    - **Identify powerful nobles susceptible to blackmail**.
    - **Weaken Ilayas’ political stability** to make it more vulnerable to outside manipulation.
    - **Determine if Cedric Veridane’s reforms create new opportunities for hidden influence.**
- **Interaction:**
    - **Highly charming, always listening more than speaking.**
    - If magically examined, **his eyes briefly darken unnaturally** before reverting.
    - His **gloves hide strange sigils carved into his skin**, visible only when illusion magic is dispelled.

#### The party

**Davos Darquet (raising a brow, voice smooth and measured):**  
_“Ah. And here I thought the evening might pass without our paths crossing. Tell me, what brings you to me this evening?”_
##### **What Davos Tells the Party About His Business**

_“Then let’s not waste words. What do you seek?”_

##### **If the Party Tries to Gauge His Interests First**

**Davos Darquet (smirking slightly):**  
_“Ah, so we are to dance before we speak plainly. Very well.”_

_Slowly, he folds his hands before him._

_“I imagine you are here because you believe I can provide something of value. And perhaps you are right. But first, tell me—what is it that you believe I trade in?”_

- He is the head of **Darquet Trade & Logistics**, a merchant-financier venture that **specializes in trade routes, security, and investment in high-value goods.**
- His **family’s legacy** was built on **finance and commerce**, but he has expanded their influence into **logistics and merchant protection.**
- **He does not sell goods—he ensures they reach their destination unimpeded.**
- **Wealth, to him, is not about coin—it is about control.** Those who can **dictate the flow of trade dictate the course of history.**

---

##### **Possible Questions the Party Could Ask & His Answers**

**1. “What does Darquet Trade & Logistics actually do?”**

- _“A simple question with a complex answer. We provide the stability that merchants crave and the discretion they require.”_
- His company **negotiates trade contracts, secures shipping routes, and ensures that merchants can operate efficiently and profitably.**
- **He does not discuss specific partners—only that those who work with him find it to their benefit.**

**2. “Are you working with Cedric Veridane’s reforms?”**

- _“I work with those who understand the necessity of progress.”_
- Cedric Veridane’s **reforms could reshape Ilayas’ economy, and any shift in power creates opportunity.**
- **If these reforms open new markets, Davos intends to be among the first to capitalize on them.**

**3. “Do you deal with private security?”**

- _“Trade is only as strong as the safety of its routes. We ensure that our merchants do not encounter… unnecessary obstacles.”_
- He employs **legitimate security forces, but the nature of their assignments is selectively discussed.**
- **If pressed, he does not confirm or deny any association with mercenaries or less lawful protection groups.**

**4. “What’s your relationship with the Veridanes?”**

- _“Business-minded, like all things in Ilayas.”_
- He respects **their ability to navigate power**, but **he is not bound to them.**
- **The Veridanes may rule the city, but trade will always be ruled by those who understand its flow.**

**5. “Are you connected to the Jade Gate?”**

- _“I make it a rule to conduct my affairs in well-lit rooms, with respectable company.”_
- He does not acknowledge criminal ties, but he **does not judge those who operate in the shadows.**
- _“Every city has its less savory elements. The question is whether they are useful or disruptive.”_

**6. “Why are you personally at the ball? Surely someone else could negotiate for you.”**

- _“Some things cannot be conveyed through letters. Presence is power.”_
- **Ilayas is shifting**, and he intends to **see firsthand who will emerge as its new power brokers.**
- **He does not wait for opportunities—he positions himself where they will arise.**

**7. “And what do you get out of all this?”**

- _“Continuity.”_
- **A merchant may deal in goods, but a financier deals in influence.**
- **To control trade is to control the city.**
#### Lysandra Calliswyn
_The Veridane Estate, near the grand library._

Lord **Davos Darquet** stands near a shelf of **leather-bound tomes**, idly running a gloved finger along their spines. Across from him, **Lysandra Calliswyn** lounges against a velvet-upholstered armrest, a half-finished glass of wine dangling from her fingertips.

**Lysandra Calliswyn (smirking, watching him):**  
_“Tell me, Lord Darquet, do you always examine books so carefully, or are you searching for one in particular?”_

**Davos Darquet (smiling faintly, not turning):**  
_“Knowledge, Lady Calliswyn, is like a well-kept secret. Sometimes the most valuable pieces are hidden in plain sight.”_

**Lysandra Calliswyn (tilting her head, intrigued):**  
_“Ah, a man who appreciates the unseen. I do wonder—do you collect knowledge for the sake of wisdom, or for something more… practical?”_

**Davos Darquet (chuckling, finally glancing at her):**  
_“A curious question, my lady. But I might ask the same of you. You, who arrived in Ilayas with a scholar’s grace and a noble’s charm—yet seem far more interested in our past than our present.”_

**Lysandra Calliswyn (raising her glass to him, smiling over the rim):**  
_“The past shapes the future, Lord Darquet. And I do so enjoy a well-crafted story.”_

**Davos Darquet (lowering his voice, stepping slightly closer):**  
_“As do I. Though I find the most fascinating stories are the ones their authors never meant to be read.”_

### [[Lord Ealdred Corlas]]

If the **party approaches**, he greets them politely but with a **keen awareness of their presence**—a statesman who rarely engages in frivolous conversation.

#### **What Ealdred Corlas Tells the Party About His Role & the State of Ilayas**

- As **Lord Minister of Ilayas**, his duty is to **maintain stability while ensuring the city’s prosperity.**
- The Council of Ilayas **is not a monarchy—its decisions are made through consensus**, but that does not mean every voice is equal.
- **Ilayas is changing, and not all changes are welcome.**
- His greatest challenge is **balancing Lord Cedric Veridane’s reforms with the need for control.**

---

#### **Possible Questions the Party Could Ask & His Answers**

**1. “How do you feel about Cedric Veridane’s economic reforms?”**

- _“Progress is inevitable, but reckless progress invites ruin.”_
- The **Veridane proposals** for deregulating trade and reducing oversight **may bring short-term gain, but at what long-term cost?**
- **Shifting control from the Council to private interests weakens the city’s ability to govern itself.**

**2. “Do you believe the Jade Gate is influencing Ilayas?”**

- _“I believe that wherever wealth flows freely, there will always be those who seek to claim a portion of it by any means necessary.”_
- He **does not name the Jade Gate outright**, but **acknowledges that corruption is a constant battle.**
- If pressed, he will state that **Ilayas’ leadership is aware of criminal elements**—the question is **how deeply they have embedded themselves.**

**3. “Are you worried about foreign interests controlling Ilayas?”**

- _“Ilayas has always been a city of trade. That does not mean it should be a city for sale.”_
- **Absalom, Taldor, and even the Shackles all have reasons to invest in Ilayas**—but whether they seek trade or control is another matter.
- **He does not oppose foreign investment, but he is wary of those who seek to dictate policy through coin.**

**4. “What is your relationship with Alinya Vilicus?”**

- _“A voice of reason in an increasingly ambitious city.”_
- He respects **her neutrality and insight**, though **he wonders if she will one day choose a side.**
- If pressed, he hints that **her father’s influence still lingers within Teseon’s politics.**

**5. “Do you think Ilayas is at risk of collapse?”**

- _“Collapse? No. But a house does not need to fall to be remade into something unrecognizable.”_
- The concern is **not destruction, but transformation**—and **who will benefit most from it.**

**6. “Why are you here at the ball instead of dealing with these problems directly?”**

- _“Because power is shaped in rooms like this as much as in Council chambers.”_
- He must **see firsthand who moves the pieces on the board**, and ensure that **Ilayas is not steered blindly into ruin.**

**7. “And what do you get out of all this?”**

- _“A city that endures.”_
- His role is **not for personal gain**—it is to ensure that Ilayas **remains strong long after he is gone.**


# Approach the party - Ask about [[Cayden's Chosen]]

## Alinya

From across the ballroom, **the party spots Alinya and Isiril speaking with a cluster of nobles**. The conversation looks civil, but **Alinya’s posture is unusually sharp**, her gestures controlled but precise. There is no idle socializing here—**she is gathering information.**

Isiril, ever the vigilant shadow, keeps a close watch, her demeanor **not of a bodyguard at ease, but of a sentinel on high alert.** Something is off.

When the party approaches, **Alinya’s sharp emerald gaze flickers toward them, and for the first time that night, her expression shifts—just slightly. Relief, perhaps, but also recognition.**

Alinya: Pleasure to see you all again. Congratulations on your newfound glory, Gunther.

Isiril: What are you guys doing here?
_A warning about the ball, It may be an evening of indulgence for most, but It is also **a proving ground. A place where power is tested, where the right words can shift the course of Ilayas.**”_

**Alinya Vilicus (controlled, professional, but with a hint of urgency):**  
_“I have spent the last few weeks reviewing Cedric Veridane’s proposed reforms. On paper, they are framed as ‘economic revitalization’—reducing bureaucracy, increasing trade opportunities, improving Ilayas’ position in the Inner Sea.”_

_A pause._

_“But if you look closer? The implications are… troubling.”_

_She gestures subtly toward the ballroom._

_“Many here either support these changes or have been pressured into compliance. And I believe that some—**perhaps without realizing it—**are serving interests beyond Lord Veridane’s public ambitions.”_

**She lays out the core issues she has flagged:**

**- Loosening restrictions on foreign imports and exports under the guise of "free trade." 
    
- Lowering tariffs on specific goods—primarily luxury items and rare artifacts.
    
- Rewriting customs enforcement policies to shift authority away from the city watch and toward privately owned security firms.
    
- Proposing to privatize certain sections of the harbor and warehouse districts.
    
- Pushing a grant for historical preservation that allows Lady Seraphina’s art gallery, The Elysian Gallery, to receive city funds.
    
- Reallocating funds from law enforcement to “economic and cultural revitalization”
    

  
Cedric ensures these reforms appear beneficial to the public, often presenting them as methods to improve trade, attract investors, and reduce bureaucratic inefficiencies. However, Alinya suspects he might have a conflict of interest, if no other more sinister reasonings.**

### **If the Party Presses for What Alinya Suspects**

**Alinya Vilicus (measured, voice lowering slightly):**  
_“There are too many convenient shifts, too many people acting… unlike themselves. Cedric’s confidence in these policies is unwavering, as if he already knows they will pass without resistance.”_

_She exhales._

_“I suspect that this is either **a well-planned manipulation of Ilayas’ economic policies for personal gain,** or—worse—**something deeper is at play.**”_

**Isiril Adren (arms still crossed, watching the crowd):**  
_“People don’t change overnight without reason. Either they’re being **bought, threatened, or influenced.** We need to find out which.”_

### Alinya vs Cedric

**Cedric:** _"Ah, then you are here to discuss my policies. I should be flattered. The Kenay Order has always preferred to observe rather than intervene. Tell me, Lady Vilicus, what is it you suspect me of?"_

**Alinya:** _"It is not suspicion, my lord, but concern. Ilayas is changing. Your reforms—privatizing the harbors, shifting the watch’s power to private hands, redirecting funds to ‘cultural revitalization’—these are not minor adjustments. You are shifting the very foundation of the city."_

**Cedric:** _"And is that not what leaders do? Stagnation is the true poison. The world changes, and Ilayas must change with it. Or would you prefer we cling to outdated systems while our rivals surpass us?"_

**Alinya:** _"Change is inevitable, but stability is intentional. You speak of progress, yet I see shadows gathering beneath your vision. Power is shifting, but not into the hands of the people. These private security firms—who do they answer to? The council, or their contracts?"_

**Cedric:** _"They answer to efficiency, my lady. The city watch has grown complacent, slow to act when true threats arise. The Jade Gate festers within our walls, and yet your Order, for all its wisdom, offers prayers rather than solutions. Private enforcement ensures the safety of our merchants, our nobles, our prosperity."_

**Alinya:** _"And what of those who cannot afford such protection? Or those who find themselves on the wrong side of a ‘contract’? Justice should not be bought and sold, Lord Veridane. Nor should the lives of Ilayas’ citizens."_

**Cedric:** _"A romantic notion, but naïve. Those who contribute to the city’s wealth deserve its protection. Commerce is the lifeblood of Ilayas—without it, we are nothing but a relic of a time that has long since passed."_

**Alinya:** _"That is where we disagree. Ilayas is not made great by wealth alone, but by its people. They are not mere assets to be protected or discarded at the whims of power. If they come to see your policies as exploitation rather than progress, they will not stand idly by."_

**Cedric:** _"You speak as if they have a choice. The people trust results, not rhetoric. When they see the prosperity these reforms bring, they will embrace them. A few murmurs of dissent mean little in the grand scheme of things."_

**Alinya:** _"Perhaps. Or perhaps you mistake silence for consent. There is a thin line between governance and control, Lord Veridane. And once crossed, it is difficult to return."_

_A pause lingers between them, the music swelling around them like a tide. Below, masked revelers twirl in intricate patterns, oblivious to the battle of words above._

**Cedric:** _"You are as sharp as ever, Lady Vilicus. But tell me—are you here to warn me, or to stop me?"_

**Alinya:** _"That depends, my lord. Are you willing to listen?"_

_A smirk plays at the corner of Cedric’s lips as he takes a slow sip of his wine._

**Cedric:** _"That remains to be seen."_

_With a graceful nod, Alinya steps away, leaving the weight of her words to settle between them. The dance of power continues, and the next move is his to make._

### ** Sir Alistair Greycastle**
Alinya is concerned that one of her allies and supporters has been late and she hasn’t heard from him since the previous day. She suspects that the council member has gone missing. Informs the party of this if the push. The council member Sir Alistair had been adamant into launching an investigation into these add behaviours.

**
**Alinya Vilicus (grim, but focused):**  
_“Alistair was one of the few voices left pushing for an **investigation** into these strange behaviors.”_

_She presses her fingers together._

_“He was supposed to meet with me yesterday. He never arrived. **No one has seen him since.**”_

**Isiril Adren (firmly, with quiet frustration):**  
_“And no one is asking questions.”_

_Alinya nods._

_“Because, we suspect, those benefiting from these reforms want them to pass **without interruption.**”_

### Enlisting the players' help

Alinya & Isiril - we cannot leave, too many eyes on us and too many people wanting to make conversation.
_“But you should be able to move more freely. Find out what happened to Sir Percival. If this is as deep as I fear, then he may have left something behind—**evidence, notes, anything.**”_

**Isiril Adren (glancing between them, voice even):**  
_“And keep an eye on **who stands to gain the most** from these reforms. Someone here knows more than they let on.”_

_Alinya’s gaze lingers on the party for a moment longer, and then she straightens._

**Alinya Vilicus (calmly, but with authority):**  
_“Be subtle. Be careful. And remember—**this is more than politics. This is control.**”_

## [[Aeliana Veridane]]

The **young and ever-curious Aeliana Veridane**, daughter of **Lord Cedric and Lady Seraphina Veridane**, moves through the crowd with the grace of a noble but the keen interest of someone who enjoys stirring the waters. As she approaches, her **emerald eyes gleam with playful curiosity**, a sly smile forming as she takes in the group. **She knows who they are. But the fun is in how they react.**
### **Aeliana’s Opening Approach**

**Aeliana Veridane (smiling, tilting her head slightly):**  
_“Well now, this is a sight to see—a champion of the Drunken Hero himself, standing in the halls of House Veridane. I must admit, I am pleasantly surprised you accepted the invitation. I put quite a bit of effort into convincing mother to extend the guestlist so close to the event. She kept going on and on about the nightmares of the logistics.”_

_She lets the words settle, watching for Gunther’s reaction before shifting her weight slightly, glancing at the others._

_“And of course, I am also delighted to meet the company the Champion keeps. Quite the contrast to the usual merchants and nobles.”_

_She takes a slow sip of her wine, clearly enjoying the moment._

### **Possible Questions Aeliana Asks Gunther & the Party**

#### **1. “So, tell me, how does one become a Champion of Cayden Cailean?”**

- She leans forward slightly, **genuine curiosity hidden beneath a veil of amusement.**
- Is it **a matter of divine favor? A test of courage? Or simply a result of too much ale?**

**(If Gunther boasts about his trials, she laughs, impressed. If he downplays it, she raises a brow, feigning disappointment.)**

---

#### **2. “And does that come with certain… privileges? Or just an insatiable thirst?”**

- **Is Cayden’s favor a blessing, a burden, or both?**
- **Does he feel changed, or is he still the same man?**

_She watches him carefully here—**is he a true believer, or a man who stumbled into godhood’s favor by accident?**_

#### **3. “What does a Champion of Cayden Cailean fight for, exactly?”**

- _“Justice? Freedom? Or just a good time?”_
- She frames the question as **casual, playful**, but **she’s listening for something more.**
- Does he see himself as **a hero? A wanderer? A force of chaos?**

#### **. “And what of your companions? Are they all followers of your... liberating philosophy?”**

- **She turns her attention to the party now.**
- Do they follow him, or does he follow them?
- She wants to see **how they define themselves in his presence.**

#### Humming noise
**Aeliana Veridane (grinning, glancing between them):**  
_“You know, I’ve heard the most **fascinating** rumor.”_

_She pauses, letting the words settle, watching their reactions._

_“It’s said that a certain group of outsiders—**guests in our fair city**—were the ones who uncovered the truth behind that dreadful humming noise.”_

_She tilts her head, eyes dancing with amusement._

_“And I just so happen to be speaking to a certain group of outsiders.”_

_She smiles, raising her glass slightly._

_“So, tell me—should I be thanking you?”_

##### **“And what, exactly, was it?”**

- She wants **details, the juicier the better.**
- _“Ghosts? Rogue mages? Some dreadful old relic?”_
- If the party gives vague answers, she leans in, pressing further:
- _“Come now, I need more than that! You can’t tease me with mystery and leave me wanting.”_

#### Farewell
**Aeliana Veridane (laughing softly, finishing her wine):**  
_“Oh, how I **love** a good story. I must say, you are quickly becoming one of my favorites.”_

_She leans in slightly, lowering her voice._

_“You must tell me more sometime. **Perhaps somewhere less crowded.**”_

_She winks playfully before stepping back._

_“Enjoy the rest of the ball, won’t you? You’ve earned it, after all.”_

#### **If the Party Tries to Avoid the Conversation**

**Aeliana Veridane (smirking, tilting her head):**  
_“Ah, I see. Keeping your secrets, then?”_

_She swirls her empty glass idly, watching them._

_“I do admire a bit of mystery. But secrets never stay buried for long in Ilayas.”_

_A playful wink._

_“I’ll be waiting.”_

_And with that, she steps away, but it is clear—**she will not forget this conversation.**_

## Lady Vaelessa

#### What is she doing at the ball
**Vaelessa (smirking, swirling her wine):**  
_“Trade, my darlings. Always trade. The Veridanes have their fingers on the pulse of Ilayas’ economy, and any merchant with ambition would be foolish not to be listening.”_

_She takes a sip of wine before adding with a smirk:_

### INTRO
Among the glittering guests, one woman, Dressed in crimson and gold,  moves with a different kind of grace—**Lady Vaelessa of Riddleport**. 
**Vaelessa (soft chuckle, tilting her head as she approaches):**  
_“You know, it’s quite the trick—walking into a room and pulling every gaze without saying a word.”_

_She lets the words settle, her lips curving into an easy, amused smile._

_“And yet, here you are, doing it effortlessly.”_

She dips her head ever so slightly—**not a bow, but an acknowledgment**

“Lady Vaelessa of Riddleport.” --- Merchant, investor, occasional enthusiast of fine conversation. And you, my dears, are making quite the impression this evening.”

**Vaelessa (raising a brow, smirking slightly):**  
_“Oh, come now. I’ve spent my life reading rooms, and this one is **reading you.**”_

_She gestures subtly toward a noble couple stealing glances in their direction._

_“Trust me, darlings—whether you **meant** to turn heads or not, you have.”_

_She pauses, then grins._

_“And people like me? Well, we simply **must** meet the ones who keep Ilayas talking.”_

_“I do wonder—are you making a habit of it, or is this all unintentional?”_
#### **What brings you to the Veridane Ball?”**

- _“A social call? Political intrigue? Or are you simply here for the wine?”_
- She asks casually, but **her eyes watch for hesitation.**
- If they give a vague answer, she chuckles.
    - _“Ah, the mysterious type. I do so enjoy those.”_

#### **“And what do you think of Ilayas?”**

- _“A beautiful city, isn’t it? Full of opportunity… for those who know where to look.”_
- She watches their reaction—**are they here to admire, or to change things?**
- If they **criticize** the city, she chuckles.
    - _“Ah, but that’s the fun of it, isn’t it? Cities like this are made to be played with.”_

#### champion

**Vaelessa (grinning, raising her glass):**  
_“Ah, so Ilayas truly does have good taste in entertainment.”_

_She takes a slow sip of wine, watching Gunther over the rim._

_“Tell me, Champion—what’s it like to be chosen by a god who prefers his clergy sloshed and smiling?”_

**Vaelessa (tilting her head, watching Gunther closely):**  
_“Ilayas has always been a city where one earns their place. It’s rare to see someone elevated by divine hand rather than coin or politics.”_

_She leans back slightly, considering._

_“But power is power, isn’t it? Whether it comes from gold, lineage, or a god’s whim.”_

_A pause. Then, with a smirk:_

_“I wonder what you intend to do with yours. If you do excuse me, I have a few other people to meet.”_

## [[Tessa Fairwind]]

_Among the nobility and merchants, one figure stands out—not because she doesn’t belong, but because she refuses to blend in._

**Tessa Fairwind**, the **second-most powerful pirate in the Shackles**, moves through the crowd with the confidence of a woman **who does not need permission to be anywhere.** She carries herself like the wind—**unpredictable, free, and entirely untouchable.**

She has been watching the **party for some time**, particularly **Gunther River-Drinker**, the **new Champion of Cayden Cailean**. And now, curiosity gets the better of her.

With an easy, swaggering stride, she **approaches them**, a **wolfish grin** already in place as she raises her goblet in a casual toast.

### INTRO
**Tessa Fairwind (grinning, taking a swig of wine):**  
_“Now, here’s a sight. A Champion of the Drunken Hero himself, standing in the halls of Ilayas’ finest.”_

_She wipes the corner of her mouth with the back of her hand—not out of sloppiness, but because she’s never cared for pretense._

_“I had to come see it with my own eyes.”_

_She tilts her head, looking Gunther up and down._

_“So tell me, Champion, does the god of drink, freedom, and **not taking things too damn seriously** approve of all this… grandeur?”_

#### **If Gunther or the Party Plays Along**

**Tessa Fairwind (laughing, raising her glass again):**  
_“Good! I’d hate to think a Champion of Cayden would turn up his nose at a fine vintage.”_

_She gestures toward a server and takes another goblet, **offering it to Gunther**._

_“No sense standing around talking about Cayden’s ways if we aren’t willing to **follow them.**”_

_If Gunther drinks, she claps him on the shoulder._

_“Now that’s more like it.”_

#### **If the Party Questions Her Interest in Them**

**Tessa Fairwind (chuckling, taking a seat as if she’s already welcome):**  
_“Well, I have a rule, you see. If I keep hearing the same names whispered around a room, I like to know who they belong to.”_

_She leans forward slightly, grin widening._

_“And you lot? You’re **getting a lot of whispers.**”_

_She takes another drink._

_“So, should I be **concerned**? Or **should I be impressed?**”_

---

#### **If They Ask About Her Own Presence at the Ball**

**Tessa Fairwind (grinning, shrugging):**  
_“Me? Oh, I’m just here for the company. But I didn’t come just to admire the décor or drink the Veridanes’ wine—though I’d be lying if I said that wasn’t a perk.. Maybe I'm looking for a bit of **opportunistic networking.**”_

_She winks, taking another sip._

_“One never knows where the **right conversation** might lead, after all.”_

_I’m here for **allies. Business partners.** One always needs to expand their influence, does it not?”_

_Her eyes flick between the party, watching their reactions._

_“A smart captain doesn’t just steer her own ship. She sees the **tides shifting**, and she positions herself accordingly.”_

_She smiles, a knowing glint in her eye._

_“And let’s just say, I have **big plans.**”_

#### **If the Party Asks About Her Fleet**

**Tessa Fairwind (chuckling, tilting her head slightly):**  
_“Ah, straight to it, I see. My fleet? It’s **the second largest in the Shackles**, and growing.”_

_She leans back, watching them carefully._

_“I command enough ships to make merchants nervous and navies hesitate. Enough **captains willing to follow**, but never so many that I lose control.”_

_A pause, then a playful smirk._

_“I keep my crew happy, my allies well-paid, and my enemies… otherwise occupied.”_

#### **If the Party Asks About Her Goal to Be Pirate Queen**

**Tessa Fairwind (laughing, raising a brow):**  
_“Ah, so you **do** listen to rumors. I like that.”_

_She picks up her goblet again, but doesn’t drink immediately._

_“Let’s just say, **Kerdak Bonefist has had his time.** The Hurricane King sits on his throne in Fort Hazard, drinking and growing **comfortable.**”_

_She takes a slow sip._

_“And comfort, my friends, is **the beginning of weakness.**”_

_A pause, then a sly grin._

_“A true leader knows when it’s time for the tides to change.”_


#### **If the Party Challenges Her Intentions**

**Tessa Fairwind (smirking, tilting her head):**  
_“Oh, don’t mistake me for some upstart with a sword and a dream. I play **the long game.**”_

_She gestures to the ballroom._

_“Why do you think I’m here? A pirate at a noble’s ball, rubbing elbows with Ilayas’ power players?”_

_She takes another sip of wine, watching them._

_“Because power isn’t just taken at sea. It’s won **in rooms like this.**”_

---

#### **If the Party Expresses Interest in Working With Her**

**Tessa Fairwind (grinning, nodding approvingly):**  
_“Now that’s the kind of thinking I like.”_

_She leans in slightly, voice quieter, but still playful._

_“Freedom isn’t given—it’s taken. **And I intend to take mine.**”_

_She tilts her goblet slightly in a silent toast._

_“Perhaps we’ll find ways to be useful to each other, hm?”_


# Ball Events
### **Summary of the Ball’s Progression:**

**Act I: The Grand Reception** → Introductions, rumors, first suspicions.  
**Act II: The Game Begins** → Private conversations, hidden motives, growing tension.  
 **Act III: The Speech & Disruption** → Cedric’s plans are revealed, the first clear signs of danger.  
 **Act IV: The Unmasking** → A conspiracy is uncovered, a confrontation looms, and choices must be made.  
**Epilogue: The Aftermath** → The ball ends, but the consequences will unfold in the coming days.

### **Act I: The Grand Reception (Early Evening)**

📍 _The Arrival Hall & Grand Ballroom_  
🎭 _Theme: Elegance, First Impressions, Measuring the Room_

- **Guests arrive** in waves, greeted with formal introductions by House Veridane’s herald.
- **The players are observed** as they mingle, with eyes following them due to recent rumors.
- **Major NPCs make their rounds**—Cedric Veridane plays host, while nobles and merchants form clusters of conversation.
- **Subtle maneuvering begins**—Vaelessa, Toren Vastra, and other figures are already seeking opportunities.
- **An opening toast** is given by Cedric Veridane, praising Ilayas’ bright future and recent reforms.

**🔹 Key Events for Players to Engage In:**  
✅ **Mingle & Build Connections** – The party can interact with nobles, merchants, and foreign diplomats.  
✅ **Observe the Power Struggles** – Cedric’s allies and skeptics are clear in their body language and discussions.  
✅ **Spot Those Who Stand Apart** – Alinya, Isiril, or others who aren’t simply here to celebrate.

---

### **🔸 Act II: The Game Begins (Mid-Evening)**

📍 _The Ballroom, Private Lounges, and Gardens_  
🎭 _Theme: Hidden Deals, Political Plays, The Web Tightens_

- **Dancing begins**, with nobles and guests partaking in traditional Ilayan waltzes and more lively performances.
- **Private discussions move to quieter areas**—secluded lounges, balcony corners, and the garden.
- **The players are approached** by those interested in their allegiances (Vaelessa, Revahl, Tessa, etc.).
- **Cedric Veridane hints at a speech later**, where he will discuss his vision for Ilayas.
- **Rumors begin to swirl**—whispers of missing figures, uneasy council members, and questionable alliances.
- **A nobleman stumbles out of a private lounge**, clearly shaken from an overheard conversation.

**🔸 Key Events for Players to Engage In:**  
✅ **Learn About Cedric’s Plans** – Find out what reforms he’s pushing through backroom deals.  
✅ **Uncover Secrets** – Listen in on conversations, steal glimpses of documents, or follow suspicious individuals.  
✅ **Engage in Social Combat** – Spar verbally with nobles or financiers attempting to manipulate the conversation.  
✅ **Notice Something Is Off** – Alinya grows more anxious, her allies missing from the crowd.

---

### **🔻 Act III: The Speech & The First Disruption (Late Evening)**

📍 _The Grand Ballroom, Upper Balcony_  
🎭 _Theme: The Illusion Fractures, Secrets Bubble to the Surface_

- **Cedric Veridane takes the floor** for his speech, presenting his vision of Ilayas as a thriving economic power.
- **Applause follows, but some nobles exchange uneasy glances**—not everyone supports this plan.
- **A messenger arrives**, whispering something to one of the council members—**news that unsettles them.**
- **Alinya & Isiril tense up**—something is happening.


#### **Lord Cedric Veridane’s Speech at the Veridane Ball**

_The grand hall falls silent as Lord Cedric Veridane steps onto the elevated platform, his presence commanding the attention of Ilayas' elite. The flickering candlelight casts long shadows behind him as he raises a glass, his voice smooth and confident._

**Cedric Veridane:**  
_"Honored guests, noble allies, and esteemed citizens of Ilayas—tonight, we stand at the threshold of a new era."_

_"For too long, Ilayas has been known as merely a crossroads where wealth passes through but seldom lingers. We have allowed others to dictate our fate—foreign merchants setting our prices, outside forces shaping our laws, and old traditions holding back our progress."_

_"But no longer."_

_"The future I envision is one where Ilayas is not merely a trade hub, but an economic _power_. A city of enterprise and innovation, where wealth is not measured by what passes through our gates but by what _we_ control. Through new reforms, we will strengthen our commercial influence, secure our markets, and ensure that Ilayas takes its rightful place among the great cities of the Teseon Empire."_

_"We will protect our prosperity—not with outdated bureaucracy, but with efficiency. Our security will be in the hands of those who can ensure it. Our docks will serve not just foreign interests, but the ambitions of Ilayas itself. And we will _thrive_."_

_"For those who share this vision, opportunities abound. For those who fear change… I assure you, it is coming, whether you embrace it or not."_

_He raises his glass._  
_"To Ilayas—the heart of commerce, the future of power!"_

_A wave of **applause** follows, but not all are convinced. Among the cheers, **a few nobles exchange uneasy glances**, murmuring in hushed tones. Some see ambition, others see danger. The game of politics in Ilayas is far from over._

**🔻 Key Events for Players to Engage In:**  
✅ **React to the Speech** – Does the party applaud? Challenge it? Speak to those who seem displeased?  
✅ **Investigate the Disruption** – What happened in the garden? Was it an attack or something more subtle?  
✅ **Decipher the Message** – Is it a warning, a call for help, or a piece of evidence about Sir Percival’s disappearance?

---

### **🔺 Act IV: The Unmasking (Late Night, Before the Ball Ends)**

🔹 **First Emotion – Anticipation & Control**  
A hand, smooth and gloved, turns the bauble over. **The Gatekeeper’s touch is patient, deliberate.** They do not marvel at the artifact, nor do they question its significance. The only emotion left behind is **assurance**, as if bestowing this token is no different from moving a chess piece.

🔹 **Second Emotion – Power, with a Hint of Doubt**  
The bauble changes hands—now **held by Cedric Veridane**. Aelwynn feels the shift immediately: where the Gatekeeper was measured, **Cedric is calculating**. A flicker of ambition surges through the resonance, like the tightening of fingers around a dagger’s hilt. But behind the confidence is something else, buried deep beneath layers of arrogance.

**Doubt.**

A moment’s hesitation. A quiet thought **he does not dare speak aloud.**

Aelwynn stumbles back, breathing heavily. The bauble remains still, silent, But he knows better. Lord Veridane wasn’t just given a trinket.
He was given a marker, or perhaps, a leash. And whatever debt it signifies… it has not yet been paid.

---
### Alinya's Echoed of Fate

**Lady Alinya Vilicus** steps forward from the centre of the dais, her voice smooth as velvet over steel.

> "Lords and ladies of Ilayas, honored guests… I beg your indulgence for but a moment."

Her presence alone stills the air. Eyes turn to her, some curious, others cautious. She carries herself like a scholar, like a priestess, like someone who has weighed every soul in the room. Her robes shimmer in celestial hues.

> "We gather to celebrate celestial alignments. But tonight, another alignment has occurred—one, woven in secrecy."


Alinya continues, her words calm—but there’s something underneath, a gathering storm.

> “A token has come into my possession. A trinket seemingly insignificant, yet touched by fate. And like all things bearing the echoes of destiny—it has a tale to tell.”

She lifts her hand.

A shimmer of magic dances across her fingers. There is a collective intake of breath as something begins to **unfold** above her head—hovering where nothing had been moments ago.

An object now **flickers into view**. A spinning sphere of polished quartz that hums softly. Light bends around it, refracting strange images that you cannot place within its crystalline heart.

> “Illumina—an artifact of divination sanctified by the will of Pharasma, goddess of prophecy, fate, and the unbroken river of time.”

> “Within this orb, truths long buried may stir. When guided by divine resonance, it allows us to glimpse not what we desire, but what _was_—a memory etched not by men, but by fate itself.”.”

> “Let us see what memory clings to this token.”

She brings the Illumina to her palm. The light bends toward it, threads of silvery starlight pulled from unseen corners of the room and drawn into the crystal's glow. 

**PERCEPTION CHECK**

**Unseen by the crowd**, **Isiril Adren**, her Warder, moves like a breath through the now shadowed corners. Her form slips from veil to veil, never staying still. She circles the crowd as Alinya speaks, positioning herself behind **Lord Cedric Veridane**, watching his body language like a falcon watches prey.

And then you see Alinya let go of Illumina which hangs still in the air in front of her. Her fingers move in intricate spirals—**somatic signs** older than language, each tracing a constellation through the air. With every motion, silver light gathers, weaving lines between her hand and the Illumina above.

Her eyes close, and her voice voice deepens—not louder, but more layered, as though each word she speaks echoes in a dozen unseen voices. As she intones the divine words in the tongue of angels, the Illumina glows brighter with each phrase, and the air around her tastes of starlight:

> “_Pharasminiel, Aetheri Telin… Lioris estal’mien. Serai’ethiel vos niren. Anel’thurion viandrel_”  
> _(“Pharasma, She Who Weaves... Hear your vessel. Let the veil grow thin. Let fate be unspooled.”)_

The Illumina pulses once—then begins to hum with **divine resonance**, emitting a high, crystalline tone that resonates not in the ear, but in the soul.

She reaches into a silk pouch at her hip and draws forth the **jade bauble**—an unassuming green orb no bigger than a plum.

While all attention shifts to Alinya, Isiril steps closer from the shadows. No spell is spoken aloud. No light flares. But those trained in the arcane—or simply those watching her closely—see the flick of her fingers.An aura briefly glints at her fingertips as **three barely visible, almost translucent threads** leap across the air—_Cedric Veridane_, _Lady Seraphina_, and _Aeliana_ each flinch almost imperceptibly, as if a chill passed through their blood. And then… they **sit still**. Perfectly still.

Their eyes remain open, their breathing calm, but something _wills them into stillness_. It's not paralysis—you see faint movement. But they don't interfere. _Won't._ Their muscles held in check by an external force that brooks no argument.

Alinya never glances at the 3 or at Isiril. She doesn’t need to. She **feels** it—the **snap of magical focus**, the invisible pulse of commitment from Isiril through their shared bond. It's like a chord plucked in her soul, one only she can hear. It tells her all she needs.

Then she places the Jade Bauble in the center of the constellation she drew in the air with magic. The bauble shines as bright as a star inside the constellation., and then with a ripple of light the setting changes:

```A darkened room. Cold stone walls. Torchlight flickering but not revealing. The atmosphere feels submerged—distant, indistinct, like a dream just before waking.

From the gloom, a figure emerges.

They are cloaked in a deep obsidian mantle, its fabric absorbing the light. Their face is masked — expressionless, unmarked by age or gender. Every inch of their form is concealed by enchantment. And yet...

On the high collar of the cloak, woven subtly in dark green against black, is a stylized symbol:  a fortress gate with a keyhole in its center—the unmistakable sigil of the **Jade Gate**.

The figure turns over a small object in gloved hands—a jade bauble, polished and perfect. They regard it not with reverence, but with the impassive grace of someone moving a chess piece across a board.

There is no sound. No breath. But you feel inside you a deep pulse of certainty, control, and something even colder: _ownership_.

And then the vision shifts—
```

```
The ballroom gasps—not because they see a stranger, but because the next face is so very familiar.

ord Cedric Veridane seated at a lacquered desk of dark mahogany within his private study. The man’s features are striking: a strong brow, aristocratic nose, and pale gray eyes sharp enough to cut through silence. He’s dressed impeccably, every line of his attire deliberate, powerful.

The room is softly lit, the only sound the crackle of firelight. Papers are scattered across the desk—economic reports, customs proposals, maps of Ilayas' harbor districts.

Then, an envelope. Black wax seal. No insignia. Cedric breaks it open.

Inside: a single folded letter and the same jade bauble seen moments before. His fingers hesitate for just a second before unfolding the parchment. The audience cannot read the letter’s words—but the effect on Cedric is immediate.

He reads it once. Then again. His brow tightens. The corners of his mouth twitch as if weighing the words against the cost of his soul. He closes his fingers around the bauble—tighter than necessary.

You feel a pulse within you, mirroring Cedric's feelings—_ambition_, raw and burning like coal under the skin. But there’s something else now. 

**Doubt.**

A single moment of hesitation. His lips part as though to speak, but no sound emerges. His hand shakes, just once, before he places the letter down—carefully and pockets the bauble.
```

### After the Vision – Lord Corlas Confronts Cedric

The **vision collapses**, its last flickers fading into the crystalline depths of the Illumina. The ballroom is deathly quiet—no sound but the slow, collective exhale of a hundred shocked witnesses.

**Cedric**, **Seraphina**, and **Aeliana** blink as if waking from a dream. The restraint holding them still has lifted, but the _weight of the room_ has not. That’s when a _measured voice_ cuts through the silence like a blade:

> “You dare bring this poison into the heart of our council?”

The crowd parts as **Lord Ealdred Corlas**, patriarch of the Corlas family and **Head of the Ilayas Council**, steps forward. His voice is deep, resonant, and heavy with restrained fury. Robed in ceremonial crimson and sable, he walks not with haste, but with deliberate purpose—each step echoing against marble.

His gaze is locked on **Cedric Veridane**.

> “You sat beside me in council chambers. You voted on trade reforms. You pledged transparency and economic uplift for our city.”

He stops just short of the Veridanes’ position.

> “And yet, what we saw tonight reveals you not as a reformer, but a _servant_—bound to the will of a masked puppet-master.”

There are gasps and murmurs.

> “The **Jade Gate**, Cedric. You’ve welcomed their rot into our institutions. Into our harbor. Into our laws.”

His voice sharpens.

> “What _else_ have you sold?”

### Cedric Veridane’s Denial

As Lord Corlas finishes his indictment, all eyes fall on **Cedric**.

He stands taller, like a noble lion preparing to swat away a barking dog. (But beneath the surface, there’s a flicker—_panic_.)

> “Lies,” Cedric says, voice sharp and imperious. “Fabricated illusions. Political theater dressed as prophecy.”
> “Lady Vilicus—respected though she may be—has long opposed my reforms. She speaks of fate, but she spins it like any bard in the market.”

He turns to the gathered guests.

> “You’ve all heard the whispers. That I lower tariffs to line my pockets. That I privatize to empower criminals. But none of you have _seen_ such things. Until tonight—when the good Lady conjures an illusion with **no witnesses, no documents, no truth.**”

The crowd shifts uncertainly.

> “And the Jade Gate? That's a mere children’s tale.”

### Alinya Steps In

But Alinya does not flinch. Her expression remains calm. The Illumina still floats beside her, glowing faintly with magic. She lifts her chin and speaks, voice steady.

> “You speak of illusion, Lord Veridane. Yet you looked upon your own hands in that vision. Held the bauble. Read the letter.”

> “You call it a lie. Then let us bring forth the truth.”

She turns—not to the crowd, not to the council, but to the **party**.

> “My friends. You found more than whispers in shadows. You carry what cannot be denied.”

Alinya accepts the letter from the players and she holds it aloft so that all might see the dark seal still intact—the symbol of the Jade Gate etched.

**“No need for your voice, Cedric. The Jade Gate speaks clearly enough.”**

She turns her gaze on him, unwavering.

**“You didn't write it. But you received it. And that’s where your fate was sealed.**

For a moment, there is silence.

And then—

> **“Enough!”**

A **voice sharp with fury and desperation** rings out across the ballroom.

**Lady Seraphina Veridane** , her heels clicking against the marble as she steps beside her husband. Her dress, an elegant cascade of violet silk, now shivers with every breath she draws.

> “This is a spectacle! A stage play written by fools who envy what we've built!”

She points a trembling hand toward Alinya, then to Corlas, then the crowd.

> “We opened Ilayas to the world! We brought art, culture, wealth! And now you turn on us like rats in a flooded hold?!”

She grips Cedric’s arm—tight.

> “We _don’t have to stand here_ and be judged by cowards who hide behind visions and trickery.”
### Cedric Tries to Flee

The illusion of poise **cracks**.

Cedric and Seraphina take one slow step back. Then another. Their eyes flick to the side doors, to the windows. **Then they bolt**— Cedric's hand reaching beneath his jacket.

### Aeliana’s Stillness

**Aeliana Veridane**, standing only a few paces away, does **not move**.

She watches the scene unfold with unreadable calm—hands folded before her, expression caught somewhere between sorrow and resolve.

If anyone looks closely, they might see her lips part, as though to say something...

But she says nothing.

She lets them go.

### Lysandra’s Medusa Gaze

But **Lysandra** is already moving.

Once a prisoner. Now a sentinel.

The medusa’s voice is low, melodic, and unyielding.

> “Do not run, little Veridane. Let the truth look you in the eye.”

### Elandra and Isiril Intervene

**Mistress Elandra Nightshade** glides forward from the periphery of the room like a shadow slipping between candleflames. Her hand is on the hilt of a dagger not meant for show.

**Isiril** comes from the other direction, her blade already halfway drawn.

They do not speak, but they **move** to surround.

### Aftermath of the Exposure

**Cedric Veridane**, restrained and surrounded, no longer wears the mask of noble grandeur. His fine clothes hang awkwardly, the sweat at his temples making the silver in his hair cling to his skin. He glares at Alinya and Lord Corlas with the eyes of a man who knows the game is over—but hasn’t stopped thinking about his next move.

### Lord Corlas Speaks

Lord **Ealdred Corlas** steps forward once more, drawing a deep breath as silence settles like dust after a storm.

> “The Council of Ilayas will convene at first light to deliberate charges of **conspiracy, treason, and corruption**. Until that time, Lord Cedric and Lady Seraphina are to be **held under guard**, stripped of authority, and barred from council chambers.”

He turns to Alinya.

> “Lady Vilicus. You have done this city a service that history will not forget.”

A soft murmur of agreement rises through the nobles and ambassadors gathered—some out of genuine admiration, others simply to _be seen_ agreeing with power.

### **🌊 Epilogue: The Ball Concludes**

📌 _Guests begin to leave, but Ilayas will not be the same after this night._

- **The Jade Gate’s presence is now undeniable—whether exposed or still lurking in the shadows.**


### Final Moments – The Festival Continues… Uneasy

Outside, fireworks still bloom across the sky—bright, beautiful, and _utterly indifferent_ to what has unfolded inside.

The **Celestial Night Festival** continues.

But the city of Ilayas has changed forever.


### Recognition Ceremony – Lord Corlas Addresses the Party

As the guards begin to escort Cedric and Seraphina away, the ballroom remains tense, filled with the quiet rustle of silks, murmurs, and the unsteady hush of shocked nobles. But then Lord **Ealdred Corlas** turns back to the dais, voice rising once more—not with condemnation this time, but with _gravitas_.

> “Tonight, we bore witness to a great unmasking. Deceit, long hidden beneath noble silk and silver coin, has been dragged into the light.”

He pauses, letting the weight of his words settle.

> “But it was not the council, nor the courts, nor even the gods alone who delivered us this truth.”

He turns fully to the party now—his gaze heavy with respect.

> “It was **you**.”

> “You who stood between shadow and flame. You who followed the thread of conspiracy through whispers, dead ends, and danger. And when confronted by masks and lies, you did not waver. You uncovered what others dared not see.”

He gestures for the players to step forward before the gathered nobles.

> “By the power vested in me as Speaker of the Ilayas Council, I offer you **the city’s gratitude** and the **Council’s blessing.**”

A steward steps forward, offering the party a velvet-lined case or satchel (your choice of ceremonial token—see below).

> “Let all present bear witness: from this day forward, you are recognized as **Trusted Agents of Ilayas**, bearing the authority to speak and act in defense of its people, under the seal of the Council.”

A round of applause begins—slow, hesitant from some, but then swelling as others join. Even among the masked political figures and foreign envoys, **respect must be paid**.

#### **The Sigil of Ilayas**: 
A platinum pin in the shape of a crescent moon over a river. Grants +1 status bonus on Diplomacy checks within the city and with any official council member.


#### You are recognized as Trusted Agents of Ilayas…"

 The party is now officially recognized as **trusted allies of the city**, not just freelancers or adventurers passing through. They're **endorsed by the city’s ruling body** (the Council of Ilayas).
 It grants them **moral and legal authority**—they can now:

- Investigate threats to Ilayas with legitimacy.
- Be called upon (or volunteer) to intervene in civic or magical crises.

They’re essentially **honorary enforcers or special envoys**, but with flexibility.

### In the Chaos…

But while all attention is on the fallen Veridanes—**not all snakes are caught**.

In the periphery, past the edge of the lanternlight, a figure in robes of ocean-silk and lapis trimming glides between clusters of distracted nobles. A man with no title on the council, yet whose gold funds half the trade flowing through Ilayas' private harbors.

**Toren Vastra**—the Merchant Prince of the **Azure Consortium**.

He adjusts his collar, his expression unreadable beneath his perfectly trimmed beard. In one hand, a folded fan. In the other, a signal ring—a crest faintly etched in aquamarine.

No one sees him leave.

Or at least, no one stops him.


## Veridane Ball Guest List:

New figures at the ball 

- Lady Lysandra Calliswyn - Alonian Noble patron of the arts and scholar of lost histories.
- Captain Tessa Fairwind - the second-most powerful pirate in the Shackles,stand out not because she doesn’t belong, but because she refuses to blend in. Has a reputation of crashing parties, although Bertie and Fleur never attended the same parties.
- Toren Vastra - Merchant of the Azure Consortium, a trading company specialising in rare goods, luxury imports, and private security for merchant ventures.
- Gunther River-Drinker (played character) - an odd last minute addition to the party list at Aeliana Veridane's insistence. An orc newcommer in the city who has recently passed the "Cayden's Challenge", an annual trial during the Celestial Night festival where anyone is welcome to try and retrieve Cayden's (God of bravery, ale, freedom and wine) sword from the stone the god placed it in. Rumours have it that Gunther pulled the sword with the stone surrounding it, and now it's more of a mace? - it is unclear, needs confirmation.

Known guests

- Ambassador Revahl Thornweald - Absalom’s appointed diplomat to Ilayas, ensuring that the interests of the Grand Council align with the city’s growing role in regional trade.
- Council members: Lord Ealdred Corlas, Chancellor of Ilayas; Lady Isolde Ravenshadow – Minister of Arcane Affairs; Dame Elara Swiftbrook - Mistress of Culture and Arts; Ambassador Elenor Vale - Guild Representative; Duchess Leonora Emberwood - Protector of Wynsend Forest; Sir Thaddeus Lightbringer - High Justiciar --- Missing: Lord Alistair Greycastle - Minister of Health and Wellbeing
- The Mistress of Revels, Elandra Nightshade - High Cleric of Calistria who provides insight into clandestine affairs and ensure that the council is informed of potential threats. Fleur has crossed paths and exhanged information in the past
- Lady Alinya Vilicus - Representative of the Kenay Order, Grandmage and politics mediator
- Lady Aeliana Veridane - daughter of Cedric and Seraphina Veridane, known socialite but has shied away from politics, preferring hosting and attending social events, acquintace of Fleur
- Lady Vaelessa of Riddleport - Pirate Financier looking to secure deals with Ilayas merchants to move smuggled goods into the empire.
- Lord Davos Darquet - Teseon Noble that Fleur knows very well as they attended many functions together. One of the most sought bachelors in Ilayas. He is the head of Darquet Trade & Logistics, a merchant-financier venture that specializes in trade routes, security, and investment in high-value goods. His family’s legacy was built on finance and commerce, but he has expanded their influence into logistics and merchant protection.