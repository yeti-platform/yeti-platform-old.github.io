---
layout: post
cover: 'assets/images/cover-snow.jpg'
cover-copyright: Tadamasa Sawada
cover-copyright-link: https://flic.kr/p/S5pKHm
title: Yeti's ecosystem
date: 2017-10-06 08:00:00
tags: use-cases
subclass: post
author: tomchop
---

Yeti is a relatively new player in the threat intel platform game. How does it fit in with all the other tools that are out there? FAME? FIR? MISP? TheHive? Let's have a look.

<!--more-->

## Yeti is a social animal

It might not be known to most cryptozoologists, but Yeti is a social animal. Sure, it may be good enough as a threat actor encyclopedia, but there's so much more you can do with it!

Yeti's ideal world is a world where all its features are put to good use. That includes data-oriented features such as feeds, analytics and exports, but also more high-level information such as describing TTPs and tying them to different actors. FAME and FIR, by the awesome CERT Société Générale team have features that allow them to work closely with Yeti, both pushing and pulling information.

### The FIR - FAME - Yeti triad

Yeti, [FIR](https://github.com/certsocietegenerale/FIR){:target="_blank" class="external"} and [FAME](https://certsocietegenerale.github.io/fame/){:target="_blank" class="external"} provide most of what anyone could ask for in terms of quick and efficient incident response.

Besides being an extensible incident management platform, FIR parses any observables present in an incident's description or comments and sends them to Yeti to see what it knows about them, displaying any matches. On the other hand, unrecognized observables can be pushed to Yeti and tagged.

FAME is also closely integrated with Yeti. Whenever observables are extracted from a sample (through one of [FAME's many modules](https://github.com/certsocietegenerale/fame_modules){:target="_blank" class="external"}), they are matched against what Yeti knows and results are shown in the FAME analysis result page. Unknown observables, once again, can be tagged and pushed to Yeti so that association can be quickly made with other submitted samples.

![Yeti's small family]({{ "/assets/images/yeti-eco1.png" | absolute_url }}){:style="width:90%;"}

This is probably one of the best ways you can setup Yeti in your day-to-day incident response workflow. This setup works particularly well with teams that have dedicated rotations to each task (threat intelligence, incident management, malware analysis, etc.).

### Interaction with other services

Yeti is one of the many tools to have been released more or less recently that aim to make threat intelligence management easier. There's a very large combination of tools with which compile feeds and enrich them, achieving a similar result to the one described above.

The good news is that Yeti is very flexible in that way, and having both feeding and exports capabilities, can easily be plugged in your existing ecosystem. Yeti is very likely complimentary to other systems that already exist and will give you a different approach on your data and the intelligence analysis you might carry out on it.

![Yeti's extended family]({{ "/assets/images/yeti-eco2.png" | absolute_url }}){:width="90%"}

[MISP](http://www.misp-project.org/){:target="_blank" class="external"} can be used as a feed to Yeti, propagating information from the MISP communities you're connected to directly to your defense systems in a way they can understand them. [TheHive](https://thehive-project.org/){:target="_blank" class="external"}, (or rather, [Cortex](https://github.com/CERT-BDF/Cortex){:target="_blank" class="external"}) can use Yeti as a source of enrichment for network artifacts.
