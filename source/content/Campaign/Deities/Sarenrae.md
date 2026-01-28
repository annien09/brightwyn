---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Sarenrae.png
aliases:
  - The Dawnflower
alignment: Neutral Good
NPC:
  - "[[Siramin Adren]]"
deitypower: Greater God
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
>> **Followers** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):NPC]` |
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
> **Followers** | `VIEW[{NPC}][link]` |
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

## Goddess of healing, honesty, redemption, and the sun
Alignment: NG

Domains: Fire, healing, sun, truth

Favoured weapon: Scimitar

When the primal forces created Brightwyn, Asmodeus planted a malignant evil upon the world under cover of perpetual darkness. The doctrine of Sarenrae’s faith tells that the Dawnflower brought light to the world, and with it came truth and honesty. Those who had turned to evil saw their wickedness and were forgiven by the light of Sarenrae.

The clergy of Sarenrae are peaceful most of the time, administering to their flock with a gentle hand and wise words. Such kindness vanishes, however, when the church is stirred to action against an evil that cannot be redeemed—particularly against the cult of Rovagug. At such times, Sarenrae’s clerics become dervishes, dancing among foes while allowing their scimitars to give their opponents final redemption. Thus, her faith attracts those with kind hearts, but willing to harden them when kindness is a dangerous weakness.

Religious art depicts the sun goddess as a strong woman with bronze skin and a mane of dancing flame. While one hand holds the light of the sun, the other grasps a scimitar, so that she might smite those who do not change their ways.

Formal raiment includes a long white chasuble and tunic decorated with red and gold thread depicting images of the sun, and officiating priests usually wear a golden crown with a red-gold sunburst device on top. Scimitars inlaid with gold sunbursts or golden gems are common ceremonial implements. Temples are open-air buildings open to the sky, sometimes with large brass or gold mirrors on high points to reflect more light toward the altar (satellite buildings, however, have ceilings).

Sarenrae’s holy book is The Birth of Light and Truth. Most copies contain extra pages for the owner to record uplifting stories he experiences or hears in order to repeat them to others. Swordplay, particularly with the scimitar, is held to be a form of art by her followers. Sarenrae indicates her favour with sightings of doves, or through the shapes of ankhs appearing in unexpected places. Her displeasure is most often made apparent through unexplained sunburns or periods of blindness that can last anywhere from only a few moments for minor transgressions to a lifetime for mortal sins.

## Notes

