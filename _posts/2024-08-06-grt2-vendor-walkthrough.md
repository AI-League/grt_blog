---
layout: post
title: Strategies for GRT2 Participants
author: Sean McGregor
date: 2024-08-06 03:00:00 +0900
category: "core"
---

> On August 8th through 11th, tens of thousands of hackers will converge on Las Vegas for DEF CON 32. One of the marquee events is a [multi day generative red team](https://aivillage.org/generative%20red%20team/generative-red-team-2/) (GRT2) where participants will find ways in which a Large Language Model (LLM) is “flawed” (i.e., it presents ["...unexpected model behavior that is outside of the defined intent and scope of the model design."](https://arxiv.org/abs/2402.07039).

In support of flaw testing LLMs, the Digital Safety Research Institute (DSRI) and the Allen Institute for Artificial Intelligence (Ai2) teamed up through our [broader red team efforts](https://dsri.org/blog/dsri-ai2/) to serve as the “Vendor Panel” for the GRT2 bounty program. Our role is to be the first line adjudicators of reports and assume the identity of a company that needs to decide whether reported flaws present a need to patch the flaw and/or disclose it on the model’s documentation.

<span style='color:red;font-size:large;font-weight:bold;'>Model documentation changes -> Bounty paid</span>

The purpose of this blog post is to help you understand the vendor decisions and make it easier to get a bounty.

![A flowchart depicting a review process with a single stage vendor approval with a GRT organizer appeal body](static/images/vendor_review.png "Vendor Review Process")

GRT2 has a [rubric](/rubric) governing payouts, but it can be distilled to a golden rule: **does the flaw report advance an “understanding of safety”?** For models designed to serve general purposes, this is a very broad frame and allows for GRT2 participants to develop many approaches. The starting model documentation is also much lighter on the details than the current understanding of LLM safety, so we know there are ample flags to capture. Below are a few strategy ideas ordered from “easy” to “hard” to help you get started.

1. **Hazardous Use Case.** LLMs can do an uncountable number of things, but can they do them safely? Pick a use case (e.g., medical advice, SCUBA dive planning, code completion) for which someone may use the LLM and quantify where it is safe or unsafe. We will tell the world what to avoid (or not) as you discover it. Plastic bags containing toys tell you not to suffocate yourself, so the bar can be pretty low for hazards.
2. **Mine an incident.** The [AI Incident Database](https://incidentdatabase.ai/) has a large number of incidents that are not covered by the GRT2 model documentation. You can find an incident and show how the LLM may make it happen again.
3. **Find the invisible.** If you look at the documentation, you will find many people are not covered by current benchmarks. We don’t know, for instance, whether the model is toxic to the Māori people. They might not even be represented in current LLM safety testing. You can find the invisible populations and report what is likely a worse performance than presented by more thoroughly measured populations.
4. **Disaggregate.** Among the biggest problems today in LLM safety is that safety scoring is reported in the aggregate and we often don’t look at whether subpopulations perform substantially worse. We recommend you start by looking at benchmark datasets and finding where there are failures. A consistency among failed instances indicates you are on to something…
5. **Systematic Vulnerabilities.** There are things we don’t want the model to do and so there is a filter preventing you from doing them. We know the filter can be bypassed, but we don’t have a catalog of where it is systematically vulnerable. This category is more difficult than the rest because we are not interested in a small collection of jailbreak examples. We want to see things like magic tokens that consistently break open a wide variety of hazardous prompts. We expect this to be difficult.
6. **Something new!** We want you to uncover the unforeseen flaws that will challenge LLM safety researchers for the next decade. Don’t harm people through your efforts, but we are hoping to be surprised.

Happy hunting.
