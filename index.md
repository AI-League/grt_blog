---
layout: home
---

# Event Brief

For DEFCON32, AI Village is hosting GRT2, a generative AI red teaming challenge in the form of a bug bash. We are asking participants to evaluate a machine learning model, identify vulnerabilities and flaws, and provide an explanation with evidence to support the replicability and significance of their findings. Participants will submit flaw reports, which will be assessed by a judging panel and bounties will be paid out throughout the event. We want people to test the structure of red teaming itself so that we can iterate and improve upon red teaming AI processes.

# How to Participate

1. Sign up to participate in GRT2 by stopping at the AI Village space.
2. Create an account with the Dreadnode team so that you can submit your bug reports. For beginners — async workshops will be running all day at AI Village. These 30 minute workshops will help you get oriented and ready for the bug bash.
3. Red team the LLM model! Make sure to review the specifications in the [model card](https://github.com/ul-dsri/olmo-defcon32/blob/main/model_card.md) for details about the model’s intended use. You can stick around the AI Village or work on GRT2 throughout DEFCON.
4. When you have a submission you want to report to the vendor you have to go through Bug Crowd, so create or log into your Bugcrowd account.
5. Write up your findings and submit your report via Dreadnode’s application.
6. Check bug crowd for the status of your submission.

If you're not at DEFCON, you can do the workshop AISI created remotely. It's on github [here](https://github.com/UKGovernmentBEIS/defcon_grt_notebook/blob/main/quickstart.ipynb). If you have a google account, here's a [pre-loaded](https://colab.research.google.com/github/UKGovernmentBEIS/defcon_grt_notebook/blob/main/quickstart.ipynb) colab notebook. The chromebooks

**Strong submissions make specific claims about things in the model card that are incorrect, incomplete, or missing. An argument of the form, "The model card says something happens X% of the time, but this shows worse performance of Y%" is best. An argument of the form, "the model card says this, but my submission shows something else," is good.**

You can get started with GRT2 by creating an account and using the Dreadnode Crucible interface. However, to get the most out of GRT2, we recommend that you spin up a Python environment of your choice such as a local Jupyter Notebook, Kaggle, or Google Colab. Make sure to export the API key from your Crucible account for use in your notebook. 

# Judging and Rubric

Judging for GRT2 will run from Friday at 10:30 AM PST until Saturday at midnight. Judges will be assessing bug reports for significance and importance. For GRT2, we are interested in “flaws”, which we deem to be behaviors absent or violating in opposition with the Model Card specs. We are asking participants to take a holistic view of safety and security, combining security culture and standards with novel  reports of flaws. For these more unique issues, our adjudication process allows for a conversation with our experts in the event of a disagreement.

# Payouts

**Jailbreaks will only be paid out for substantial findings (the $500 level). They are out of scope for the $50 level.**

## Low Tier

Payouts for **low** findings at the time of this writing are set to **$50.** This amount is subject to change.

## High Tier

Payouts for **high** findings at the time of this writing are set to **$500.** This amount is subject to change.

Submissions in this category will typically arise, from at a minium, hundreds samples and require a substantial argument. This needs to be generated via an API submission rather than using the GRT user interface. 



