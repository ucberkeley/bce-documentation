---
layout: post
title: Another pass at causation with Little & Rubin
author: Dav Clark
---
This week, we discussed:

> Little, R. J., & Rubin, D. B. (2000). Causal effects in clinical and
> epidemiological studies via potential outcomes: concepts and analytical
> approaches. Annual Review of Public Health, 21(1), 121–145.

In this article, Little and Rubin lay down some of their requirements for causal
inference, including a variety of approaches. Read the full post for some notes
and links to python code and angry physicists.

<!--more-->

### Nailing down our assumptions

Of critical importance is the authors' claim that a “stable unit-treatment
value” assumption (SUTVA) is necessary for causal inference. Put simply, SUTVA
breaks down into the following:

 - If one bunny is given a treatment, it doesn't affect other bunnies.
 - There is no (relevant) variation in treatment.

However, it seems that there are certainly situations in which we could claim
causal effects (and can't assume homogeneity of treatments) -- for example, in
psychoterapeutic settings, or when compliance with a protocol is violated by
some participants.

Michael claims another paper of interest (*Interference between units in
randomized experiments*, by Paul R. Rosenbaum) lays out a version of causal
inference that does not require SUTVA.

The authors present three forms of inference.

 1. Fisherian: We demand full randomization, and perform Null-Hypothesis
    Significance Testing (NHST) on differences between groups.
 2. Neyman's: We still demand full randomization, and generate a (frequentist)
    confidence interval around the difference.
 3. Model-based: Compute a bayesian confidence interval. The authors find this
    to be the most satisfying approach.

A breakdown of these different forms of confidence intervals, including python
code is given in this [well-circulated blog post by Jake
VanderPlas](http://jakevdp.github.io/blog/2014/03/11/frequentism-and-bayesianism-a-practical-intro/).
(But note that it's not hard to find folks who argue that [Jake's specific
examples are
ignorant.](http://madhadron.com/posts/2014-08-30-frequentist_and_bayesian_statistics.html))
