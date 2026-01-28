---
tags:
  - "#Letter"
holder: "[[Aelwynn Ianven]]"
sender:
  - "[[Elandra Nightshade]]"
sentfrom:
  - "[[The Red Door]]"
recipient:
  - "[[Aelwynn Ianven]]"
sentto:
  - "[[The Cleric's Wineskin]]"
status: ✅
quest:
  - "[[Of Dreams and Spiders]]"
organization:
  - "[[Veil of Shadows]]"
---

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
>> **Aliases** | `INPUT[list:aliases]` |
>> **Quick Notes** |  `INPUT[textArea:quicknote]`
>> **Holder** | `INPUT[Null][suggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):holder]` |
>> **Letter Sender** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):sender]` |
>> **Sent From Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):sentfrom]` |
>> **Recipient Of Letter** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):recipient]` |
>> **Sent To Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):sentto]` |
>> **Cost** |  `INPUT[textArea:servicecost]`
>> **Sent Date** |  `INPUT[textArea:sentdate]` |
>> **Estimated Delivery Date** |  `INPUT[textArea:deliverydate]` |
>> **Previous Letter** | `INPUT[inlineListSuggester(optionQuery(#Letter AND !"z_Templates"), useLinks(partial)):previous]` |
>> **Next Letter** | `INPUT[inlineListSuggester(optionQuery(#Letter AND !"z_Templates"), useLinks(partial)):next]` |
>> **Letter Status** | `INPUT[Status][:status]` |
>> **Quest** | `INPUT[inlineListSuggester(optionQuery(#Quest AND !"z_Templates"), useLinks(partial)):quest]` |
>> **Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |


> [!infobox]
> #### Letter Info
>  |
> ---|---|
> **Sent Date** | `VIEW[{sentdate}]` |
> **Estimated Delivery** | `VIEW[{deliverydate}]` |
> **Status** | `VIEW[{status}]` |
> **Owner** | `VIEW[{holder}][link]` |
> **Previous Letter** | `VIEW[{previous}][link]` |
> **Next Letter** | `VIEW[{next}][link]` |

# **To:** `VIEW[{recipient}][link]`  <span style="font-size: medium">**Location:** `VIEW[{sentto}][link]`</span> 
Letter contents that has been sent to `VIEW[{recipient}][link]` <span style="font-size: small">

- **From:** `VIEW[{sender}][link]` <span style="font-size: small">**Location:** `VIEW[{sentfrom}][link]` </span> 

## Notes

Veil of Shadows: Operative Brief – Subject Inquiry: Rogi, Mavik, Serena

Compiled by: Whisperleaf, Shadowcaller (Level IV Agent)  
Authorised by: The Mistress of Revels, Elandra Nightshade  
Location: Ilayas, District V - The Shingles  
Date: 30th Desnus

  

### PRIMARY DIRECTIVE

As per contract authorisation, a discrete investigation has been completed into the current status and known whereabouts of Rogi “The Rat”, Mavik “The Mace”, and Serena “The Phantom”, formerly implicated in the death of Archivin Walder. All subjects were last linked to known addict haunts within the Fever Dream Alley region of The Shingles. Rogi “The Rat” is currently under guard arrest and could not be interviewed.

Fever Dream Alley continues to deteriorate under reduced patrol presence, thriving instead under informal rule by various coinboys, lucid sleepers, and drug dealers. The presence of supernatural anomalies and unexplained deaths in the vicinity prompted heightened caution during surveillance.

  

### LOCATIONAL INTEL

- Fever Dream Alley remains the last credible known location for all three targets. The alley has become a makeshift flophouse for Shiver addicts, dominated by plank bridges and sagging ropeways above refuse-strewn corridors. The hovel with the rusted potbelly stove is still active, providing minimal shelter and warmth to a small knot of users.  
      
    
- Mavik remains unseen, though his name was mentioned in a back-alley code drop. A courier overheard a Night Market peddler say, “Tell the Mace the dream’s about to break.” Tone suggests warning or possibly signal for movement.  
      
    
- Serena may be operating under a false persona. Multiple witness statements describe a veiled woman with pale skin and silver eyes watching the alley from rooftops, always disappearing before approach. Her behavior aligns with Serena’s known patterns of extreme withdrawal and rooftop migration.  
      
    
- A known associate of the subjects by the name of Frell Tann was spotted three nights ago crawling through a collapsed plank bridge near the alley’s upper western rise. He appeared gaunt, unwashed, and paranoid, clutching a cloth-wrapped parcel and muttering about “things with eyes that don’t close.” He has since vanished, presumed to be hiding in the upper ropes or in deep drug-induced stupor.
    

### OBSERVED PATTERNS

Investigation correlates strongly with a set of Shiver-related deaths. Attached are verified vignettes from our files:

- Alley Addicts: Six shiver users found hanged in Fever Dream Alley over the last two weeks. Official report: mass suicides driven by despair. Veil sources confirm each corpse was covered in tens of miniscule puncture wounds, unexplained by coroners. Local vagrants whisper “the spiders got ’em.” We interpret this as an urban euphemism for an unseen predator or spiritual phenomenon native to the area.  
      
    
- The Breakwater Three: Three female victims recovered from the lake’s edge in the Breakwater Pier, bodies broken and contorted. City Watch reported shiver-induced drowning. Veil analysis suggests the trauma aligns with drowning patterns, crush injuries and claw-like abrasions indicate impact or dropping from height.  
      
    
- The Hungry Dead: Three partially consumed corpses discovered near Bridgefront gutters. City Watch concluded self-inflicted gnawing under shiver withdrawal. Authorities claim that the sleepwalking addicts must have been so malnourished and intoxicated as to unknowingly gnaw themselves to death. One victim carried a branded token associated with Barvasi’s crew. Possible punishment, ritual, or predation.
    

### OPERATIONAL CONCERNS

- No divinations have yielded reliable insights on the deceased. This is consistent across all vignettes. Residual magical resistance or post-mortem interference is suspected.  
      
    
- The spread of shiver and its effects on lucid dreaming behavior are no longer confined to the users. Proximity to chronic users or exposed sites appears to cause emotional disturbance, sleepwalking, hallucinations, or paranoid fixations in uninvolved civilians.
    

