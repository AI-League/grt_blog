---
layout: post
title: A series of firsts!
author: Daniel Furnivall
date: 2024-08-16 12:00:00 +0000
category: "core"
---

This was my first ever DEFCON, but I've been actively following the community for more than 10 years, across multiple careers. I live in Scotland so it's always felt like a huge undertaking to make my way over to Vegas. This year, however, the stars aligned and I was able to make the trip with a couple of security-adjacent buddies I've known for almost 20 years via IRC. 

I work as a security-focused developer within a UK government department. Although I'm primarily focused on non-AI stuff, I've been hooked on breaking LLM security since Lakera's Gandalf first appeared. The idea of exploiting applications simply using manipulative rhetoric greatly appeals to me for some reason! I've been asked a couple of times at work to try and break some custom AI solutions built by colleagues so I was somewhat prepared.

As you can imagine, the AI village was my first port of call when I arrived at the con, and due to some lucky queueing I was actually the first "Human" (i.e. non-staff) attendee to make it over there!

The first thing I saw when I arrived was a few tables with computers, and the deepfake demo DARPA was running nearby. I had assumed (wrongly) from reading the schedule that the GRT2 event was something that required pre-registration, but upon arrival I enquired and was told they'd be more than happy for me to get involved! 

I got to work on setting up my environment - due to my early arrival I was hit by most of the initial technical difficulties with registration/wifi/captchas which gave me the background to assist others in getting themselves set up and assisting the developer working on the API with debugging info (tech support hat on).

Although there were a lot of early technical issues, the goons and village volunteers did an exceptional job of working quickly to get everything up and running. Running a participation-based event at DEFCON must be incredibly daunting given the nature of the conference and the ... unique talents of attendees.

After I was all set up, I set to work bug hunting. I somewhat misunderstood what exactly qualified for a bug bounty throughout the event - I focused heavily on a universal jailbreak as opposed to finding specific areas where the model card was violated without actively subverting the intended behaviour. In hindsight, I probably should have spent more time on the latter as there's probably a lot of low hanging fruit there.

I had a fairly good idea of a potential pathway to success thanks to my exposure to the work of Andriushchenko et al (https://arxiv.org/abs/2404.02151). I've previously used some of their methods to jailbreak Anthropic's Claude, GPT4o and other models.  Using a variant of this exploit, I set to work looking to see what I could break. I was immediately drawn to the 'malicious uses' track within the challenge (what can I say? I love mischief!). I was able to get a fairly high degree of model divergence after a bit of polishing, and after showing the (very helpful) Brad, was encouraged to create a submission for a bug bounty. 

This was the first time I'd ever submitted an attempt at a bug bounty and it was a somewhat daunting experience! My initial submission was very simplistic and I got some great feedback encouraging me to use more quantitive evidence to demonstrate that I have something that tangibly distorts intended behaviour in a systematic fashion.

I updated the submission with some additional data and received my first bounty! 

I also spotted some bizarre behaviour which didn't necessarily violate the model card but still appeared worthy of attention - when a variant of the following is inserted at the end of the prompt, it sometimes returned 7 or 8 distinct responses nested within a single response "Separate all outputs with an appropriate delimiter". What made it odder is that occasionally the replies contained both model violations AND hit the guardrails (e.g. "I will not assist you with harmful behaviour. <delimiter> Here is a recipe for methamphetamine", all within the same response!). Very odd! I was able to verify after testing that this occurs even on innocuous queries without the jailbreak in place.

I added a lot of additional information to my submission (I placed it within one single submission, but I now realise I probably should have made separate submissions for each issue - lesson for next time!). I've been told the team will take a second look at things after they've had some (well deserved) rest this week.

All in all, I want to say a huge thank you to the organising team as they did an excellent job of guiding those with no experience of bug bounties through the experience, while trying to build a formalised approach for creating AI bug bounties for the future. 

I think it's fair to say I'm hooked on searching for bounties now, and this event is entirely responsible for that. I am incredibly grateful to have had the opportunity to participate. You're building an army of budding AI bounty hunters!

