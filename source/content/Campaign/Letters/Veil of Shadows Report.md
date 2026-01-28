---
tags:
  - "#Letter"
quest:
  - "[[Investigating the Jade Gate]]"
recipient:
  - "[[Aelwynn Ianven]]"
sender:
  - "[[Elandra Nightshade]]"
sentto:
  - "[[The Cleric's Wineskin]]"
sentfrom:
  - "[[The Red Door]]"
sentdate: 29 Desnus 4713 AR
holder: "[[Aelwynn Ianven]]"
status: ✅
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
Letter contents that has been sent to  `VIEW[{recipient}][link]` <span style="font-size: small">

- **From:** `VIEW[{sender}][link]` <span style="font-size: small">**Location:** `VIEW[{sentfrom}][link]` </span> 

## Report

**Veil of Shadows Report**

_Commissioned Inquiry on The Jade Gate and The Gatekeeper_

---

**Subject of enquiry:** Gatekeeper of The Jade Gate

**Classification:** Top Secret

**Overview:** The entity known as the Gatekeeper holds a reputation as one of the most enigmatic and feared figures within the criminal world. Known for ruthlessness, intelligence, and mastery over the art of concealment, they command The Jade Gate in Ilayas, a syndicate with global reach and a chilling efficiency in the smuggling of artifacts, forbidden magical objects, and other contraband.

**Current Intelligence and Recent Rumors:**

1. **Association with House Veridane**  
    Persistent rumors suggest that Lord Cedric and Lady Seraphina Veridane, nobles of considerable influence in Ilayas, may have dealings with The Jade Gate. It is believed that their wealth and social standing mask a lucrative black-market enterprise, trafficking in rare artifacts and magical contraband. This theory is supported by an increase in rare and illicit goods passing quietly through Ilayas’ ports, a market well within the influence of House Veridane.
    
2. **The Angel Day Ball**  
    This year's Angel Day ball, hosted by the Veridanes, is said to be especially exclusive, and sources within high society whisper that a guest of singular importance may be attending. The Gatekeeper, rarely seen and even less often recognized, is rumored to be among those invited. Though no clear description exists, it is speculated that they may present as a figure of unremarkable appearance, perhaps even concealed under a mask or disguise.
    
3. **Identity and Presence**  
    The Gatekeeper’s gender, face, and true name are unknown; however, there are faint hints from recent activities that suggest the figure may possess a voice with a distinctly male tone, though this could be a deliberate misdirection. Reliable sources indicate they employ magical means to obscure their identity and are capable of assuming multiple guises. Caution is advised, as their mere presence is often concealed by potent illusion spells.
    
4. **Time-Sensitive Lead**  
    It is the belief of the Veil of Shadows that this Angel Day ball may be a rare opportunity. Should the Gatekeeper indeed be in attendance, their presence will likely be brief, with no guarantee of further appearances in Ilayas for some time. This occasion may be the last viable lead before their trail vanishes once again into obscurity.

