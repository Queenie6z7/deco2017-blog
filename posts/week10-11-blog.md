---
title: "Post 5 — Moving from Feature Building to Clearer System Structure"
date: "2026-05-15"
description: "A Week 10-11 reflection."
---

Over the last two weeks, our project has started to feel more real, but that has also made some structural problems easier to see, our work on VintArchive has started to shift from building isolated interface pieces toward making the prototype feel more like a connected system. Earlier in the semester, many of our decisions were about concept, wireframes, visual language, and data structure. At this stage, the challenge is slightly different: we now have enough pieces built that the main question is no longer what should exist, but how these parts should work together clearly and meaningfully for users.

One important step forward was the successful deployment of our map API. At the moment, it functions mainly as a technical proof of concept, but its real value is not simply that a map can be displayed. What matters is how it could support the project’s broader goals. In our case, location could become useful for showing where vintage objects are based, where sellers are located, or whether a local exchange is realistic. This is especially relevant because VintArchive is not only an exhibition-led archive but also includes marketplace behaviours. In later development, the map may help users judge whether an in-person trade is practical without needing to reveal overly precise private information too early. That means the map feature is connected not only to functionality, but also to trust and responsible information design.

![Deployed map view for early location-based browsing](/assets/deco2017-week11blog5-api.png)

A second major step was building a dataset of 50 vintage items and creating a dedicated vintageItems.ts data source. This was an important shift from placeholder content to a more reusable and scalable structure. Instead of designing around empty cards, we are now starting to test how real item names, categories, prices, and images affect layout, filtering, and browsing behaviour. This also makes later development more realistic, because features such as listing cards and detail pages can now draw from a consistent source of data rather than manually inserted content.

![Folder of collected vintage item images used to build the dataset](/assets/deco2017-week11blog5-images.png)

At the same time, this data exposed a problem in our current tag system. Right now, there are too many tags displayed at once, which makes the interface visually noisy and harder to scan. More importantly, broad categories such as clothing are mixed together with narrower descriptors such as late 1990s, which weakens the logic of filtering. Rather than treating all tags as equal chips, the next step is to restructure them into a clearer hierarchy. A more workable approach would be to separate primary categories (for example clothing, accessories, bags, digital products, other) from secondary style or era filters (such as late 1990s, 1920s inspired, minimalist vintage). Technically, this suggests a stronger distinction between a single item category field and a separate tag relationship, rather than one flat list. From a UI perspective, this could also be implemented through progressive disclosure, grouped filter sections, or filter chips that only appear after a main category is selected. This would improve both usability and code organisation, since the filtering logic would become more predictable.

![Current marketplace filtering interface showing the overloaded tag structure](/assets/deco2017-week11blog5-tags.png)

Another issue appeared in the Profile interface. At the moment, sections such as Account, Published, Wishlist, and Orders have all been combined into one long page, which means the tab structure is not yet functioning as intended. This weakens the clarity of the profile flow, because users are shown too much at once rather than seeing content change in response to navigation. The next step is to separate these sections properly, either by routing or by conditional rendering tied to an active tab state. This is not only a front-end clean-up task; it is also about aligning the interface with the mental model implied by the tabs themselves.

![Current profile page where Account, Published, Wishlist, and Orders are still combined in one view](/assets/deco2017-week11blog5-profile.png)

Finally, although the listing cards are now much more developed, the item detail page is still missing. This is a significant gap because it breaks the user journey between browsing and understanding an object in depth. A vintage marketplace needs more than thumbnails and prices; it needs a page where material, condition, story, category, and exchange options can be understood properly. My goal is to complete the first version of this detail page by the end of the week.

![Early state of the item card/listing view before the detail page is completed](/assets/deco2017-week11blog5-items.png)

Overall, these two weeks have made it clear that the next stage of development is less about adding more features, and more about improving structure, hierarchy, and flow. The prototype is becoming more real, but that also means inconsistencies are becoming more visible. In that sense, the problems we are finding now are useful: they show where the system still needs clearer organisation before it can feel coherent to users.
