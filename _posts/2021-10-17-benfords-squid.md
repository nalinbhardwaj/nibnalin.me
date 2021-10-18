---
layout: post
title: "Benford's Squid Game"
description: "Does Squid Games follow Benford's Law? 🦑🔫"
category: 
tags: data visualization
---

# Does Squid Games follow Benford's Law? 🦑🔫

**NO**, but it's surprisingly close.

{% include squid-games/chart.html %}

## What is Benford's Law, anyway?

Benford's Law is a somewhat surprising result on distributions that predicts the probability of an arbitrary digit being the leading digit of numbers in a "natural" dataset. For instance, it expects \~30% numbers in the dataset to have the leading digit 1 (like 1, 13, 102...). There's a much more detailed discussion on Benford's Law on [Wikipedia](https://en.wikipedia.org/wiki/Benford%27s_law) and how it's often used to identify statistical anomalies like [election fraud](https://www.reuters.com/article/uk-factcheck-benford/fact-check-deviation-from-benfords-law-does-not-prove-election-fraud-idUSKBN27Q3AI) and [tax fraud](https://www.forbes.com/sites/taxnotes/2021/08/19/can-benfords-law-detect-tax-fraud/).

## What is Squid Games, anyway?

Squid Games, if you haven't seen it yet, is a new Korean television show from Netflix centered around a fictional battle royale game. Throughout the show, players (and game staff) are primarily identified by numbers, which makes it an interesting dataset to check for Benford's Law.

At the top of this post is the plot of observed frequency of leading digits in the dialogue from all episodes of Squid Games (scraped together from Netflix subtitles) and a comparison with what Benford's law would expect. For 1 and 2, the observed frequencies fall pretty close to the Benford's law prediction, but it seems the creators really didn't like 3 and 5. It also does seem oddly suspicious when you look at [lists of notable characters](https://asianwiki.com/Squid_Game) that so few of them had labels in the 300s.

## What about individual episodes?

Here's a plot of the breakdown of which episode sourced how much frequency to each digit.

{% include squid-games/chart-2.html %}

If you are interested, the iPython notebook for this data analysis is [here](https://colab.research.google.com/drive/1xmVVtfAs3-KkSZcxzSPFQgS3PmhMPnd4?usp=sharing). I'm not certain about the legality of sharing scraped subtitles, so I'm not going to include those. For more such data analysis (or reading about all the random things I think about), consider subscribing to my Substack.
