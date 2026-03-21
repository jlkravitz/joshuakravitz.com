---
author: Joshua Kravitz
pubDatetime: 2019-11-09T16:32:41-08:00
title: "What Is Causality"
slug: what-is-causality
featured: false
draft: false
tags:
  - causal-inference
  - statistics
description: "A quick pitch on what causal inference is and why it's important."
---

When I meet new people or talk with friends, many wonder what I mean when I say I'm interested
in causal inference. I then go on to give a short pitch on causal inference and observational
studies. I figure I'd write down what I say in a blog post. Be warned that I have only been studying
this stuff for around a year, so I'm by no means an expert; some of what I say, too, might be
oversimplified or plain wrong (hopefully not the case, but if something seems suspect, let me know!).

## Correlation versus causation

Most people have heard of this distinction, so I won't spend much time here. Basically, if you have
two variables A and B, just because they correlate with one another does not mean that A causes B.
There are many examples of [spurious correlations](https://www.tylervigen.com/spurious-correlations)
that clearly are not causal in nature (an absurd example from that site: the divorce rate in Maine is highly
correlated with the per capita consumption of margarine).

Ok, so why do we care about causality / causal inference? Because it's all about imposing some change on the
world: we want to know if some treatment, policy, training or other behavioral intervention is effective.
The FDA requires researchers to provide convincing evidence that a new drug is effective before they'll
allow its approval for general use: Does the drug improve quality of life? Extend life? These are questions
of _causality_.

## Randomized Controlled Trials (RCT)

The gold standard of causal inference is the randomized controlled trial. Let's continue with the FDA
example and say some pharmaceutical company has a new experimental cancer drug that they want to bring to market; they have
to provide strong evidence that that drug improves outcomes (in this case, increases length of life). How do you do this?

To start, let's note what _won't_ work. If the company lets anyone enroll in their study and take the drug,
could they simply compare that group to those who don't take the drug? Probably not -- those who chose
to take the drug are probably different (in some sense) than those who don't. For example, those who take
the experimental drug may be on their last leg of life and so have nothing to lose by trying one last thing.
Then, those who take the drug will generally have died earlier, even if they hadn't taken the drug at all.
This will lead us to underestimate the effectiveness of the drug -- we'll think it made many people die!

To avoid issues like this, we ideally want the group that takes the drug to look very similar to the
group that doesn't take the drug (in technical terms, the treatment and control groups should be balanced
in their covariates). That's where the Randomized Controlled Trial (RCT) comes in. In the RCT, the pharmaceutical
company randomly assigns (think: a coin flip) each individual to take or not take the drug. If enough patients
are enrolled in the study, we'll have two groups of people that look relatively similar.

## Observational Studies

RCTs are all well and good, but what if I don't have the time or money to run one? More importantly, what if
it'd be _unethical_ to run one? To see if smoking causes lung cancer, I probably can't get away with forcing
some people to smoke. There has to be another way.

Observational studies use observational data, which is data that is passively collected from the world. We might
have data on who does and does not smoke and whether or not they've been diagnosed with lung cancer. Can we say
with certainty whether smoking causes lung cancer from this data? Maybe. The problem is similar to the one described
earlier -- the people who smoke and don't smoke might be very different. For example, the smokers might be generally
lower income and live in areas with worse air pollution, house maintenance, etc: maybe this is what's actually causing
the lung cancer.

Much of the world of observational studies tries to emulate what an RCT does: make the treatment and control
groups look similar. An in-depth exploration of how one might do this is beyond the scope of this post, but
as a teaser, one common method is "matching," where you find pairs of people in the treatment and control
groups (say, smokers and non-smokers) who look very similar (say, live in nearby neighborhoods, have similar
incomes, are of the same gender, etc). Combining these pairs together, you can form two groups that look more
alike.

**A word of warning:** even now, you can't claim that your results are as powerful as those of an RCT.
One major problem is that there might be some variable that's the actual cause of lung cancer, but that you don't
have available in your data set (this is called "unobserved confounding"); a major assumption of any observational
study is that you can ignore these variables.
Good observational studies require careful analysis and consideration of assumptions like these.
A professor of mine this quarter put it well: "A good observational study will spend 10% of its paper on the results and
the other 90% testing its assumptions."

## Conclusion

Causality is about discovering the world around us, and the study of causal inference provides a framework to
facilitate that discovery.
If you're curious to learn more, look up Don Rubin's potential outcomes
framework -- it's the foundation of much of this work.
