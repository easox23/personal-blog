---
pubDate: 2025-07-12
author: Enrique Alejo
title: "Serverless should be your default"
description: "Unless you have a compelling reason not to, serverless should be your default architecture on AWS."
image:
  url: "../../images/blog/serverless.png"
  alt: "Serverless should be your default"
tags: ["Architecture"]
---

One of the first services I used on AWS was Lambda. For me, Lambda seemed intuitive. I had only written a few Python scripts and executed them running `python main.py` beforehand, so uploading a zip and pressing run made sense to me. However, I quickly realised this was a brutal paradigm shift for all the dev and ops teams that had been running systems since before I was born.

Without Lambda, without this serverless paradigm shift, you need a dedicated infrastructure team just to keep the machine moving. These teams focus on patching operating systems, provisioning new VMs for developers, troubleshooting operational issues and monitoring the overall health of all the infrastructure they govern.

Instead, Lambda makes sense because you can forget about this complexity, and only need to think about business logic (i.e. the processes that actually matter to your company).

- **No server maintenance:** AWS handles all the underlying infrastructure.
- **Built-in observability:** Logs and metrics are provided out-of-the-box.
- **Managed operations:** AWS resolves operational issues behind the scenes.
- **Rapid deployment:** Development teams can deploy and tear down functions in seconds.
- **Cost efficiency:** You only pay for the compute time you actually consume, down to the millisecond.

Unless you have a compelling reason (such as hyper-optimization needs, access to GPUs or you have a very constant and sizeable load and Lambda is not cost effective), serverless should be your default target architecture.

*PD: Note that this does not mean automatically going to microservices (I think the Lambdalith is still a valid architecture choice). For projects that will never scale or have just a few developers and strong need to reach the market quickly, microservices probably do not make sense, we will leave the details of this for another post.*
