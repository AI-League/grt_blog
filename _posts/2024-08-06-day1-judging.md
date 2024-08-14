---
layout: post
title: Day 1 GRT2 Judging Recap and Notes
author: GRT Adjudicators
date: 2024-08-09 18:00:00 +0900
category: "core"
---

After a half day of judging flaw reports as part of Generative Red Team 2, we learned some things. In response, we made a few changes to the bounties.

**(1) Bounties are going up 10x**

$500 if you meet the bar of showing where we need to change the model card. We recommend reviewing our [recommended strategies](https://grt.aivillage.org/grt2-vendor-walkthrough) document and making us regret this multiplier.

**(2) We added a new lower tier of submision**

This tier is described as:

> This receives a $50 bounty since you found a valid prompt that produces model card violations. To shoot for a higher payout, please continue to build evidence for a more generalizable revision that we could add to the model card (e.g. more diverse prompts to build out a clearly defined category).

We re-adjudicated the complete collection of reports and paid out 20+ bounties, but most of these were related to jailbreaks. Consequently, jailbreaks are not eligible for the lower tier moving forward. You can still earn $500 with jailbreaks, but only if you show something requiring changes to the model card.

# Reasons for the Change

(1) **Rates and Statistics.** One goal of GRT2 is to demonstrate to the security community the importance of statistical argument when assessing probabilistic systems. Generating a proof-of-concept for a probabilistic system is easy. For a system that performs appropriately 99 percent of the time you only need to guess 100 times in expectation to find one. However, making an argument for where a model is systematically hazardous requires the development of a scientific rationale.

(2) **Missing Sections.** We intentionally produced a model card with few details. We set up an [open world](https://dsri.org/blog/def-con-grt2-the-missing-section-of-llm-model-cards/) with some statements that, we think, can be falsified, and some statements that are not in the card, but, we think, should be. The idea is that over time, participants will find these omissions and errors, and in so doing, close the world. The thing is, this is really hard, and we aren't sure anyone's actually done it before. _Hint. Hint._

(3) **User Interface vs. API.** Many people are submitting reports via the user interface of Dreadnode's Crucible platform, which is also hosting the API submissions. Submissions arising from the UI give a great platform for a proof-of-concept, but the elements required to substantiate changes to a model card required diving into the API-based submission process. 

(4) **Education and Community.** Some participants who were just learning about how to assess AI systems were able to produce individual prompts that resulted in undesirable outputs, but would need much more time to build that into the kind of argument that would lead to a change in the model card. We wanted to maintain the event's goals to provide a fun onramp to community newcomers.

Day 2. Bounties go up.
