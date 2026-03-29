---
pubDate: 2025-06-13
author: Enrique Alejo
title: "Code is a Liability"
description: "As the GenAI hype train continues its path, a truth of the past is often forgotten. The more code you have, the more things can break."
image:
  url: "../../images/blog/code-liability.png"
  alt: "Code is a Liability"
tags: ["GenAI"]
---



Developers typically enjoy writing and deploying code. Its the part of the job where you can quickly iterate, problem solve and see your vision progress into reality. But every bit of code needs to be followed by proper testing, security analysis and documentation. And every line of code has the potential to introduce new bugs.

A big benefit of AWS is exactly this: you delegate code maintenance to someone else. With Step Functions, you can delegate state tracking, retries and parallel flows. You declare your process, and AWS will maintain and update the actual code that executes your desired processes behind the scenes.

And AWS offers this because no one wants to maintain code (or infrastructure): code is a liability waiting to break. When I worked at Amazon Logistics, I created a serverless (API GW + Lambda + DynamoDB) solution that automated capacity planning for [Amazon Flex](https://flex.amazon.com/) drivers. This solution saved around 8 hours of work per week and reduced costly manual errors. When I left the team, no one wanted to take care of it. They were more comfortable having an employee manually go through the process every week. Without me, the cost of a security breach, a bug or an overloaded system far outweighed the cost of an employee's 8 hours and the ocasional manual errors. And this was a mistake I made: I did not realize that the cost of maintaining the code I wrote outweighed the benefits it brought to the business.

LLMs write thousands of lines of code per minute, without context of the whole solution. They break a key principle in software engineering: Don't Repeat Yourself (DRY), which makes it even easier for inconsistent monitoring or security practices to appear. They solve code errors and reach the solution that you asked for, regardless of the maintainability, security or performance costs. **LLMs spit out code tactically, without thinking of the longterm.**

I love working with LLMs. They boost productivity and help me iterate faster. But the more I use them, the clearer it becomes: the more skilled you are, the more they can help. It's still up to us to ensure the solution we develop fits the bigger picture.

![](/img/image.png)
