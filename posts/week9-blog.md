---
title: "Post 4 — From Wireframe to Data Structure in VintaArchive"
date: "2026-05-03"
description: "A Week 9 reflection."
---

This week shifted my attention from interface building to designing with data. In previous weeks, I was mainly thinking about structure, colour palette, and reusable components such as the footer. However, the Week 9 lecture made it clear that a wireframe is only the user’s view of a system. The next step is to ask what data must exist behind that screen, how those pieces of data connect, and how they might eventually be stored. The lecture frames this as a pipeline from wireframe → DDD → ERD → schema, which was especially useful for thinking about how our current VintaArchive wireframes could become a more buildable system. 

For our project, I think the most useful screen to start with is either the profile page or the marketplace listing page, because both look simple on the surface but actually hide quite a lot of data structure. A profile page is not just a visual layout with an avatar and some cards. It may require user information, saved items, published items, browsing history, favourites, and possibly relationships to themes or stories. Similarly, a marketplace page is not just a group of item cards. Each card may involve an item, an owner, a theme, an image, a condition, a price, availability status, and perhaps a short story excerpt. This means the wireframe is already implying a data model, even before any SQL is written. 
![Selected profile as the starting point for data modeling](/assets/deco2017-week9blog4-profilewireframe.png)

One of the most important ideas from this week is that awkward rows in a DDD are often a signal that a hidden entity or relationship exists. The worked Pokédex example shows that things which first look like single attributes often turn out to be lists, split structures, or relationships that need their own table or junction. This is highly relevant to VintaArchive. For example, “saved items” should not be treated as one field on a profile page; it is really a relationship between user and item. Likewise, “theme” may need to become its own entity if it carries not only a label, but also a description, visual style, or curatorial meaning. In the same way, “publish history” is not one attribute but a collection of listings connected to a user.

Because of this, I think this week’s task is not simply to add more interface code, but to improve the project’s conceptual integrity. The lecture argues that a system becomes fragile when the same concept is described differently across the wireframe, database, and code. For our project, that means terms such as theme, story, item, favourite, and listing need to mean the same thing everywhere. If we keep these concepts consistent now, later work on routes, templates, and seed data should become more manageable.

My next step is to take one existing wireframe screen and turn it into a first-pass DDD using the simplified format of attribute | description | example value, then sketch an ERD that separates user, item, theme, and story into clearer entities. This should also help our group update the task list, because once the data model becomes visible, new implementation tasks usually appear as well, including schema writing, seed data preparation, and route planning. 

Overall, this week helped me see that moving from wireframe to database is not only a technical step. It is also a design decision about what the system believes exists.
