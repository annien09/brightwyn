---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/PlaceholderImage.png
alignment: Chaotic Good
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
>> **Pronouns** | `INPUT[Pronouns][:pronouns]` |
>> **Alignment** | `INPUT[Alignment][:alignment]` |
>
>> [!metadata|metadataoption]- Deity Info
>> #### Deity Info
>>  |
>>---|---|
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Power** | `INPUT[DeityPower][:deitypower]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
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

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ![[PlaceholderAudio.webm]]
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |


# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|organizations]- Related Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE econtains(worship, this.file.link) AND contains(tags, "Organization")
> SORT organizationtype ASC, file.name ASC

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

## Desna, Song of the Spheres – Goddess of dreams, luck, stars, and travellers

Alignment: CG

Domains: Dreams, luck, moon, travel, stars, void

Favoured weapon: Starknife

While the other gods created the world, legend holds that Desna was busy placing stars in the heavens above, content to allow the other deities to create a world full of wonders for her and her faithful to explore. Since that day, all those who look up to the stars find themselves wandering in the endless mysteries of the sky. Trailblazers, scouts, adventurers, and sailors praise her name, as do caravaneers and those who travel for business, and her luck makes her a favourite of gamblers and thieves. Desna often appears as an elven woman, clad in billowing gowns with brightly coloured butterfly wings on her back. Delicate clouds of butterflies frequently accompany her image.

Wanderers at heart, the faithful of Desna travel the world in search of new experiences, while always trying to live life to its fullest. Their temples are light, open affairs, with a significant number of astrological charts to help track the stars and mark important celestial events. Formal attire for most of the priesthood is a flowing white robe with black trim and a matching silken cap, although ranking members of the church add more decorative elements. Her temples also double as celestial observatories or at least have one room partially open to the sky, and in rural areas they often have services for travellers. Her holy text is called The Eight Scrolls.

Desna is one of Brightwyn’s oldest deities, and she has changed little since the dawn of civilization. She often shows her favour through the manifestation of butterflies, particularly bright blue swallowtails. Her priests often make it a point to master the use of her favoured weapon, a throwing blade known as a starknife—the weapon has become quite popular among others as well. She keeps several palaces throughout the Great Beyond, including one called Cynosure, visible in the northern night sky as the star around which all other stars dance.


## Dreams

### **Who is Desna in Relation to Dreams?**

- Desna is **the Tender of Dreams**, the **Song of the Spheres**, and the **Wanderer Among Stars**.
    
- Dreams are not just rest—they are a **sacred domain**, a reflection of hope, fate, fear, and possibility.
    
- She doesn't control dreams in a tyrannical sense—she **tends** them. Like a gardener. Or a dream-sailor.
    
- Her presence ensures that the Dimension of Dreams remains a place of **beauty**, **growth**, and **self-discovery**, rather than one consumed by **nightmares**, **fatalism**, or the **Nightmare Lords**.
    

> 🦋 _"Dreams are where the soul remembers what it’s capable of. My lady just hands you the map."_ — A Kenay Sister

---

## 🛌 **The Types of Dreaming (Mechanics + Lore)**

### 1. **Normal Dreaming (Monadic Soul Projection)**

- All mortals project their **monadic soul** into the **Dimension of Dreams** while sleeping.
    
- This is called the **lucid body**—a psychic reflection of self shaped by the dreamer’s subconscious.
    
- The dreamscape formed is an **ephemeral demiplane**—a personal bubble that fades upon waking.
    
- **Not physically real.**
    
    - Spells cast aren’t used up.
        
    - Wounds don’t last.
        
    - Death simply wakes you up.
        

> Desna _allows_ this by divine law—it is natural, safe, and meant to **refresh the soul**.

---

### 2. **Lucid Dreaming**

- With the **Lucid Dreamer** feat or certain drugs (e.g., _shiver_), a dreamer gains **control** over their dream.
    
- You may:
    
    - Alter the dream.
        
    - Attempt to perform **“impossible feats”** with Charisma checks (conjuring items, flying, etc.).
        
    - Interact more meaningfully with recurring dreamscapes or others' dreams.
	    
	- A lucid dreamer’s spell slots and magic item charges used on the dream realm are similarly consumed in the waking world. Most importantly, lucid dreamers in certain nightmarish dreamscapes that are killed while dreaming also die in the real world.
        

> This is the path of **prophets, psychics, and Desnan seers**—those who awaken within the dream and shape it with purpose.

---

### 3. **Dreamwalking (Physical Entry into the Dream)**

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
    

---

## ✨ Desna's Role in Dreamwalking

Desna acts in dreams **symbolically**. She rarely appears in person but often manifests:

- As a **white moth or swallowtail butterfly**.
    
- Through **songs** or dream-music.
    
- As a mysterious woman giving cryptic aid.
    
- Through **serendipity**—an item placed just where needed, a vision seen at just the right time.
    

Her dream interventions **offer choice**, not mandates. She _never binds fate_.

> “Even dark dreams are stars in reverse. And stars are always watching.”

---

## 🕯 What Desna's Faith Teaches About Dreams

### ▪ Dreams Are Sacred

- Every dream is a **map of the self**. Even nightmares reveal hidden truths.
    
- Followers of Desna **record** their dreams and treat them as **divine texts**.
    

### ▪ Nightmares Must Be Fought

- Desnans actively **oppose night hags**, **Nightmare Lords**, and entities like **Mog-Lathar**.
    
- They consider it holy work to protect dreamers from these intrusions.
    

### ▪ Prophecy Must Leave Room for Hope

- Desna sends **dream-warnings** only when absolutely necessary.
    
- She always includes a **sign of hope**—a protective spell, a star, a vision of an alternate path