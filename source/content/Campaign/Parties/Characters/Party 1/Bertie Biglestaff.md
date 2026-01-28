---
tags:
  - "#Character"
  - "#Player"
art: z_Assets/People/Bertie 7.webp
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
>>---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>>---|---|
>> **Played By** |  `INPUT[textArea:playedby]`
>> **Character Sheet** |  `INPUT[textArea:charactersheet]`
>> **Pronounced** |  `INPUT[textArea:pronounced]`
>> **Aliases** | `INPUT[list:aliases]` |
>> **Ancestry** | `INPUT[Ancestry][suggester:ancestry]` |
>> **Heritage** | `INPUT[Heritage][suggester:heritage]` |
>> **Gender** | `INPUT[Gender][:gender]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]`
>> **Age** | `INPUT[Age][:age]` |
>
>> [!metadata|metadataoption]- Info
>> #### Player Info
>>  |
>>---|---|
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):religion]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):ownedlocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>> **Which Party** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Condition** | `INPUT[Condition][:condition]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Played By: `VIEW[{playedby}][text]`
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Ancestry** | `VIEW[{ancestry}]` |
> **Heritage** | `VIEW[{heritage}]` |
> **Gender** | `VIEW[{gender}]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Age** | `VIEW[{age}]` |
> ###### Info
>  |
> ---|---|
> **Occupations** | `VIEW[{occupation}][text]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!kirk|info] Info
>

> [!metadata|charactersheet]- Character Sheet
> ```custom-frames
frame: Demiplane
style: height: 700px;
>```

> [!metadata|servicerequests]- Service Requests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(customer, this.file.link) AND contains(tags, "Service") AND !contains(status, "✅") AND !contains(status, "❌")
> SORT file.name ASC

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

## Appearance

He has a mop of brown hair with long blonde streaks going through it, the same colour as the rest of his family, he keeps it messy as a statement to others that he does not abide by societies rules. He has piercing green eyes, also like his family, that show a fascination of everything around him and wanting to learn more, almost manic in its desire for more. His nose is crooked, clearly broken several times throughout the years, most likely from scuffles with his peers, it only further pushes the idea that he rebels against societal norms.

His build is average to slight, he is 5”10 and skinny, as he has never had to physically exert himself because of his upbringing and specialisations. His clothing is expensive and well made, but scruffy. He wears a formal shirt that is always half untucked with an open waistcoat of a deep maroon, his trousers are stained with ink and clearly stuffed with trinkets and collectibles. He carries a satchel over one shoulder that is always open and stuffed with papers. The only wizard stereotype he seems to keep to is a beard which is of medium length of the same colouring as his hair and is clearly unkempt.

 

## Background

He is the only member of the Dubois family who has showed any latent ability with magic and expressed that very early in life. As soon as he showed magical capabilities his parents shipped him off to the Arcanamirium, so he has had minimal interaction with his family through his most formative years, and he resents them for that. His animosity to hierarchy and those who see him as better than himself led to his tutors and peers to dislike him throughout his time at the Arcanamirium. He constantly got into arguments with his tutors on the application and cross over of magic as he thought there had to be more than the strict lineation of magic schools, which led to a lot of disdain from his tutors who thought they knew better.

 

When he finally left his education, his family insisted that he use his skills and abilities to further the family name, because of that he has an aptitude to understand magical items and their properties quickly, albeit he resents having to do this and be the family specialist in this regard. He only reluctantly continues to do this as his family provides him with a stipend which allows him to pursue what he wants in his spare time and afford a separate house in the upper quarter. A lot of his work requires him to work alongside Fleur which has led to them building a bond together, which includes a hatred of their siblings who think they are better than the youngest siblings. Therefore, he attends most of the same galas and parties as Fleur to provide magical assistance on verifying information acquired and on artifacts presented to them for barter, or explanations on what customers are looking to acquire from the family business.

 

He resents his place in society and how he was raised, because of this at the soonest opportunity he changed his surname to Biglestaff to distance himself from the Dubois’ and took on an accent and mannerisms to try and place himself more firmly into the upper echelons of society, which when mixed with his appearance and history with these people (nobles, and richest of society), led to him being excluded even more until they required something from him.
## Ideals
### Loves
His sister Fleur, he wants to see her happy and to flourish away from the confines and expectations of the Dubois family.

Gathering more knowledge of anything available, especially if it helps further his own goals of becoming the best wizard around and proving his theories are correct.

Exploring more about the world as a whole, he has only experienced this through books so far and desperately wants to see what is out there for himself.

### Hates
Current societal norms and expectations of behaviour and appearance.

The pressure and reliance on his family and parents to do what they want in order to get just a little of what he wants. His other siblings, as they are so self-serving and resent him for not wanting to further the families interests.

Religion, he knows the gods are real, but he hates how subservient people are to them. He wants to use magic to lead people away from their dependence on religion, but this is mostly an afterthought if he can get what other things that he wants instead.

## Goals
He wants to achieve the highest rank available to wizards and prove how the various magic schools can be linked together by the intrinsic nature of magic for which he had so much contentious arguments with his tutors while in education. He stubbornly believes he is the only person that can see that and has dismissed others who have presented similar theories before.

He wants what he truly believes he deserves, recognition and standing in the society he claims to hate. He wants to belong to a group that want him and believe him, but always struggled to fit into.

He also wants to help Fleur to achieve what she wants, which is freedom from the family which so easily uses the pair of them. However, he struggles to see how he can help her to achieve that.


## History

Born in Ilayas and has never really left the city confines apart from sporadic family trips near the city in the countryside. Has led to a very insulated viewpoint of the world but has also led to a very curious mindset of everything else that is out there and wants to experience it as much as possible.
 

Fourth child of five from his parents Jean-Pierre Dubois and Marie-Louise Dubois. Jean-Pierre is a merchant specialising in acquiring rare materials that businesses need but cannot easily require. He spends most of his time away from the city acquiring the specialised requested materials in a long train caravan that he owns, maintains and protects. The company is named The Dubois Emporium and Logistics, he has expanded this company after taking over from his forebears over the last couple of centuries and diversified its acquisitions. Because of this the family is very wealthy and has the ear of several significant members of the council of nine, however as they do not come from a noble familial line the family has struggled to gain the recognition that Jean-Pierre believes they deserve. Marie-Louise is anything but a mother, she has spent most of her time working the logistical and financial side of the business and throws herself wholeheartedly into this line of work, to the point of neglecting her children by letting them essentially be raised by nannies, servants, and tutors. She has also actively encouraged competition between her children over the years which has led to conflict between them to the point where several don't talk to each other.
 

His siblings are:

**Eldest** - Alexandre Dubois - Heir apparent to the business and family name. Received the best education that money can buy for someone, and from an early age showed interest in taking over the family business. From the age of 12 started accompanying Jean-Pierre on his caravan trips and at the age of 18 started his own caravan and is often out of the city acquiring the specialised goods that are requested. Primarily takes his caravan out to the Kingdom of Oshad due to the requests that are made by customers.

Because of his education and spending most of his time away from home and being but on a pedestal by his parents, he has total disdain for almost all his other siblings except for Genevieve. He particularly dislike Bertie due to the difference in upbringing and Bertie's ability to cast magic.
 

**Second eldest** - Genevieve Dubois - Eldest daughter and firmly rooted into the business. Like Alexandre had the best possible education affordable and quickly showed an aptitude for logistics and diplomacy. Settled herself into an apprenticeship underneath her mother to learn as much as possible on the intricate running's of the family. She has a pompous superiority complex and believes the business would fail without her direct involvement, which has led to constant conflict with her mother Marie-Louise, who also share that mindset. Genevieve has attempted several times to drastically change the workings and machinations of the business under Marie-Louise's nose but was caught and reprimanded each time. That has not stopped her though and she is now hellbent on plotting away to remove her parents from the business so she and her brother Alexandre can fully take over and run the business to her ideas.
 

**Third eldest** - Jean-Pierre Dubois the second - The Fredo of the family. The family fuckup, too high expectations were placed on him by his father and namesake. He has no interest in the family business and crashed out of his formal education very early in life. He mostly just resides at home, doing nothing but lamenting his position in life and drinking expensive wine to the point of being blackout drunk. Until he comes up with a hairbrained scheme that he is sure will make him fabulously rich, famous, and his parents proud. They always end in disaster, and a few times have ended in violence when he inevitably fails, and his backers lose all of their investment. His latest scheme involves taking over failing pubs and taverns and trying to turn them into cabarets to make them profitable. He currently owns four of them primarily in the lower quarters of the city, one is making a profit (The Vibrant Vignettes) where all the other important families fuckups or spare heirs go to drink their sorrows away, the rest are failing badly. Shunned by all of his family he is alone, the only attention help he gets is from his father, who injects much needed funds in a regular stipend to him and his business ventures.

 

**Youngest** – Fleur Dubois – The youngest child of the Dubois family, she is essentially a caged canary. The most beautiful of all the children she excelled in her formal education and has a particular skill and diplomacy and understanding her environments around her. She attends a lot of galas and parties, where she uses the opportunity to trade in secrets and information to others and frequently asks Bertie to help with this. Her parents have better ideas as to her worth, and let her attend the galas, in the hope she finds a suitor who is a noble that she can marry. This would allow the Dubois family to finally achieve the noble lineage they have so desperately tried to acquire over the years. She resents this and has been secretly saving up her funds from being an information broker in the hope of escaping her family and setting herself up independently where she can live abiding only by her own morals and whims and continuing with what she is passionate about, trading information.

## Notes

