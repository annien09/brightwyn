---
tags:
  - "#Letter"
quicknote: Job Board of Illayas
holder: "[[Nezoh Regis]]"
sender:
  - "[[Isiril Adren]]"
sentfrom:
  - "[[The Lunar Radiance Inn]]"
sentto:
  - "[[Ilayas]]"
status: ✅
quest:
  - "[[Magical Research during Celestial Night]]"
recipient:
  - "[[Nezoh Regis]]"
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
**Description:** Embark on a magical quest to procure samples of the elusive Moonwort and mystical Angel's Trumpet! These rare plants are crucial for research on the upcoming celestial event and require skilled adventurers to gather them in their entirety.

**Task at Hand:** Retrieve samples of Moonwort and Angel's Trumpet, including their roots for replanting and freshly picked flowers. The bounty of these magical herbs is needed to prepare for the Celestial Night astrology event.

**Deadline for Completion:** The quest must be completed by the 28th of Desnus. Time is of the essence, and the timely return of these mystical botanical samples is crucial.

**Quantity Needed:**

- Moonwort: 8 complete sets (roots and flowers)
- Angel's Trumpet: 5 complete sets (roots and flowers)

**Reward:** Generous compensation of 75gp for Moonwort samples and an additional 75gp for Angel's Trumpet samples awaits the successful adventurers who procure the plants.


**Further Contact:** Interested adventurers can inquire at [[The Lunar Radiance Inn]].