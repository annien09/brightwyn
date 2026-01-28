---
tags:
  - "#Letter"
holder: "[[Bertie Biglestaff]]"
recipient:
  - "[[Bertie Biglestaff]]"
status: ✅
organization:
  - "[[The Scorching Sun]]"
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

### ✦ Extract – Encrypted Ledger Snippet (Translated by Fleur Dubois)

|Date|Benefactor|Routing Alias|Transfer (gp)|Recipient|Allocation Purpose|
|---|---|---|---|---|---|
|26th Gozran |_Emerald 6_|L.P. (W7 - Dock Pass)|3,000|**The Elysian Gallery**|“Framing materials, expedited delivery”|
|29th Gozran|_Mirrorhand_|S.T. (via Nightcoach)|4,250|**Seraphina Veridane – Gala Fund**|“Invitation printing & talent fees”|
|3rd Desnus|_Ash Lantern_|V.F. (vault proxy)|2,500|**Gala Committee – Illumination Rites**|“Stagecraft, civic shielding”|
|8th Desnus|_Client S._|G.F. (via house courier)|6,000|**Cedric Veridane – Economic Symposium**|“Revitalisation exhibit sponsorship”|

---

**Notations (Encrypted Margin Markings – Deciphered by Fleur):**

> ✶ “Ensure E6 entries are scrubbed in outer archives. Route all further notes through Sapphire Coil.”  
> ✶ “Ash Lantern authorized by G.K.?”  
> ✶ “Mirrorhand tipped Nightshade - handle.”  
> ✶ “Client S. scheduled for attestation ceremony. Prepare Elysian floor for red sigil work.”

---

###  **Fleur’s Private Translation Notes (in margin of her copy):**

- **Emerald 6**: Likely one of the Jade Gate’s internal financing codes. Has appeared before.
    
- **Mirrorhand**: Alias used by a known noble’s majordomo connected to Veridane’s art acquisitions.
    
- **Ash Lantern**: This code is new, but associated with _ritual funding_?
    
- **Client S.** = Seraphina? Or _Seraphim_, the title used in certain cult records? Could mean both.
    
- **G.F.** = Galavell Footman - likely under duress or paid to courier.
    
- **Nightshade tip line** implies Elandra knows, or is being tested. Possibly being watched herself.


10 days prior to current day, when cross-referencing the donation records, particularly the line marked "Client S.", with obscure cult references, Fleur has found something and had come running to Bertie, in distress. 


Fleur slips into Bertie’s study without knocking. She appears to be in slight distress. There’s a slim folio tucked under her arm and a familiar look in her eye: that mix of curiosity and unease that usually means she’s found something she shouldn’t have

Fleur: I’ve been reviewing the old records again - ledger fragments, donation routing, that sort of thing. You remember that ‘Client S.’ transfer we flagged a while back?”

>(She sets the folio on the desk, flipping it open to reveal handwritten annotations and transcribed phrases from various documents.)

Fleur: Something about it didn’t add up. So I started digging in old library archives, fringe cult records, anything that might match the language. And, well… I think I found the source.

> (She taps one of the transcribed phrases with a gloved finger.)

Fleur: The Scorching Sun cultists, obscure, but not entirely unknown. They believe in devotion through death. Willing sacrifice, ritual immolation. Volunteers who step into flame, claiming "clarity comes only when the self is burned away". And when they succeed in dying that way, willingly, with inten, their souls don’t pass on peacefully. They become something else. A kind of daemon called a Ceustodaemon. They have been used as guardians of vaults, tombs, sealed doors

Some of these donation lines could lead to places that might need guarding, but… if that's the case and demons are involved, this isn’t about coin anymore. I’m not saying we burn down the Elysian Gallery. But I do think we should stop treating this as just a scandal. There’s more than gold behind these donations, and I don't think we'll like the truth."