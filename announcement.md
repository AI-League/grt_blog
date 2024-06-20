---
layout: page
title: AI Village Announcing Generative Red Team 2 at DEF CON 32
author: AI Village, Sven Cattell
date: 2024-06-10 09:00:00 +0900
category: "core"
---

[Original Post](https://aivillage.org/generative%20red%20team/generative-red-team-2/)

******

At DEF CON 31 AI Village hosted the Generative Red Team (GRT1), the world’s largest, public Large Language Model (LLM) Red Team, in conjunction with other non profit, corporate, and government partners. We brought a taste of model testing to DEF CON and as a first event of its kind much was learned about the models, and about the event. The GRT was a Capture The Flag (CTF) where you found single examples of the model behaving poorly. Hopefully it prepared you for the real thing as this year we’re asking DEF CON for real model evaluations in  a “bug” bash. The TL;DR is:

* We want you to learn how LLM reporting and testing is done professionally.
* You'll be preparing reports about flaws in the LLM you found with the [Inspect AI](https://ukgovernmentbeis.github.io/inspect_ai/) framework.
* You'll then submit the report to a platform built off of [Crucible](https://crucible.dreadnode.io/).
* The LLM vendor will then accept or reject your report. If there’s a dispute there will be several independent experts to help mediate.
* All data generated will be public shortly after DEF CON. 

An exploratory Red Team with single samples can tell you where to look but isn't a proper evaluation of the model’s performance. Each example can be dismissed as statistically irrelevant as a model that’s 100% accurate is deeply suspicious to any data scientist worth their salt. To show that your finding is not a fluke, you have to provide a representative dataset that demonstrates a statistical tendency for undesired behavior, not just single examples. This is how evaluations are done; one cannot rely on single proof of concepts for a system whose outputs are a bit random. If we're going to have coordinated disclosure for machine learning (ML) harms, then we have to rethink the way we write up "bug" reports for ML models. We need to think in terms of datasets, and ways of  processing the output into a statistical statement describing how well the target model performed. This is true for malware and spam, as well as LLMs and text to image models. The UK AI Safety Institute just released [Inspect AI](https://ukgovernmentbeis.github.io/inspect_ai/) which is a great framework for creating these evaluations and we’re going to be running several workshops with them on it to get you started. Once you have one, you’ll submit via a platform built by Dreadnode. They host the yearly AIV CTF and will extend their Crucible platform specifically for GRT2.

To advance reporting and measurement at GRT2 we are running a modified CVE - Common Vulnerabilities and Exposures - process. We will provide you with a model card, telling you the intent and scope of the target model. This describes how the model is intended to work and what it was trained to do. You’re not working to a universal definition of “vulnerability”, but instead “flaws” according to the model card. There are harms that don’t fit MITRE & CERT’s definition of vulnerability, like bias against protected classes, which we’re calling flaws for this event. There will be examples you can build off of and we’re asking you to find new violations of the model card. If the vendor accepts your flaw report we’ll pay a small bounty. If they reject it and you disagree with them we’ll have experts who will adjudicate the dispute.

We are also interested in seeing how this normal CVE process breaks down when applied to machine learning models. Lying with statistics is possible on both sides. There are several scenarios we can imagine that are undecidable with the above process. There’s already scaling issues with the [NVD being unable to keep up](https://www.cybersecuritydive.com/news/nist-national-vulnerability-database/712826/) with the deluge of vulnerability reports they receive. Additionally, there’s also disagreement between the NVD and projects like curl about individual vulnerabilities, which lead them to [become a CNA](https://daniel.haxx.se/blog/2024/02/21/disputed-not-rejected/). When the reports are statistical arguments that depend on the particulars of the model’s intent it’s only going to mean longer review periods with a larger backlog. When we add in fuzzier definitions around bias and harms this will only become worse. 

How do we resolve this issue? We don’t know, but we want to find out what goes wrong. **We want people to come and red team the process of submitting ML reports.** We will have a vendor with a smallish open source LLM, and an adjudication team acting as the root. We will pay bounties for awarded reports, and everything is going to be published immediately after the event. Every report, every appeal, every bit of data the LLM saw, and every LLM response. We hope this forms case studies that are used to create better AI transparency platforms and build trust in the ecosystem.