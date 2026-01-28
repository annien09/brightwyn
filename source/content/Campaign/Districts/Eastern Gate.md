---
tags:
  - "#Location"
  - "#District"
art: z_Assets/Locations/Eastern Gate.webp
pronounced: Eastern Gate
aliases:
  - Eastern Gate
districttype:
  - Commercial
location:
  - "[[Ilayas]]"
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
> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Type** | `INPUT[DistrictType][inlineListSuggester:districttype]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{districttype}][text]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!recite]+ Introduction
> 

> [!metadata|map]- Map
> ```leaflet
> id: TBD
> image: [[PlaceholderImage.png]]
> height: 600px
> width: 640px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 1
> zoomDelta: 0.5
> unit: meters
> scale: 1
> darkMode: false
> ```

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(location), ", ") AS "Location", join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "POI") AND  !contains(poitype, "Shop")
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|shops]- Shops
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(location), ", ") AS "Location", join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND (contains(tags, "POI") and contains(poitype, "Shop"))
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|organizations]- Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Organization")
> SORT tags DESC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview 
### Approaching the Gates

**Fields and Farmlands**: As travelers approach the city gates, they pass through fields and farmlands extending beyond the city walls. These lands are worked by local farmers, and the sight of golden wheat fields, flourishing orchards, and vibrant vegetable patches creates a picturesque scene. The air is filled with the earthy scent of fertile soil and the occasional waft of blooming flowers.

**Humble Homesteads**: Scattered beyond the city walls are the humble homes of the farmers and rural residents who contribute to the city's prosperity. These cottages, constructed from a mix of wood and stone, are surrounded by small gardens and tended fields. It's a glimpse into the simple and hardworking lives of those who sustain the city with their agricultural efforts.

### The Gates

The gate leading into Hearthstone Haven is flanked by sturdy guard posts, constructed from a mix of stone and reinforced timber. These posts stand tall on either side of the entrance, each featuring a watchtower with a pointed roof. Banners displaying the city's emblem flutter from the towers, adding a touch of color to the otherwise utilitarian structures. Magical sconces illuminate the area, ensuring that the gates are visible day and night.

Diligent city guards, clad in practical uniforms of Ilayas, stand watch at the gate posts. They are a diverse group, reflecting the varied population of the Common District. They wear enchanted insignias on their uniforms, indicating their affiliation with the city's security forces. Well-trained and experienced, the guards are adept at handling a range of situations, from routine inspections to ensuring the safety of the district.

As people approach the entrance, guards maintain a watchful eye while also engaging in polite interactions.

Regulars from the Common District, including farmers, artisans, and merchants, approach the gates with a familiarity born of daily routines. They exchange friendly greetings with the guards, often sharing news or engaging in lighthearted banter.

Merchants from neighboring regions approach with loaded carts and magical trinkets for trade. The guards, recognizing these familiar faces, often inquire about their latest wares and news from other parts of the realm.

### Guards Greeting

PCs are greeted by [[Sargent Elysia Stormblade]]. a well-built and tall guardswoman with deep black hair cascading down to her shoulders in loose waves:

- "Greetings, travelers, my name is Sargent Elysia Stormblade! What brings you to Ilayas today?"  
    
- "Are you here for business, pleasure, or perhaps seeking residence?"  
    
- "How was your passage to Ilayas? Any noteworthy sights or encounters along the way?"  
    
- "May I know your names, please? It helps us keep a friendly record of those entering. Do you have any identification or documentation we should be aware of during your stay?"  
    
- "Is this your first time in Ilayas, or have you visited our fair city before?"  
    
- "Our district is known for its markets and cultural celebrations. Is there anything specific you're looking forward to experiencing?"  
    
- "If you need any recommendations for inns or taverns, feel free to ask. We want your stay to be pleasant."  
    
- "For the safety of everyone, please be mindful of the city's rules.
    1. Show courtesy and respect to fellow residents, guards, and visitors. Avoid disruptive behavior and maintain a quiet atmosphere during nighttime hours.
    2. No Littering. Dispose of trash in designated bins to keep the streets and public areas clean.
    3. Report any suspicious activities or concerns to the city guards promptly.
    4. No Unauthorized Magic Use: Refrain from using powerful or potentially dangerous magic in public spaces. Seek permission from the authorities for any magical displays or performances.
    5. Bargain respectfully with merchants and vendors in the markets. Do not engage in theft or dishonest practices; respect the livelihood of local businesses.
    6. Keep pets on a leash and under control while in public areas. Clean up after your pets and ensure their behavior does not disturb others.
    7. Avoid damaging public property, including flora, benches, and structures. No unauthorized graffiti or defacement of city walls or buildings."
- "Do you have any questions? Thank you, enjoy your stay."

### Entering [[The Common District]]

**Lively Market Sounds:** Beyond the gates, the sounds of a lively market become apparent. Merchants call out their wares, and the hubbub of bargaining and friendly conversations fills the air. The market square is a central point, surrounded by stalls selling everything from fresh produce to magical trinkets.

**Colorful Banners and Festive Decorations**: Hearthstone Haven is adorned with colorful banners and festive decorations, creating a vibrant and welcoming atmosphere. The decorations change with the seasons and reflect the district's communal spirit.

**Aromas of Street Food:** The tantalizing scents of street food waft through the air as food vendors offer a variety of culinary delights. From savory pies to grilled meats and magical confections, the aromas beckon visitors to explore the diverse culinary offerings of the Common District.

**Community Notice Board**: Near the entrance, a community notice board displays announcements, upcoming events, and messages from local residents. It serves as a communal hub for sharing news and fostering a sense of togetherness.


## History
The gates leading into Hearthstone Haven, [[the Common District]] of [[Ilayas]], are sturdy and practical, constructed from weathered oak and reinforced iron. They stand open during daylight hours, a symbol of the district's welcoming nature. As one approaches the gates from the outskirts of the city, the atmosphere transitions from the rural outskirts to the bustling heart of the Common District.


## Notes

