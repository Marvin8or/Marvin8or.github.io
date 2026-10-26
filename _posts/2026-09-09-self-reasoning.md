---
layout: post
title: "How I stay sane when working on complex topics."
date: 2026-09-09 21:00:00 +0200
categories: research
---

In this post, I describe a simple process I use to navigate the open-ended nature of research projects.

At the beginning of every project, I often have a clear end goal but considerable uncertainty about which approach will work.
I often find myself getting stuck at decision points where I'm not sure how to maintain the direction of the project’s central purpose.
I can think of many things to build, improve, or investigate, but I struggle to distinguish high-impact work from noise.
In the past, this often caused me to drift into tasks that are interesting but irrelevant to the project’s main objective.
As a consequence, making me miss out on opportunities to showcase my abilities and produce meaningful results.
It was not until I started my PhD that I gave serious thought to how I could improve in this area.

---

Imagine yourself as a painter. When you focus closely on one small section of a canvas, it can be difficult to judge how that section fits into the whole painting.
By stepping back, the broader composition comes into view. You may notice imbalances in color, shape, contrast, or proportion that would be difficult to recognize while concentrating on a specific detail.

In the same way, when I am deeply focused on a particular implementation task, I can lose sight of the larger goal.
Taking a step back helps me evaluate whether a task is genuinely important, identify what is missing, and decide what the project needs next.

---

## Current state

Every project starts with an initial note, usually titled with the current date followed by a description of the final goal.
For example:

```text
Jan. 1. 2026 - Anomaly detection in wind turbine operational data with LSTM models.
```

In this note, I explain in detail what I am trying to achieve and outline the expected milestones, such as data cleaning, model development, training, and evaluation.
When I feel that there is no obvious next step, I create a new note and start writing a section titled "**Current state**."

This section is a self-reasoning session in which I try to explain to myself what I have done up to that point.

I tend to write this text in a way that resembles my own thought process, as if I were talking and trying to explain the project to myself.

---

## Questioning my decisions

Naturally, as in any conversation, many questions arise:

- Why did I choose this method rather than another?
- What evidence supports this assumption?
- What problem does this feature actually solve?
- Is it necessary to investigate this property of the data, or is it just interesting?

This back-and-forth process of describing the project’s current state, asking myself questions, and answering them serves as the core diagnostic mechanism.
The questions that arise from this self-reasoning process test whether every part of the project has a sound reason for existing. They expose implicit reasoning and make it deliberately explicit.

For example:

```text
Why did I select this particular baseline for comparison with my method?
```

A strong answer might sound like this:

```text
I selected this baseline because it is commonly used for this problem, it was tested enough times, and across a wide range of metrics so it will give me a meaningful comparison for the proposed method.
```

A weak answer might be:

```text
I used it because it was tested on only one metric, and my method happens to outperform it on that metric.
```

A question answered with an unclear explanation usually points to unclear or faulty reasoning.
If I fail to state what I did, why I did it, or how a certain decision helps the overall objective, then I have potentially found an area that needs investigation or revision.

This process creates a traceable narrative of the project, where the questions I ask myself test every connection in my chain of thought.

---

## Next steps

After pointing out at the project’s possible weak points, I focus on a section in the same note that I call "**Next steps**", where the main goal is to decide what direction should the project take in the near future.

This stage is similar to the one I just described, but instead of explaining what was already done, the goal is to critically examine several plausible directions before committing.
I start by generating a list of plausible future directions for the project, where my goal is to invalidate as many potential next steps as possible.
For each proposed future step I search for reasons it might be wrong, premature, or unnecessary.
This way I steer myself away from doing something that I find more interesting at the moment, reducing uncertainty around the selection of high-impact tasks.

Over time I noticed that this process became partially internalized and streamlined, where I only need a few sentences to reject a bad idea instead of writing a whole paragraph where I explain to myself why I consider it bad.


---

## Conclusion

This process reminds me of software version control with Git, where the core principles are loosely borrowed and applied to the reasoning process.

A dated note is a commit, with the commit message being the meaningful title.
A branch is an explicitly tracked alternative research direction, where merging it means integrating its useful findings into the main line of thought.

By repeatedly recording my reasoning, goals, decisions and doubts, I not only build a searchable history of how my project and thinking developed over time, but I also improve my intuition and judgement in similar situations.
