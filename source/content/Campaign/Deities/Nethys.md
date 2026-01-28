---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/Nethys.png
aliases:
  - The All-Seeing Eye
alignment: True Neutral
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

## God of Magic
Alignment: N

Domains: Destruction, knowledge, magic, protection, glyph

Favoured weapon: Quarterstaff

Ancient Osirian texts mention a powerful God-King named Nethys, whose mighty sorceries allowed him to see all that transpired, even across the planes of the Great Beyond. The knowledge he gained through these visions fuelled his divinity, but shattered his psyche as well. Ever since, Nethys has been of two minds—one set upon destroying the world and another pledged to protect it.

The church of Nethys tries to balance the god’s two aspects, but individual temples might lean one way or the other. His followers are those who desire magical knowledge or power, arcane or divine, regardless of how they want to use it—whether to destroy, invent, or protect. Nethys is often shown with both his aspects in action. One side of him is burned and broken, unleashing terrible magic upon the world, while the other half is calm and serene, using magic to heal the sick and protect the innocent.

Formal ceremonies in the church require an elaborate robe, skullcap, mozzetta, and hood, all in similar colours (such as red, maroon, and burgundy), the colour range chosen depending on the temple. Depending on its focus, a particular temple might look like a fortress, sanctuary, wizard’s tower, or even a small palace, but all are staffed by knowledgeable people unfazed by loud noises and strange appearances. His bible is The Book of Magic, a comprehensive tome that discusses guidelines for channelling magic and the moral ramifications of its use and misuse (often taking alternative positions in the space of a few paragraphs); its words are always written on the temple’s interior walls, but most priests also carry it as a book or scroll bundle.

It is said that the manifestation of zones of unpredictable magic are the results of Nethys passing close to the Material Plane, while the manifestation of zones of “empty magic” (areas where magic simply doesn’t function) are indications of his anger at a region. Nethys is not known for showing favour or wrath to his followers or enemies, a fact in which many of his worshipers take pride. They are quick to point out to other faiths that their god does not patronize or coddle them with frustrating dreams or bizarre omens—traits that generally do not endear the faithful to members of other churches.

## Notes

