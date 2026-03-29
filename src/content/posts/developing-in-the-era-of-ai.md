---
pubDate: 2025-03-27
author: Enrique Alejo
title: "Development in the era of AI"
description: "Honest thoughts about new GenAI development tools."
image:
  url: "../../images/blog/ai-dev.webp"
  alt: "Development in the era of AI"
tags: ["GenAI"]
---

After a questionable initial experience with Cursor when it first launched, a colleague recently convinced me to give it another go. In the last months I've dedicated time to develop with [Q Developer](https://aws.amazon.com/q/developer/), [Cursor](https://www.cursor.com/), [Lovable](https://lovable.dev/), [Copilot](https://github.com/features/copilot) and [Claude](https://claude.ai/). Here is my honest experience.

##### The 'Aha' moment

Change is hard, for everyone. Even though I work in big tech and was surrounded by GenAI messaging, I was not really a GenAI power user. I used it on a daily basis, but had never diven deep into its inner workings, the alternative offerings or played around to unleash its full potential.

The turning point came while preparing workshops to teach university classes. I knew a lot about the subject, so I could clearly envision the end goal. Because of this, creating the workshops became a game of prompting. Quickly iterating to find the best path. It was still hard work, but it was so dynamic that I really felt the term [vibe coding](https://en.wikipedia.org/wiki/Vibe_coding).

It was after this moment that I started going down the GenAI rabbit hole.

##### Magic at First Prompt

When I revisited Cursor and tried Lovable for the first time, I was stunned. Seeing a random token generator (a.k.a. an LLM) create **thousands** of lines of working code from a single prompt still impresses me, even after having seen it happen dozens of times.

##### When Magic Hits Limits

Lovable created a responsive React GUI with a modern feel from a single prompt. And from that initial state, I could prompt my way to add new features. But soon, Lovable got stuck. The problem: I am not a frontend developer. So I was stuck too. I ran into the [the 70% problem](https://addyo.substack.com/p/the-70-problem-hard-truths-about). AI coding tools easily generate about 70% of your codebase, but the remaining 30% became extremely frustrating. For the backend, this was fine. I've squashed my fair share of bugs in Python. But dealing with edge cases and errors for a framework of which I had not even read the quick start in the documentation became counterproductive.

##### The Gains

Regardless of my struggle, the end result was always better and faster than anything I could have done alone. Maybe I did not become a coveted 10x developer, but I would estimate that my productivity doubled.
