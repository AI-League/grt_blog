---
layout: home
---

# GRT 3

Unfortunately AI Village did not make it to run GRT3 this year at DEFCON. We do not have sufficient networking to run this event at DEFCON. 

We will run it online in about a month with partners. Please signup [here](https://auth.aivillage.org/login) to recieve an email with more information.

## Philosophy

Model reporting needs to be about learning more about the models. Not flaws, not vulnerabilities, not weaknesses. Those are useful bits of information, but the process of disclosure works better when viewed as an aspect of applying scientific method to these black boxes. This is how things used to be, before the explosion of LLMs brought thousands of AI experts to the yard. However, with the extra capabilities these models have, we need to work holistically, including useful behaviors like math and tool use and not just focus on the mistakes. What we used to do was write papers about an interesting aspect of the model and post them to arXiv, not throw prompt injections at a model until it broke and call it a day. Aside from just running stock evaluations, this is what “AI Red Teaming” largely became. The hype for this type of “AI red teaming” in policy circles is dying down because it’s largely unproductive as is. The older academic publishing meant we used to learn about the models when we “red teamed” them. The incentive was interesting findings, not pwns. We need to go back to that. 

What I’m proposing is a process for learning about models and is as much about a cultural shift as a system for probing models. This is an attempt to take the best ideas from security and data science and combine them together to more effectively understand the strengths and weaknesses of AI models. We’re bringing together the academic DNA of machine learning with the hard fought lessons from security:
Make things easy with automation: Software Bill Of Materials took off after we automated the process. The idea was good, but making it easy unlocked it.
Triage is the hardest aspect of Disclosure: Even in far less subjective traditional security managing figuring out what to do with submissions is hard.
Scoping is important: Specialized knowledge is often required for determining if a report is valid. A general disclosure form, like the portal without a robust triage systems behind it, is inefficient.

## Objective

What I built is a completely in-browser evaluation framework with a WASM pipeline or UK AISI's inspect. It's got some tricks to make it easy to manage adding data to evaluations. It is very cool, but is fairly network heavy. We'll add some polish and run the GRT3 in September.