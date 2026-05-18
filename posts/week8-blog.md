---
title: "Post 3 — Modularity, Consistency, and Early Build Decisions for VintaArchive"
date: "2026-04-26"
description: "A Week 8 reflection."
---

This week was the first time VintArchive started to feel like an actual website rather than a set of separate ideas. In Week 7, our group had already clarified that the project should be led by an exhibition experience rather than functioning as a standard resale platform. This week, that idea had to start taking shape across actual screens. One important step was that we completed the main wireframes for the core parts of the site, including exhibition, marketplace, upload flow, profile, and chat. Seeing all of these interfaces together made the project feel more coherent, but it also made inconsistencies much easier to notice.

One of the clearest decisions this week was confirming a brown-based colour palette for the site. This choice was partly aesthetic, but not in a superficial way. We chose brown because it immediately suggests warmth, age, and materiality, which felt much more aligned with a vintage archive than brighter or more neutral palettes. At the same time, once I started applying the colours to screens rather than moodboard references, I realised that some combinations did not provide enough contrast. In other words, the palette worked conceptually before it always worked functionally. That was a useful reminder that choosing a visual direction is not the same as proving it can support readability across a full interface.
![Initial footer for VintaAchieve](/assets/deco2017-week8blog3-palette.png)
Figure 1. Colour palette that choose for website.

At the same time, because our team members were working on different pages, another challenge was maintaining a shared visual language. It was not enough for each page to look individually “good.” They also needed to look like they belonged to the same system. That meant we had to keep returning to questions such as spacing, typography, image framing, and how much decorative styling each section should carry. This is one reason why I found this week’s lecture focus on modularity useful: consistency is not only about code reuse, but also about repeated design decisions appearing stable across the whole site.

I also completed the first coloured HTML version of the footer by myself, although it is not fully responsive yet. I chose to build the footer before moving on to more specific pages like the item detail page because it is one of the few elements that will appear across nearly every screen. It is basic, but also foundational. Building it early helped set the tone for the rest of the site and gave us a stronger shared reference point for how the site should feel overall. In that sense, it was not just a bottom section of the page, but an early test of whether our visual system could hold together in code.
![Initial footer for VintaAchieve](/assets/deco2017-week8blog3-footer.png)
Figure 2. First coded footer component, developed as an early reusable block for maintaining consistency across pages.

Another design direction that became clearer this week was the marketplace layout. While working through the wireframes, I moved the item display away from a standard rigid grid and toward a more waterfall or masonry-style arrangement. The reason was not only visual variation. I wanted the marketplace to feel slightly more curated and artistic, so that it still connected with the exhibition side of the platform rather than reading as a generic second-hand catalogue. That said, I am still aware this may create trade-offs later in development, especially around responsiveness, scanning speed, and layout control.
![Wireframes for VintaAchieve](/assets/deco2017-week8blog3-wireframes.png)
Figure 3. Early wireframes for VintaAchieve, used to test how exhibition, marketplace and profile sections might share a consistent vintage visual language.

In terms of team roles, I am mainly responsible for the profile and marketplace sections, while Cassie is stronger in the exhibition pages where first impression, composition, and aesthetic atmosphere are especially important. That division has helped us work more efficiently, but it also reinforces the need for repeated alignment so the site does not split into visually separate parts.

Overall, this week was less about inventing new features and more about testing whether our early decisions could stay coherent once they became real screens and early code. At this point, I feel like the project has a clearer tone, but also more obvious weak points, which is probably a good sign.
