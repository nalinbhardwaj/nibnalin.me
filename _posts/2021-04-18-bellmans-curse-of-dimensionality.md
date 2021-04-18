---
layout: post
title: "Bellman's Curse on Advice"
description: "On applicability of advice"
date: 2021-04-18
tags: rationality math advice
---

In dynamic programming and reinforcement learning, the most fundamental challenge we face is just grokking the high dimensionality of a state space. Go is a "simple" game whose rules can be fully explained on a single sheet of paper, yet those rules yield more board configurations than the number of atoms in the universe (10<sup>174</sup>). Given the state space, how does any solver for this game even represent these configurations, let alone evaluate them? While games are helpful toys to start with, this phenomenon of “exponential explosion” in systems is extremely common in many real-world problems, where we’ve given it the stage name: *Bellman’s Curse of Dimensionality*.

While popular study of dimensionality is usually focused on tight, mathematical systems, I’ve found that thinking about dimensionality as a metaphor in other, less well-defined systems is a surprisingly helpful problem-solving tool.

Advice, for instance, tends to fit such a model very naturally. You have an extremely large state space (_life_) where you only get one opportunity to traverse a path. To add to that, like the typical exponential problem, as dimensionality of life increases, the volume of the space of possibilities increases so fast that the available data on historical outcomes becomes quite sparse. How, then, can someone evaluate others’ advice, or look at someone else’s life to figure out what they should do with their own?

I don't claim to have a solution to this problem, but in my experience it's helpful to keep the dimensionality framework suggested by Bellman in the back of your mind as you navigate advice. For starters, thinking about the dimensions in this space independently is helpful to evaluate different states clearly:

- _Time:_ Your professor probably don’t have the best advice for you because their own experience was frozen in 1980s, and a lot about the world has changed since then.
- _Space:_ Advice about fundraising from a US entrepreneur is obviously not as relevant for someone raising in India or China.
- _Internal state:_ This is one of the harder categories to pin down. One way to think about these as some function of an individual's personality and thought processes, but I think that only scratches the surface of the dimensions this broad category intends to cover. If someone attempts to use Steve Jobs' offbeat management methods, but lacks the charisma and the "Reality distortion field" Steve Jobs is said to conjure, they're not going be as successful in their endeavours.

I think the only antidote to evaluating advice given such dimensional differences is to figure out relative distortions in the advice to your state, and "port" the advice as necessary. Don't do what Napoleon did, do what he _would_ do if he was a founder born in silicon valley during the Information Age.

Another consequence of this framework is that differences in multiple dimensions scale non-linearly. A 60 year old college professor will always have strictly less *applicable* advice, since they are separated from you in time, space and possibly internal state vs. someone of your age living in the same city as you. Note that I’m only making a claim about the *applicability* of their advice here, whether the advice itself is good or bad is a completely different question that one should evaluate separately.

I've always found it somewhat surprising how much different, often entirely contradictory, advice you can hear about any choices you can think of. When just about everyone has their own strongly held opinions about everything, it's really hard to evaluate the applicability and the net delta of any singular piece of advice.

Notably, however, there are many flaws in this framework. The most obvious flaw to me is that it isn't clear if the aforementioned dimensions are linearly independent, and treating them as such has unintended consequences (for instance, someone at different space and time but with the same internal state aren’t necessarily as bad as someone at the same space and time but wildly different internal state).

## Blessing of dimensionality

There is one other interesting result that arises from this framework that's applicable to advice: the blessing of dimensionality. In math, the curse of dimensionality leads to a conjugate that feels un-intuitive on first consideration: because exponential problems are so hard, even basic heuristics are enough to get reasonably close to optimal solutions. The simplified explanation for this is that state spaces for such problems are so large that taking random paths is exponentially worse than taking a path that’s just good enough.[^1]

When I first read Dale Carniege's "How to Win Friends and Influence People", I was extremely surprised by the blandness and obviousness of all the advice it described. Surely, I thought, this couldn't be a multi-decade bestselling book with advice that claims to have changed countless lives. Weirdly enough, Dale Carniege or Stephen Covey (author of "7 Habits of Highly Effective People") don't need their readers to develop Steve Jobs' charisma to be successful, if they take the basic, most obvious steps they'll already be good enough to be reasonably successful in life. This "blessing of dimensionality" is why most popular advice you'll find is un-specific and vague, even though, in practice, most of us will end up applying that advice to the most specific scenarios and circumstances.

On a broader point, this conjugate "blessing of dimensionality" is a good reminder to avoid traps of overthinking and taking life overly seriously. If you're taking actions with some reasonable justifications, at the end of the day, the worse you'll do in expectation is really not that bad in absolute terms: You're unlikely to end up in a ditch in a forest due to picking a wrong option at some fork in the road once, if all the other forks you've picked had some reasonable amount of consideration behind them too.

[^1]: More technical details about the set up for this class of problems are better described [here](https://en.wikipedia.org/wiki/Curse_of_dimensionality#Blessing_of_dimensionality)