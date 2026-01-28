---
tags:
  - Quest
art: z_Assets/Misc/PlaceholderImage.png
adventure: "[[Ilayas Job Board]]"
whichparty: "[[Party]]"
status: ❌
location:
  - "[[Ilayas]]"
NPC:
  - "[[Elandra Nightshade]]"
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
As PCs plunge deeper into Ilayas’s occult underground, should lay the groundwork for later plot points by using dreams to introduce mysterious elements that hint at things to come. In these dreams, PCs always find themselves on the distorted streets of Ilayas, its towering, overgrown tenements looming overhead.

Strange flittering shapes peer from dark alleyways and the forms of other dreamers staggering wearily through the landscape. PCs should never appear alongside each other, and should emphasize on their initial isolation in this strange realm, though they appear within shouting distance of one another or from different vantage points to witness the same events. 

The dreamscape is an increasingly dangerous place. Dreaming PCs should not initially have harrowing nightmares every time they sleep, but they should at least witness the dangers firsthand: baying shadow mastiffs, throat-slitting vulnudaemons, swooping nightgaunts, and surprising fissures that open to swallow dreamers. A brief-yet-intense narration of a dream should suffice to set the stage for PCs and highlight the threat they face for the first few days of their investigations, before they seek assistance from Alinya Vilicus who can offer some protection to slumbering PCs (see page 10).

### Dreamscape

The first thing you feel is the cold. Not of weather—but of absence. Light, warmth, certainty… all gone. You awaken alone in unfamiliar streets, the cobblestone beneath your feet slick with mist that clings to your boots like cobwebs. The air is thick with the scent of mildew, rust, and something sweetly rotten—like fruit left too long in the dark.

Shadows curl around the corners of crooked rooftops, and every lantern post leans just a little too far. The buildings, familiar yet wrong, seem to lean inward as if listening. You're somewhere in a city, but the city isn't yours. It might once have been.

You hear voices…
A child's distant, high-pitched laughter—cut short.
The honking giggle of something massive and wrong, echoing from an alleyway too narrow to hold it.
The dry, brittle cackle of a crone, bouncing from rooftop to rooftop like she's above you—everywhere and nowhere.

The mist hangs thick in the air, veiling your vision to no more than forty, maybe fifty feet. Beyond that, the world fades into a trembling grey. The silhouettes of buildings twist with the fog, and shapes seem to move through the haze, though they vanish the moment you try to focus.

And then you realize… you're alone. None of your companions are beside you. Not in voice, not in step. Each of you has awakened in a different part of this impossible city. 

**The VOID**
As you step beyond the edge of the broken street, the city’s fall behind… and something else takes hold.

Not silence—noise. Endless noise.
A static roar floods your ears, not loud in volume but in totality. Like every sound you've ever heard stacked atop itself, stripped of meaning, fed through shattered glass, and poured directly into your thoughts. It drowns out your heartbeat. You can’t tell if your friends are calling to you—or if the sound is inside you now.

The air grows sharp, not cold, not hot.. It’s like breathing in a memory that wasn’t yours, and choking on it.
Vision contracts. The edges of your sight bloom with phantom shapes and flickers of impossible color. Everything around you judders, like a failing spell.

Every instinct screams at you to get out. But something here—something buried under the static—is watching to see if you’ll stay.


**HAG**
A gaunt silhouette looms just beyond the curling mist, hunched and bone-thin beneath a mass of tangled, midnight-black hair. Her long limbs move with inhuman grace, jointed all wrong, each finger tipped with a claw like a rusted hook. Hollow white eyes shine through the gloom, seeing not the world, but the dreams behind your eyes. Her toothy grin splits a face drawn tight as leather—an ageless mask of mockery and hunger. The air around her hums with whispers you can't quite understand, each step she takes making the shadows twitch as if in fear. She does not walk through the dream; she drags it behind her like a veil of sorrow.



**BLOBBY**
You hear it first—an echoing honk, warped and distant, followed by a giggle that curdles the blood. Then, from behind the warped scenery of this dreamscape, lumbers a horror wrapped in pink flesh and polka dots. Its form bobs and jiggles grotesquely, as if it’s barely holding together. Its bulbous eyes bulge wide and wet, and its grin—so wide it splits its face—shows rows of jagged teeth like a shark’s. Its clownish bowtie is soaked red at the tips, its steps leaving puddles of something sticky and wrong. This thing shouldn’t exist, and yet here it is... waving. It sees you. It’s delighted. And it is very, very real.

**Mirrorwight**
Born from broken identity and nightmare anxiety, a Mirrorwight is formed when a dreamer’s self-image is too fractured to reconcile. It manifests as a twisted version of the observer—and reflects not how they are, but how they fear to be.

**Lanternskin**
A pale figure drifts through the fog, its body barely more than parchment-thin skin stretched into the rough shape of a robed person. Inside, a bluish flame writhes where its heart should be, casting long, shifting shadows with every motion. Its face is featureless, save for two sunken voids where eyes should burn. As it moves, you feel an inexplicable warmth… and an overwhelming sense of loss. The light beckons you to follow—without thought, without will, without return.



### Shiver
Shiver is a potent, hallucinogenic drug made from the processed venom of the dream spider. It is generally ingested after which the user falls into a deep slumber filled with vivid dreams. While asleep the user generally shakes and shivers, which is where the drug earned its moniker.

The venom of the dream spider has highly hallucinogenic properties, to which anyone who has ever been bitten can easily attest. It is not addictive until it is boiled in a mixture of alcohol, water, and the spider's webbing. The process is quite time-consuming and difficult, requiring a competent alchemist. Once distilled in this way it becomes highly addictive, and a user must take shiver on a weekly basis or suffer severely adverse consequences to they mental well-being.

Desperate individuals have even been known to track down dream spiders in their lairs in Wynsend Forest to let themselves be intentionally bitten, a dangerous proposition at best. Dream spiders are native to the Allanar and were specifically imported for the sole purpose of harvesting their venom. Since that time, many have escaped captivity, and now nest in the Wynsend Forest.

#### Secret information not privy to the party:

Shiver users experience augmented effects (in addition to the drug’s normal effects) while under the drug’s influence within the creeping
radius of the dreamstone. Users that fall asleep under the drug’s effects become lucid dreamers, allowing their lucid bodies to enter
Ilayas' dream realm overlay for 1d4 hours, with all the abilities afforded lucid dreamers. Those intoxicated by the drug ignore the
incorporeal quality of dream haunts. Additionally, while in the dream realm, they can use a successful Charisma check to channel positive energy as a cleric of the lucid dreamer’s character level in order to damage the dream haunt. Those who instead gain immunity to fear for
1d4 minutes after taking the drug experience an additional lingering side effect for 1d4 hours. In this somnambulistic state, users gain the staggered condition and are under the effects of see invisibility, which allows them to perceive the fog-shrouded dimensional overlay
of Ilayas' dream realm. All forms of the creature’s vision are reduced to 10 feet, and most users disregard the strange passing creatures and landscape distortions as vivid hallucinations. 



### Background
The events of Earthfall affected not only Brightwyn, but also portions of the Dimension of Dreams where the falling fragments were no less deadly. The goddess Desna intervened on that plane in ways not possible in other realities. Yet one meteor, silent and slow, plunged into an ephemeral demiscape, where it tore through one reality and into another, coming to rest not in the realm of dreams, but in the waking world. Desna’s emissaries clandestinely collected this fragment from a deep crater in the Wynsend Forest. This dreamstone passed secretly among her clergy for thousands of years, their actions recorded in a secret journal known as the Paginarum Lethargica. The taint of nightmare could not be entirely erased from the reality-warping stone, however, and the dangerous meteorite was locked away in a shrine 2 centuries ago.

Those few aware of the stone’s existence sought it desperately. One such entity was Mog-Lathar, a Leng spider who slipped through the weak borders of reality around the meteorite’s flooded crater. The creature’s efforts were thwarted by the deadly spears of fey hunters, and its slain body settled into the crater’s sediment, where it waited, dead but dreaming, bathing in the warped energies of the dreamstone.

Two decades ago, an obsessive collector and occultist named Nahum Caligaro rediscovered the Paginarum Lethargica in his family’s library. Nahum, his lover, Myra Lombroso, and the son of their aristocratic sponsor, Stainton Drune, soon set out on an expedition to unearth lingering fragments from the meteorite’s impact crater. Though they found none, they uncovered the fossilized remains of Mog-Lathar. Soon the warped remnants of the petrified Leng spider awakened and began whispering foul temptations to its saviors, promising immortality in exchange for freedom.

They chiseled the fossil free and packed it for selling to interested collectors, but the relic never arrived. Nahum and Myra succumbed to the temptations of the spider’s promising whispers. They abandoned Stainton and the others and secreted the fossil away,  Establishing the Brotherhood of the Spider, a cult formed around the idol’s worship. 

Since that time, the scorned Stainton Drune has grown old and bitter at the unfulfilled offer of immortality. Drune has since used his position as a Magistrate in Ilayas to seek out the hidden cult. The Brotherhood of the Spider has grown, becoming cunning and potent. In return for worship and supplication, the idol Mog-Lathar has gifted its followers with their promised rewards, including immortality to its most faithful. The Brotherhood has also gained significant influence over Ilayas’s shiver trade, using the profits earned by selling the drug to fund increasingly elaborate ceremonies of supplication to the hungry idol.

As part of his obsessive study, Nahum discovered that the dreamstone’s final resting place lay just below the foundation of his family’s ancestral manse—now his cult’s headquarters. Nahum found the object shielded in a deep well. Mog-Lathar grew jealous and feared Nahum might use the stone’s power to destroy the Leng spider’s remains. Secretly, the idol ordered his high priestess, Myra, to betray her lover by disrupting an occult ritual meant to awaken the dreamstone. As a result, Nahum, his initiates, and the dreamstone itself were drawn into the Dimension of Dreams, cut off from the Paginarum Lethargica and an important ritual component known as the Clavis Somnus in the waking world. Both the book and the key were soon stolen by the cult’s new hired enforcers, Barvasi’s Band. Without the tome’s knowledge of the dreamstone and the mithral key needed to reverse the ritual, the artifact has grown wildly out of control, and Nahum and his initiates have warped into nightmarish forms flush with power. They seek revenge on their former cult and the recovery of the Paginarum Lethargica so that they may return to the material world and again take both the dreamstone and the petrified idol as their own.

Nahum and his group are now using the stone’s power to reclaim their old cult by murdering its acolytes within their nightmares. Now, the stone’s strange world-merging energies have brought dreams too close to reality, and reality too close to dreams, creating a stable pocket dimension. The dreamscape is twisting beyond Nahum’s control, and bizarre, inexplicable deaths have caused Ilayas’s residents to suspect some strange new nightmare plague.

Worse yet, the district’s desperate shiver addicts have found their lucid dreaming gives them surprising control over the new dreamscape, and the dreamstone’s new masters find themselves fighting a war on two fronts: on the streets of Ilayas, where they battle to assume control over their former cult’s enterprise, and in the dream realm, where the nightmare creatures who carry out their bidding are forming plans of their own. 


### Trigger Report

[[Veil of Shadows Operative Brief – Subject Inquiry Rogi, Mavik, Serena]]


### Dreams/Research

[[Desna]]

Desna is the **goddess of dreams, stars, travel, and luck**—also called the **Song of the Spheres**, **Tender of Dreams**, or **Starsong**. Her symbol is a **butterfly with starry wings**. Her priests are often wanderers, poets, musicians, or interpreters of dreams. She opposes entities that twist or corrupt dreams—especially **night hags**, **Nightmare Lords**, and the demigod **Ghlaunder**

>“She walks in every dream we don’t remember—and watches the ones we do.”

She doesn't control dreams, she **tends** them. Like a gardener. Her presence ensures that the Dimension of Dreams remains a place of **beauty**, **growth**, and **self-discovery**, rather than one consumed by **nightmares**, **fatalism**, or the **Nightmare Lords**.

She is not a goddess of fixed prophecy. She allows for **choice**, and encourages mortals to shape their own fate within dreams.

#### 1. **Normal Dreaming (Monadic Soul Projection)**

- All mortals project their **monadic soul** into the **Dimension of Dreams** while sleeping.
    
- This is called the **lucid body**—a psychic reflection of self shaped by the dreamer’s subconscious.
    
- The dreamscape formed is an **ephemeral demiplane**—a personal bubble that fades upon waking.
    
- **Not physically real.**
    
    - Spells cast aren’t used up.
        
    - Wounds don’t last.
        
    - Death simply wakes you up.
        

> Desna _allows_ this by divine law—it is natural, safe, and meant to **refresh the soul**.

---

#### 2. **Lucid Dreaming**

- With the **Lucid Dreamer** feat or certain drugs (e.g., _shiver_), a dreamer gains **control** over their dream.
    
- You may:
    
    - Alter the dream.
        
    - Attempt to perform **“impossible feats”** with Charisma checks (conjuring items, flying, etc.).
        
    - Interact more meaningfully with recurring dreamscapes or others' dreams.
	    
	- A lucid dreamer’s spell slots and magic item charges used on the dream realm are similarly consumed in the waking world. Most importantly, lucid dreamers in certain nightmarish dreamscapes that are killed while dreaming also die in the real world.
        

> This is the path of **prophets, psychics, and Desnan seers**—those who awaken within the dream and shape it with purpose.

---

#### 3. **Dreamwalking (Physical Entry into the Dream)**

This is **rare**, **powerful**, and **dangerous**.

- The body physically enters the **Dimension of Dreams** using special magic (e.g., _dream travel_, _breach the veil of dreams_).
    
- This bypasses the need for a lucid body—you are **you**, in flesh.
    
- **Everything becomes real**:
    
    - Magic is expended.
        
    - Injuries persist.
        
    - **Death is permanent.**
        

#### 📜 Desna’s View:

- Desna **permits** dreamwalking but does not encourage it without **preparation**.
    
- Her agents and the Kenay Order treat it like **pilgrimage through the stars**—dangerous but sacred.
    
- Those who enter the Dream unprepared risk attracting **Nightmare Lords**, **animate dreams**, or worse.
    


## Story

### Act I: “Web of Ghosts”

#### **About Frell Tann (Ilayas Context)**

- A **noble-born  (good for nothing)**, Frell is the **nephew of Magistrate Garrick Tann**, one of Ilayas’s most hated officials (Magistrate of Commerce).
    
- Known for his heavy shiver addiction and mercenary ties to **Barvasi’s Band**, Frell participated in the **theft of the Paginarum Lethargica** from the Brotherhood's temple complex.
    
- Days prior, Frell fled into the dreamscape during a lucid bender and never returned. His dream-self was hunted down by one of **Sally Scrabblebones’ spawn**, and now his **physical body shambles through Ilayas**, animated by something born of nightmare.
    

---

#### **Encounter: Frell's Dreamspawn**

> The midday light has dimmed—not by clouds, but by a strange, creeping fog that snakes low through the alleys of Ilayas. It moves unnaturally, curling in tendrils along the cobblestones as if hunting. Screams echo off the sagging rooftops above, warped and distant through the haze. Something is happening.

> As you round the corner into **Canebrake Plaza**, the fog thickens to a near-wall. Then—movement. A figure stumbles backward from the mist—an Ilayas guard, bloodied and wild-eyed, swinging a cracked halberd in panic. Behind him, dragging forward through the vapors, is... _something_.

> It’s a body—gaunt and grotesquely twisted—half-devoured, ashen gray, its limbs reduced to sinew and exposed bone. And from its **distended, torn-open jaw**, a **shapeless fog-creature slithers**, like mist poured from a corpse’s mouth.

> You hear the sound of bone scraping stone as the corpse lurches forward, marionetted by the writhing cloud that exudes from its own throat. The stench of death and rot floods the air.

> Nearby, **three more guards lie scattered across the paving stones**, unconscious or worse, eyes frozen wide in terror. The lone survivor locks eyes with you and shouts, "Don’t let it—don’t let it take them too!" before being flung aside by an unseen force.

> The fog pulses with malevolent intent. Something about it feels _wrong_—not just undead, but unreal. Dream-born.

> It sees you now.
**Guard**: **Corvin Glais**

**Creature**: _Dreamspawn Hungry Fog_
- Appears as a **billowing fog** dragging Frell’s half-devoured corpse.
    
- Frell’s **distended jaw** hangs wide open, torn in half from the inside. From it pours a sentient, misty ooze.
    
- Combat begins with a **single surviving Ilayas guard (Corvin Glais)** ineffectively fending it off, while **three others lay injured** nearby.
    
- The creature uses negative energy, discordant auras, and fear effects.

#### **Aftermath & Scene Details**

After defeating the creature, several key details become clear:

- **The corpse is disturbingly ashen**, almost **leached of color**.
    
- Frell’s **head is wrenched back unnaturally**, the jaw ruined by the dream-creature’s exit.
    
- His **left leg and arm have been gnawed to the bone**—clearly by something other than the fog (a hint toward his time in the pigsty behind **Rook’s Roost**).
    
- The only remnant of his noble heritage is a **torn red silken undershirt**, still clinging to his corpse.
    
- Attempts to **cast divination or Speak with Dead** fail—his soul is devoured or missing entirely.

#### Development:

> _Heavy boots echo on stone as a group of uniformed Ilayas guards jog in from the east. At their head is a broad-shouldered man with a severe jawline and streaks of gray at his temples. He takes one look at the scene—Frell’s corpse, the scattered guards, the curling residue of unnatural fog—and curses under his breath._

**Captain Crandon**:  
“Gods below... again?”

Shortly after the fight, **Captain Steven Crandon** (LN human fighter 7) arrives. 

- Severe in bearing, with armor half-polished and an ever-present frown.
    
- He quickly checks on his men, then eyes the PCs.
    

> “You recognize the corpse, don’t you?” he asks one of his guards, just loud enough for a perceptive PC to overhear (DC 15 Perception).  
> 
> 
> Once confirmed, he approaches the party:
> 
> “My men say you handled yourselves well. Ilayas could use folks like you. More would have died if you hadn’t stepped in. If you’re willing to keep helping, I can arrange introductions that’ll give you the authority to make a real difference around here.”



**Crandon**:  
“There’ve been rumors. Whispers about dreams killing folks. We’ve seen the bodies—colorless, twisted, but no signs of magic. No soul left to question.”

“Yeah. We’ve had bodies. A dozen at least. Ash-gray, eyes wide, no wounds we can explain. All shiver users. Found one slumped against a lamppost, grinning like he’d just seen Pharasma herself. Another with bite marks all over—tiny ones, like spiderlings. The wounds all point to suicide and overdose. But that's more than your usual suicides though."

_He glances down at the twisted corpse of Frell Tann._  
“This one’s different. But it fits. The look, the rot. It’s just... worse.”
**If asked about the corpse**:

> “He wasn’t important—but his uncle is.”.

If the party agrees, Crandon personally **escorts them to City Hall** in the **Old Quarter**, to meet with **Magistrate Stainton Drune**.

#### Crandon: On the Magistrate

> **Crandon (cautious):**  
> “Drune? Civic Order Magistrate. One of the top dogs in Ilayas. Oversees urban crime, narcotics, that sort of thing. You could say this is his jurisdiction.”
> 
> _He folds his arms, studying the players a moment before adding:_  
> “He’s ambitious. Political. Likes to make his own calls—and doesn’t like questions.
---



---

### 📜 Act II: “Nightmare Credentials”

#### Meeting with **Magistrate Stainton Drune**:

- Offers formalized authority, reward (800 gp), and a mission: trace Frell’s death back to its source—dealer, drug, cult.
    
- Mentions that "his office believes" a cult is poisoning wells and triggering nightmare-fueled suicides.
    
- Clearly has ulterior motives—his tone is desperate but practiced.
    

#### Leads Provided:

- **Frell’s den** was the **Rook’s Roost**.
    
- Addict allies: **Reynaldo, Nomi, Langston** at **Fever Dream Alley**.
    
- Possible link to dealer **Moses Greeley**.
    

---

### 🕷️ Act III: “Haunts in the Alley”

#### Location: **Fever Dream Alley (CR 8)**

- Mavik and Serena were part of this group.
    
- PCs meet Reynaldo, Nomi, and Langston—semi-lucid addicts still tormented by dreams.
    
- Dream Haunt Manifestation:
    
    - Langston convulses, releases spider swarms.
        
    - _Vomit Swarm_ + _Phantasmal Web_ haunt effect.
        
- Langston dies in the dream realm mid-haunt, his corpse greying instantly.
    

#### Clues Obtained:

- Frell recently bartered with Greeley’s crew.
    
- Spoke of a “book of dreams” and a “silver key.”
    
- Named dropped items: butterfly brooch, silverware, blue parakeet—traceable.
    

---

### 🌒 Act IV: “The Well of Echoes”

#### Location: **Night Market Fountain (CR 8)**

- PCs can stake out the well.
    
- May catch a cult deacon placing shiver doses in a hidden crevice.
    
- Witness Greeley’s gang member collecting the drop and vanishing into a stairwell under the **Red Oliphaunt**.
    
- Can overhear or discover the cult’s hand gesture: spider-sign with crossed wrists.
    

---

### 🌊 Act V: “Breakwater Ambush”

- As the PCs close in, the **Brotherhood strikes**.
    
- Battle at the old pier: drug-addled guards, summoned water elemental, and **Guttermaw**, a hydrodaemon.
    
- Fleeing mob and collapsing planks create environmental hazards.
    

#### Fallout:

- PCs are officially sanctioned by Drune.
    
- Gain legal authority to arrest **Moses Greeley**.
    

---

### 🕯️ Act VI: “Den of Lies”

#### Location: **Greeley’s Den (CR 8+)**

- High above the Night Market, beneath the Red Oliphaunt.
    
- Evidence of Frell’s stolen goods and cult paraphernalia.
    
- Greeley may be desperate or defiant, possibly high himself.
    
- PCs can secure:
    
    - Clavis Somnus
        
    - Proof of drug link
        
    - Cult dealer confirmation
        

---

### 🧩 Threads Leading Forward

1. **Dreamscape Bleed**: PCs learn of the Paginarum’s influence spreading through Ilayas.
    
2. **Carrington’s Warnings**: She may appear in visions or be sought out by name.
    
3. **Sally Scrabblebones’s Signature**: Corpses bearing odd bite marks hint at her dream-hunting.






## Notes

### Dreamstone

- **Type**: Major Artifact
    
- **Aura**: Strong transmutation
    
- **CL**: 20th
    
- **Weight**: 3 lbs.
    

---

 🔮 **Origin and History**

- The Dreamstone is a fragment of a **meteorite** that fell through the **Dimension of Dreams** during Earthfall and ended up on Wynsend Forest.
    
- It was **recovered by Desna's clergy**, who passed it down secretly for generations, recording its history in the **Paginarum Lethargica**.
    
- Though sealed away in a **lead coffer** beneath a shrine in Ilayas, it was eventually unearthed by **Nahum Caligaro**, **Myra Lombroso**, and **Stainton Drune**.
    
- The cult of **Mog-Lathar** attempted to harness the stone, but **Myra betrayed Nahum**, triggering a failed ritual that **sucked Nahum, his cultists, and the dreamstone into the Dimension of Dreams**, creating the nightmare-ridden dreamscape that now infects Ilayas​.
#### **Effect and Powers**

The Dreamstone’s primary power is to **stabilize and expand a dreamscape**. Its major effects include:

- **Overlays the Material and Ethereal Planes** with a _shared_ dreamscape.
    
- **Normal dreamers** appear randomly in the dreamscape.
    
- **Lucid dreamers** (e.g., shiver users) have limited control but risk **real death** if killed within the dream.
    
- Every death within the dreamscape **expands the stone’s radius** by 1 foot per HD of the dreamer.
    
- Radiates a **“Vision of Hell”** (DC 20 Will) illusion of fiery cataclysm out to 50 feet​.
    
- Dreamers increasingly suffer **nightmare effects** each night (nightmare spell, DC starts at 15).
    
- Spell and item use by lucid dreamers **consumes resources in the real world**.
    
- Once a certain radius threshold is crossed, it is believed the stone can **overcome water boundaries**, threatening entire cities​.
    

---

#### 🗝️ **Destruction and Ritual**

The Dreamstone **cannot be destroyed conventionally**. Its destruction requires:

1. Performing the **“Breach the Veil of Dreams”** occult ritual.
    
2. Doing so **within the dreamscape** (not just near the stone in the real world).
    
3. Using the **Clavis Somnus** as the ritual’s key/focus.
    
4. Dropping the dreamstone into the portal created by the ritual and **shutting it**, which dissolves it into the Dimension of Dreams forever​.

### Clavis Somnus

- **Type**: Wondrous Item
    
- **Rarity**: Unique Artifact (non-consumable)
    
- **Aura**: Moderate **transmutation** and **divination**
    
- **CL**: 10th
    
- **Weight**: —

	Owner: [[Myra Lombroso]]
---

#### 🧭 **Appearance & Feel**

> A large, **ornate key made of mithral and silver**, cold to the touch and trailing a vapor of condensation. The shape is stylized with crescent and star motifs, echoing **Desnan** iconography.

---

#### 💡 **Primary Functions**

1. **Ritual Focus**
    
    - Satisfies the focus component of the **Breach the Veil of Dreams** occult ritual (from _Occult Adventures_).
        
    - **Grants a +5 competence bonus** to the primary caster’s skill checks during that ritual.
        
2. **Dream-Realm Buffs**
    
    - **+4 bonus on saving throws against illusion** effects.
        
    - **+4 bonus on Charisma checks** made _within the Dimension of Dreams_—useful for negotiating, manipulating dream terrain, or influencing intelligent entities.
        
3. **Waking Drawback**
    
    - **–2 penalty on saving throws against sleep effects**.
        
    - The bearer is considered to have **2 fewer Hit Dice** for determining sleep effect thresholds, and is always considered first when resolving which creatures are affected.
        

---

#### 🧠 **Psychometric Legacy**

Using spells like _object reading_ or the _psychometry_ skill unlock, PCs can learn a sequence of **visions** from the Clavis Somnus' history:

- **Vision 1**: Myra Lombroso receiving the key from Greeley in the Drowned Presbytery as part of a betrayal against Nahum.
    
- **Vision 2**: Frell Tann stealing the key and _Paginarum Lethargica_ from the ruined ritual site (area G3).
    
- **Vision 3**: Nahum’s failed ritual, his plunge into the dreamscape, and the dreamstone's awakening as the key clatters away. These glimpses help connect the cult’s schism, Nahum’s exile, and the artifact’s true nature​.
    

> _As you place your hand upon the Clavis Somnus, cold flashes through your fingertips—like plunging your hand into a forgotten grave. Your vision narrows, sound folds in on itself, and then the world cracks open like glass under pressure. Fractures of memory spill across your senses..._

---

**⚷ Vision I — The Betrayal in the Deep**

> You are underwater without drowning, weightless among barnacle-covered glass and sunken pews. The **Drowned Presbytery**.
> 
> **Myra Lombroso** stands amid rusting relics and sea-damp stone, eyes cold as the deep. In her hand: a vellum-wrapped book.
> 
> Across from her, **Moses Greeley**, hunched and anxious, wipes his hands on his robes before presenting something:
> 
> The **Clavis Somnus**—a silver and mithral key, glowing with pale condensation.
> 
> “This ends it,” he mutters. “He’s gone, and it’s yours now.”
> 
> Myra takes the key. No hesitation. Behind her, shadows shift. The **idol of Mog-Lathar** broods in the gloom. A pact is sealed—_not with words, but with silence_.

---

**⚷ Vision II — The Theft in Ash and Ember**

> A surge of heat. A choking cough.
> 
> You see the **ruined ritual chamber**, arcane chalk sigils still scorched into the floor. Candles sputter in broken glass.
> 
> **Frell Tann** stumbles over a smoldering bookstand, casting furtive glances behind him. His face is pinched with desperation and greed.
> 
> He scoops up the Clavis Somnus—_still faintly warm_—and a heavy, burned tome bound in darkwood slats: the **Paginarum Lethargica**.
> 
> “We need to go!” a voice whispers from the hall. Frell bolts, the artifacts pressed tightly to his chest.
> 
> The vision blurs with smoke and ember, like ink in water.

---

**⚷ Vision III — The Moment Everything Broke**

> Now: a chamber **alive with power**.
> 
> **Nahum Caligaro** chants in ecstasy or madness—you cannot tell. Dozens of cultists encircle him, shadows warping behind their robes. The **dreamstone** hovers above the floor, pulsing like a second heart, bleeding green and gold flame.
> 
> And then—**something goes wrong**.
> 
> The chanting falters.  
> A portal yawns open, a mouth of unmaking.  
> Nahum screams—not in fear, but in rage—as it pulls him and his followers inward, distorting them like wax figures in a furnace.
> 
> The **Clavis Somnus** slips from his hand, spinning once in the air… then **clattering to the stone floor**, alone.
> 
> The last thing you see is the dreamstone flaring—_a final, impossible light that devours the scene whole._

---

> 💫 _You lurch back to reality, gasping as if you’ve been held underwater. The Clavis Somnus is cool and inert in your palm once more. But the echoes remain—betrayal, theft, collapse. The key has been witness to it all._
---

#### 🔓 **Narrative Importance**

- The Clavis Somnus is the _literal_ and _metaphorical_ key to the mystery. It's the final piece needed to:
    
    - Enter the **Dimension of Dreams** intentionally.
        
    - Destroy the **Dreamstone**.
        
    - Unravel the fate of Nahum Caligaro and his excommunicated dream cultists.
        
- **Player Decision Catalyst**: Myra Lombroso often **offers this key in a desperate bargain**, signaling a shift from cult confrontation to occult investigation.

### Paginarum Lethargica

> “A battered tome, bound in darkwood slats, filled with centuries of vellum scraps and mismatched parchments scrawled in dozens of hands and languages. It is the secret journal of those who dared study the dreamstone—and the grave warning they left behind.”

- **Type**: Unique Artifact (not inherently magical, but contains powerful rituals)
    
- **Appearance**: A collection of **ragged, ancient pages**, bound roughly between **two hinged slabs of darkwood**.
    
- **Location History**: Passed in secret by Desna’s clergy for **over a thousand years** before being uncovered by **Nahum Caligaro** in his family library​.

The **Paginarum Lethargica** is a **record of the dreamstone’s entire known history**, including:

- The stone’s **fall through the Dimension of Dreams** during Earthfall.
    
- Its **collection by Desna’s emissaries** and subsequent attempts to study and contain its influence.
    
- Warnings that **nightmares always crept into any reality created by the dreamstone**, no matter how well-meaning the dreamer.
    
- Final records from the **Caligaro family**, chronicling:
    
    - Nahum and Myra’s expedition to the Wynsend Forest
        
    - The discovery of **Mog-Lathar** and the formation of the cult
        
    - The dreamstone’s awakening and Nahum’s fateful ritual.
        

---

#### 🧠 **Knowledge Utility**

Reading the Paginarum Lethargica:

- Grants a **+5 bonus on Knowledge (planes)** checks related to the Dimension of Dreams or Ethereal Plane (after 1 hour of study).
    
- Reveals the **ritual to destroy the dreamstone**, detailed below.
    

---

#### 🕯️ **The Ritual: _Breach the Veil of Dreams_**

The **most important entry** in the Paginarum Lethargica is the complete **occult ritual**:

> **Breach the Veil of Dreams** (_Occult Adventures_, pg. 209)  
> Allows the PCs to **enter the dreamscape physically** and **confront Nahum and the dreamstone** on their own terms.

The version in the Paginarum Lethargica includes _fail-safes_:

- If the **dreamstone grows out of control**, the ritual allows it to be **sealed back into the dreamscape**.
    
- Performing the ritual _inside the dream realm_, with the **Clavis Somnus**, and placing the stone in the portal it creates will **destroy the artifact forever**​.
    

---

#### 🧠 **Psychometry (Object Reading) Visions**

The book holds **psychic impressions** visible via _object reading_ or _psychometry_, revealing:

1. **Myra** receiving the Clavis Somnus from Greeley.
    
2. **Frell Tann** stealing the book and key from the failed ritual chamber.
    
3. **Nahum** in the middle of the ritual, being dragged into the dream realm as the dreamstone awakens in burning light​.

> As your fingertips brush the ancient vellum, your sight vanishes into darkness. A jolt of vertigo grips your mind, and then—**the visions begin.**

---

**⚷ Vision 1 — The Apology and the Betrayal**

> You see a **dusty, domed chamber**, its stone walls damp with seeping seawater. A **tattered tapestry of a spider** sways faintly in the stagnant air.
> 
> **Myra Lombroso** stands tall in her mourning robes, her expression unreadable. Across from her, **Moses Greeley**, pale and twitching, holds out a silver-mithral key wreathed in vapor—**the Clavis Somnus**.
> 
> “For what it’s worth,” he says with a sneer, “I’m sorry.”
> 
> He hands her the key. Myra takes it slowly. Behind her, **the idol of Mog-Lathar looms**, watching in silent judgment.

---

**⚷ Vision 2 — The Theft**

> The image shifts violently. **Soot-choked light** bleeds through shattered beams in a ruined ritual chamber.
> 
> A young man—**Frell Tann**—kneels amid the wreckage, sweat beading on his brow. With trembling hands, he seizes the Clavis Somnus and a thick, smoke-blackened tome.
> 
> “Hurry up,” someone whispers off-screen.
> 
> Frell stashes the items under his cloak and bolts. The chalk circle beneath him still smolders with dormant power, and behind him, **a shadowy sigil pulses faintly in red.**

---

**⚷ Vision 3 — The Cataclysm**

> The air becomes _heavy_. Time unravels. You are now inside the ritual chamber _before_ its collapse.
> 
> **Nahum Caligaro**, draped in cult vestments, stands at the center of a grand sigil surrounded by hooded figures.
> 
> On a stone plinth before him hovers the **dreamstone**, blazing with a swirling internal fire—**too bright, too wrong**.
> 
> Suddenly, the energy spikes. The chanting falters. One acolyte screams.
> 
> **Nahum's body warps**, shadows pulling at his limbs. A **portal of infinite depth** yawns open behind him. He reaches for the Clavis Somnus—just beyond his grasp.
> 
> The dreamstone pulses again—**a blinding burst of viridescent fire**—and the scene is swallowed in an avalanche of light and falling stars.

	Take Damage!!!
---

> You return to yourself breathless, sweat slicking your brow. The book lies in your lap, silent once more—but the echo of screams and the heat of that unnatural fire still dance at the edge of your senses.