---
layout: post
title: "Procrastination isn't laziness, it's escaping uncertainty."
date: 2026-10-18 21:00:00 +0200
categories: research
math: true
---

A few weeks ago, I noticed a range of symptoms, such as a decline in my focus, lack of motivation, and a steadily shrinking attention span.

Despite "working" all day, I was not actually getting things done.
This left me dissatisfied with what I was achieving on a day-to-day basis.

It was not until recently that I started to turn my attention to this issue.

While working, my chain of thought would often be disrupted by different kinds of urges.
They manifested in several ways, such as reaching for my phone, standing up from my desk, or opening a new tab in Chrome and starting to watch YouTube videos.

For the past few months, my daily work has mostly consisted of programming and reading research articles, so these disruptions had a great impact on whether I would achieve my daily goals or not.

---

## The pattern

Figuring out my behavioral pattern, and what caused it in these situations, took some serious self-reflection.

I found that my chain of thought was not being disrupted by random urges!
Instead, the urges were the product of uncertainty about what the next steps in a particular task should be.

When I write code, I usually describe in detail what a function should do in bullet points, sorted by implementation order. However, if one of those points is not described well enough, it causes a thinking block that disrupts my "flow" and makes me feel uncomfortable because the next step is not obvious. To escape this discomfort, I would do one of the actions mentioned above, which gave me a sense of temporary relief.

Simplified, my emotional trajectory looks something like this:

$$
\text{block} \to \text{discomfort} \to \text{quick escape} \to \text{relief}
$$

---

## Remedy

Once I pinned down what was actually happening, I came up with a simple strategy to break this habit.

The strategy combines aggressively limiting my access to the things that steal my attention, like YouTube videos, with a simple framework for getting past the thinking block when it happens.

First, to stay off YouTube while working on my computer, I installed a Chrome extension called [`StayFocused`](https://www.stayfocusd.com/), which lets me set how much time I'm allowed to spend on a certain site. Once that time is used up, the site gets blocked and I can no longer access it for the rest of the day.

Second, to stay off my phone, I bought a cheap [`Nokia`](https://nokiapoweruser.com/nokia-105-2g-2023-the-no-nonsense-feature-phone/).
This fix was a bit on the aggressive side, but it made me realize a few things, which I will talk about in a bit.

Finally, when the thinking block happens, the flow of reasoning breaks, and I start feeling the discomfort of not knowing what to do next, I open Notepad and answer the following questions:

- **Describe the issue:** Where am I feeling stuck?
- **Goal:** What am I trying to achieve?
- **Known:** What is known so far?
- **Unknown:** What is unknown, or what prevents the next step?
- **Next steps:** What steps are needed to solve this issue?

Here is an example of a recent session that was still open in my Notepad:

```text
Issue:
  I'm reimplementing the evaluation script from the paper and I'm stuck on
  the function that computes accuracy.

Goal:
  Reproduce the accuracy reported in Table 2 so I can trust my baseline
  before trying my own changes.

Known:
  - The model and the checkpoint load correctly.
  - The test set has 10,000 samples, same as in the paper.
  - My accuracy is lower than the reported one.

Unknown:
  - Does the paper drop samples longer than the max sequence length, or
    truncate them?
  - Is the reported number from a single run or an average over seeds?

Next steps:
  1. Search the paper and its appendix for "truncat" and "max length".
  2. Check the authors' GitHub repo for the preprocessing script, if exists.
  3. First run with drop, then with truncate and compare.
  4. If it's still off, move on.
```

## Why this works for me

Following this framework, I deconstruct the issue by describing it and reminding myself of the overall goal.

The issue gets divided into digestible pieces, and slowly working through the `next steps` generates small moments of instant gratification and reduces the uncertainty around the issue.

## What I found

I found several things while these changes were active in my daily work.

- Switching to a dumbphone does not need to be permanent. After using the Nokia for a week, I felt how much easier life is when I have access to modern features like online banking or Google Maps. However, using it broke my bad habits, and after switching back to my smartphone, I no longer have the urge to grab it whenever I'm bored.
- Blocking YouTube (and other attention-stealing sites) made me realize that YouTube was the only thing more interesting than working on my projects, so restricting it really boosted my enthusiasm for my research.
- The framework is essentially the self-reasoning framework I described in my previous [post](https://www.gabrielmarvin.com/research/2026/08/18/self-reasoning.html), but on a micro scale. It can be cumbersome to go through all the steps for a trivial thinking block. In that situation, I advise describing the issue, going for the quickest and dirtiest solution, and revising it later. When you are really stuck, though, the framework is a lifesaver, and the self-reasoning session that comes out of it can be useful in the future.
