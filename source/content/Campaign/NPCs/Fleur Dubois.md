---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/People/Fleur 2.png
ideals: |-
  Freedom: She believes in defining her own path, even if she must play the role expected of her in the meantime.

  Truth has value: Secrets are currency, and Fleur is one of the richest young women in Ilayas—none know it yet.

  Beauty is a weapon: A glance, a word, a perfectly timed laugh—these are just as sharp as daggers.
flaws: |-
  Distrust of anyone outside her and Bertie.

  Has grown so used to manipulation that she struggles to recognize genuine affection.

  Harbours resentment so deeply it’s begun to poison her compassion.
fears: |-
  Being married off to a noble stranger, stripped of autonomy and trapped forever.

  Bertie being hurt or exiled by the family or nobility due to his defiance.

  Losing the game of secrets and being exposed or blackmailed herself.
mannerisms: |
  Speaks in measured tones but often peppers her words with double meanings.

  Twirls her wine glass when in thought.

  When uncomfortable or emotionally affected, subtly touches the brooch hidden inside her corset (a gift from Bertie).

  Maintains eye contact as a show of dominance, especially with nobles.
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
> ![[PlaceholderAudio.webm]]
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
> 

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

## Goals

- Secretly amass enough wealth and influence to escape the Dubois family and establish herself as an independent broker of information.
    
- Protect Bertie from the manipulations of their family and the scrutiny of the nobility.
    
- Discover leverage powerful enough to dismantle the family's grip on her future.
    
- One day, host her own salon—a center of secrets, arts, and influence far from the shadow of her lineage.

## **Fleur Dubois — Official Persona**

**Title/Role:** _“Cultural Liaison & Patron of the Arts”_

**Public Image:**  
Fleur Dubois is widely regarded in Ilayas’ upper social circles as a patroness of refinement, known for supporting local artists, sponsoring salons, and advocating for cultural preservation. She presents herself as someone who **“connects noble causes with noble coin,”** often seen attending gallery unveilings, historic preservation campaigns, and charity auctions tied to the arts or education.

She's praised for her eloquence, grace, and tireless attendance at every major gala, making her a natural intermediary between high society and civic causes People trust her with sensitive social introductions and discreet messages, which she handles with all the poise expected of a proper lady, never raising suspicion.

**Why it works:**

- It lets her be everywhere important people are without question.
    
- Artists, writers, and gallery owners are perfect sources of gossip and whispers.
    
- “Preserving cultural heritage” gives her a legitimate reason to ask about old bloodlines, noble claims, rare items, or buried secrets.
    
- It's a role her parents approve of, especially as they believe it's helping raise her social profile and “displaying her for the right suitor.”
## Acquaintances



## Current Events

Fleur continues to attend galas, but every event is a mission. She seeks out nobles with debts, scholars with forbidden curiosities, and diplomats looking for leverage. Every whispered confession or flirtatious tease adds to her growing archive of usable secrets.

Recently, a new player has emerged in Ilayas’ political landscape: someone seeking to move power from the council to the shadowed syndicates. Fleur has begun gathering intelligence on this “Silent Accord,” and is feeding scraps of information to Bertie to investigate through magical means. Together, they walk a knife’s edge.

## History
Fleur was groomed for nobility—flawless etiquette, impeccable fashion, and enough political sense to survive a court. But behind the masks and compliments, she grew to loathe what she represented. She found a sense of self not in being _seen_, but in _seeing_. She watched as her siblings clawed and crumbled beneath the family’s expectations and quietly swore she’d escape before that fate found her.

Though her parents still believe she’s a willing pawn, she’s already woven a secret life of espionage and subtle sabotage. Her bond with Bertie is the one tether she clings to without strategy—he is the only one who sees her cage and does not judge her for not yet breaking it.

## The Silent Accord

**1. Unusual Council Behavior & Whispers of a Political Shift**  
Fleur has noticed the shift in tone among certain council members and high-ranking nobles, especially Cedric Veridane. She's overheard repeated rumours and allusions to "economic realignment". She has found that Cedric Veridane has been pushing new reforms and gathering (more like buying/extorting) the support of other nobles. She suspects this is more than just economic posturing.

These reforms refer to shifting trade authority and wealth control from the council’s traditional regulatory arms (like independent guilds, city watch customs officers, and temple-managed ledgers) into the hands of private security firms, noble-owned companies, or even foreign-backed cartels.

Sources of information:
> _“Ilayas must modernise. Our independence should not be shackled by traditionalist fearmongers. These reforms offer more than economic advantage. They ensure Ilayas is no longer a city that reacts, but one that leads. If art is evolution of thought, this is our Renaissance. I once feared these changes would cheapen us. But I’ve come to see that resisting growth is its own form of stagnation.”_
Said by a councilor Elara Swiftbrook (Mistress of Culture and Arts) at a private salon, after three glasses of silver-aged plum wine. Fleur noted that a Veridane steward was present and was satisfied with her vocal support.

>_"We’ll deliver the city’s economic heartbeat into better hands. Ones that aren’t afraid to break tradition.”_ 
– Found in a burned letter fragment intercepted by one of Fleur’s informants. The handwriting resembles that of a junior clerk in the Council’s trade department.


>_“The days of fragmented regulation are over. Unified control, whether by council or contract, is the only way forward.”_
– Whispered during a walk in the High Garden by a merchant baron of House Cinthel who rarely attends public events. Fleur’s contact notes he’s recently had his debts cleared.

**2. Discreet Disappearances & Hesitations**  
Fleur knows that one of Lady Alinya’s allies on the council, Lord Alistair Greycastle (Minister of Health and Wellbeing) a council member known for vocal opposition to the reforms, has gone silent and was last seen at a discreet private meeting organised under the guise of a cultural event. (She doesn’t know what happened to him but suspects foul play.)

**3. The Jade Gate’s Influence Is Growing**  
While not explicitly confirmed, Fleur has **compiled enough whispers and patterns** to deduce that the Jade Gate might be involved in backing Veridane’s reforms. She's pieced together:

- A series of quiet trades and donations from shady benefactors to Veridane-aligned patrons.

See [[Extract - Encrypted Ledger Snippet]].

### How Fleur Discovered This

- **Private Conversations** at gala after-parties and balcony interludes. Fleur is a magnet for loose tongues, especially those enchanted by her charm.
    
- **A paid footman** from House Galavell, who passed her notes about odd deliveries and "frequent late-night meetings" involving Veridane’s estate.
    
- One of her contacts in the Veil of Shadows, whom she occasionally feeds rumors to in exchange for curated truths, gave her the tip that the Jade Gate might be involved.



## Notes

- **Alias:** "The Velvet Whisper" (used in her covert dealings)
    
- Fleur is beginning to suspect one of her family members is feeding information to an outside party—possibly Alexandre or Genevieve.
    
- She has recently been approached (indirectly) by a member of the Veil of Shadows who may know about her side dealings.
    
- Keeps a coded diary in Infernal—hidden beneath a false bottom in a jewelry box.



