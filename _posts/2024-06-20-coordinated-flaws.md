---
layout: page
title: Coordinated Flaws Enumeration
author: Sven Cattell
date: 2024-06-10 09:00:00 +0900
category: "opinion"
---

The discussion about coordinated disclosure for ML flaws beyond the classic definition of vulnerabilities started in the first Generative Red Team. From these discussions with folks all over the industry [I wrote a process](https://arxiv.org/abs/2402.07039) that Avijit Ghosh and I turned into a paper. These are the minimum changes I see as needed to reuse the current CVE process for ML. The paper doesn't talk about the drawbacks and limitations of the "CFE" process, mostly because it's untested. In the GRT 2 we're testing some of this and I hope that the case studies are useful to people working on this and other problems.