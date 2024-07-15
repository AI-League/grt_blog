---
layout: page
title: Prior Events
author: Sven Cattell
date: 2024-06-10 09:00:00 +0900
category: "opinion"
---

This isn't the first event or program that focuses on the issues of safety and bias in Machine Learning (ML). The first Generative Red Team also combined ideas from the responsible ML and security communities and there were several events before that. It is, however, the first one that's paying bounties. 

Twitter's "[Bias Bounty](https://blog.x.com/engineering/en_us/topics/insights/2021/algorithmic-bias-bounty-challenge)" in 2021 was a competition with specific rules of engagement. CDAO's [bias bounty](/Users/svencattell/code/flaws/_posts/2024-06-20-coordinated-flaws.md) with Bug Crowd is closer, but is still a competition. Once all the prizes are awarded in a competition, the organizers are done. They don't need to justify why an award wasn't issued to everyone who lost. Actual bounty programs do. Saying "no" to a CVE number means the security researcher can appeal to the root. On Bug Crowd there's a "make-it-right" fund that they pay out (not the vendor) if the vendor didn't pay a bounty they should. Too many uses of this fund might get the vendor removed from the platform. For in-house bounty programs a denied find means the finder can go public immediately as it's not a "vulnerability". In all situations, there's a cost for saying no to a bounty that doesn't exist when not awarding an entrant a prize in a competition.

There are, however, 2 bounty programs for AI systems in place, one at [Google](https://security.googleblog.com/2023/10/googles-reward-criteria-for-reporting.html?m=1) and one at [Microsoft](https://www.microsoft.com/en-us/msrc/bounty-ai). Both are great, and I'm excited to hear what they've learnt. However, both don't include bias and other harms as in-scope. I wouldn't if I were them, due to the uncertainties involved. Evaluation of LLMs is difficult at the best of times, requiring a carefully constructed dataset and evaluation protocol to accurately assess a model's capabilities on a task. Small mistakes can lead to models being optimized for the wrong thing (see the alignment problem in reinforcement learning) and so peer review is key to creating good assessments. For an outside reporter to prove some kind of unwanted bias in a model would require quite a deep level of trust between the reporter and vendor. 

Competitions don't prepare our systems for a coordinated disclosure with a scope that includes bias and less tangible harms. The potential award of either money, or a CVE number, to each reporter adds complexity to predecessors that dealt with bias with a competition format. They do, however, prepare us. Now is the time is perfect to run this. 