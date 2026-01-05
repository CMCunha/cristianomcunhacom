---
layout: post
title: "Stop the Tooling Avalanche: How Tool Chaos Erodes Software Quality"
description: "Uncontrolled tool adoption silently erodes software quality. Learn how a Technology Radar helps teams reduce tool sprawl, improve testing reliability, and scale quality sustainably."
tags: [technology radar, tool adoption, devops, quality engineering, testing]
date:   2026-01-5 10:00:00 +0100
img: /posts/tooling-avalanche/StopTheToolingAvalanche-slide1.png
categories: blog
comments: true
published: true
---

## TL;DR

- Software quality is not achieved by tests alone — it emerges from the entire system
- Uncontrolled tool adoption increases complexity and reduces confidence in results
- Infrastructure, developers, and testers all pay the price in different ways
- Fragile tooling chains make testing signals unreliable
- A Technology Radar creates shared context for intentional tool adoption
- Used correctly, it reduces tool sprawl and helps scale quality sustainably

---

## Why Tool Chaos Is a Software Quality Problem

We live in a fast-paced world where software systems are no longer simple applications. They are **socio-technical systems**, composed of tools, software, infrastructure, and — most importantly — how people interact with them.

In systems like these, quality does not come from a single activity or role.

> **There is more to quality than just tests!  
> Testers are not the gatekeepers anymore, and they have more weapons than just tests.**

Quality in modern systems cannot be reduced to test execution alone.

**Quality cannot be achieved by tests only.**  
It emerges from *all aspects of the system* — tooling choices, infrastructure, integration, standards, and long-term maintainability.

As testers, we often hear phrases like *“tests are failing in this environment, but they pass in another”*.  
Flaky tests are frequently blamed on test code, but more often than not, they are symptoms of a deeper issue: **an unstable and overly complex system**.

Tests do not run in isolation.  
They run *inside* the system.

When the system is fragile, inconsistent, or poorly understood, the testing signal becomes unreliable — regardless of how good the tests themselves are.

And yet, under pressure to deliver faster, comply with regulations, and improve visibility, many organisations fall into the same trap:

> “We need a tool for that.”

This is how the tooling avalanche starts.

---

## When Tool Adoption Goes Wrong, Quality Pays the Price

This talk was intentionally presented at **software testing conferences**, because uncontrolled tool adoption is not just an engineering concern — it is a **quality concern**.

Tools are often introduced with good intentions: to solve a problem, improve visibility, or increase speed. The problem arises when these decisions are made **in isolation**, without shared ownership or long-term thinking.

When that happens, quality doesn’t fail loudly.  
It **slowly erodes**.

![Illustration of uncontrolled tool adoption slowing delivery and causing software quality to decay](/assets/img/posts/tooling-avalanche/STA-2.png)

The problem is rarely a single bad tool.  
The real issue is **too many tools, adopted independently**, each adding complexity to the system.

---

## How Tool Chaos Impacts the Entire Organisation

Uncontrolled tooling does not affect just one team.  
It creates friction everywhere — in different ways, but with the same outcome: **reduced confidence in the system**.
![Overview of how uncontrolled tooling impacts knowledge, integration, maintenance, and standards across teams](/assets/img/posts/tooling-avalanche/STA-3.png)
### Infrastructure and Platform Teams

Infrastructure and platform teams are often expected to *“just make it work”*, as if it were possible to deeply understand every tool adopted across the organisation.

In reality, uncontrolled tool adoption creates an invisible operational burden. Tools appear without documentation, without clear ownership, and without consideration for how they will be installed, upgraded, or supported.

This usually results in:

- Tools they did not choose
- Unknown installation, upgrade, and rollback paths
- Lack of operational and debugging knowledge
- Conflicting infrastructure requirements
- Security patches that cause unexpected downtime
- Incident investigations where identifying the root cause is time-consuming
- Chained workflows breaking when a single tool is impacted

When infrastructure teams lack visibility and ownership, stability suffers.  
And when stability suffers, **quality becomes unpredictable**.



---

### Developers

For developers, tool chaos rarely feels like chaos at first.

It often starts with good intentions: solving a problem quickly, improving productivity, or experimenting with a better approach. The problem appears when these decisions are made **without shared visibility**.

Over time, teams begin solving the same problems repeatedly, each with a different tool. Instead of innovation, the organisation ends up with fragmentation.

This often leads to:

- Multiple tools solving the same problem
- Inconsistent approaches across teams
- Frameworks introduced without long-term support or maintenance plans

Even worse, some tools do not comply with **security, performance, or logging standards**. These gaps usually surface late — during audits, incidents, or production failures — when the cost of fixing them is significantly higher.

At that point, quality is no longer something you *engineer*.  
It becomes something you *react to*.

![Software tooling standards including security, performance, logging, and error handling](/assets/img/posts/tooling-avalanche/STA-4.png)

---

### Testers and Quality Engineers

For testers and quality engineers, uncontrolled tool adoption is especially painful.

Testing rarely depends on a single tool. It depends on **flows** — chains of tools that must work together to produce a reliable signal. When tool adoption is unmanaged, these flows become fragile.

Test execution often depends on:
- Multiple tools integrating correctly
- Data flowing through several systems
- Reports being generated, aggregated, and interpreted reliably

When one tool in the chain fails, the entire testing signal becomes questionable.

Testers are then forced to ask uncomfortable questions:
- Are these failures real?
- Can we trust these results?
- Did the system fail — or did the tooling fail?

At this point, testing no longer increases confidence.  
It increases doubt — and doubt is the enemy of quality.

---

## Tooling Complexity Makes Quality Unscalable

As tooling complexity grows, quality becomes harder to sustain:

- Knowledge becomes scattered
- Maintenance costs increase
- Failure points multiply
- Standards are inconsistently applied
- Confidence in results erodes

The organisation may *look* mature — dashboards, pipelines, tools everywhere — but underneath, **quality is paying the price**.

This is the tooling avalanche.

---

## The Technology Radar: A Quality-Driven Approach to Tool Adoption

At some point, I realised the problem wasn’t tooling itself.

It was **how we were making decisions about tools**.

Security chose their tools.  
Development chose theirs.  
Testing chose theirs.

What was missing was **shared context**.

![Technology Radar showing tools categorized as Assess, Trial, In Use, and Hold](/assets/img/posts/tooling-avalanche/STA-5.png)

The **Technology Radar** provides exactly that.

It is a shared, evolving snapshot of the **tools, frameworks, platforms, and techniques** an organisation is experimenting with, using, or deliberately avoiding. It is not a static document, and it should never become a governance weapon.

Its real purpose is to support **intentional, quality-driven tool adoption**.

The Technology Radar I used (with some adaptations) was originally shared by Zalando on GitHub.

---

## Implementing the Technology Radar Without Bureaucracy

A Technology Radar only works if it stays practical and lightweight.

This is how I’ve seen it succeed in real organisations — and yes, expect friction.

> “This limits innovation.”  
> “Developers are artists; we cannot be constrained.”

These concerns must be addressed early. Introducing a Technology Radar without leadership support is extremely difficult, because it challenges how decisions have been made so far.

We already work under constraints: **security, compliance, performance, and operational stability**.  
The Technology Radar does not create these constraints — it makes them **visible and explicit**.

> *Adoption is encouraged when done with purpose.*

### Start Small and Focused

One of the fastest ways to kill a Technology Radar is to make it too big, too early.

Trying to map the entire organisation at once quickly turns it into an abstract exercise with no ownership. Instead, start where tool sprawl already hurts:

- Testing tools
- CI/CD tooling
- Observability
- Security tooling

A small scope keeps discussions grounded in real problems and real experiences.

---

### Infuse Quality and Standards Early
![Aligning tool adoption with security and quality standards](/assets/img/posts/tooling-avalanche/STA-6.png){: style="float: right; margin-left: 5em; height="20%" width="20%""}
Tool discussions should never be only about features.

Introducing a Technology Radar is often the spark that starts long-overdue conversations about **standards and quality**. Do teams across the company actually know which standards they are expected to comply with when adopting a tool? Is everyone aligned on what *quality* means in practice? And in some cases, does the company even have a shared definition of quality?

These questions are uncomfortable — but necessary.

Once expectations around quality and standards are clarified, they must be embedded directly into the Technology Radar. This ensures that tool adoption is not just fast or convenient, but also **safe, sustainable, and aligned with organisational goals**.

For us, every entry in the Technology Radar had to implicitly answer the following questions:

- Does this comply with our security standards?
- Does it meet performance expectations?
- Is it observable and debuggable?
- Can we safely install, maintain, and upgrade it?

When these questions are asked early, quality stops being reactive and becomes **intentional**.

---

### Find Champions, Not Gatekeepers
![Find your champions](/assets/img/posts/tooling-avalanche/STA-7.png){: style="float: left; margin-right: 5em; height="20%" width="20%""}
A Technology Radar does not need approval committees.

It needs **champions** — people with hands-on experience who are willing to share what worked, what didn’t, and, most importantly, *why*.

In my case, these champions were the architects assigned to groups of teams (teams organised under a specific area of expertise). These architects were usually among the most experienced people in the company. They had a good understanding of the overall architecture while still working closely with the teams, helping them overcome complex technical challenges.

That combination was critical.

They had enough technical depth to assess tools realistically, and enough proximity to the teams to understand real needs and constraints. This made them the ideal bridge between day-to-day engineering work and the broader Technology Radar discussions.

Champions should be able to:
- Understand the challenges and needs of the teams in their area
- Act as the main contact point for the Technology Radar
- Share updates and decisions with teams, keeping them informed and aligned
- Bring feedback, concerns, and new needs from the teams back into the Radar

This two-way flow is essential.

Champions build trust, encourage learning, and keep the Technology Radar grounded in reality — not theory.

---

### Make It Visible and Easy to Access
![Visibility is key for a technology radar](/assets/img/posts/tooling-avalanche/STA-9.png){: style="float: right; margin-left: 5em; height="20%" width="20%""}

A hidden Technology Radar might as well not exist.

One of the biggest strengths of having a Technology Radar is making it easy to:
- Find
- Read
- Discuss

Having a single, well-known place where tooling decisions live is game-changing. In our case, the Technology Radar quickly became part of the onboarding material for new joiners. This gave them immediate visibility into which tools were in use, which ones were approved, and which ones were being evaluated.

For new team members, this removed a lot of uncertainty. Instead of guessing or copying what a nearby team was doing, they had a clear reference point. For the organisation, it created a natural way to spread alignment — even with teams that were initially reluctant to adopt shared tooling practices.

Visibility also means transparency.

The Technology Radar should not only show which tools are approved, but also:
- Which tools were evaluated and discarded — and why
- Which tools are currently under assessment
- Which teams are experimenting with a tool and can be contacted to share experience

This turns the Radar into a conversation tool, not just a status board.

And because the Technology Radar is a living practice, updates must be shared regularly. Highlight changes explicitly:
- “Moved to Trial”
- “Moved to Hold”
- “Promoted to In Use”

When people can see decisions, context, and movement, alignment happens naturally.

Visibility creates alignment — without enforcement.

---

### Treat It as a Living Practice
![Monthly spotlight](/assets/img/posts/tooling-avalanche/STA-8.png){: .img-small style="float: left; margin-right: 5em; height="20%" width="20%""}

A Technology Radar is never “done”.  
Its value depends entirely on the people involved and their willingness to keep it alive.

Teams will continuously demand new tools. Champions will carry information back and forth between teams and the Radar. At the same time, tools evolve, organisations evolve, and company demands change. What was acceptable yesterday may no longer be acceptable tomorrow.

For example, a company that previously did not handle credit card information may suddenly need to do so. Overnight, security, compliance, and tooling requirements shift — and the Technology Radar must reflect that reality.

Because of this, the Radar must evolve as:
- The organisation evolves
- Standards change
- Tools mature or decay

This evolution does not happen automatically.

It requires deliberate time and attention. Schedule regular reviews, remove outdated tools, and adjust categories when reality demands it. In our case, we introduced a mandatory monthly meeting dedicated to reviewing the Technology Radar. We did not wait for these meetings to move tools forward when needed, but having a fixed moment in time ensured the Radar never became neglected — especially in the early stages.

This is how the Technology Radar stays relevant instead of becoming shelfware.

---

## Scaling Quality by Controlling Tooling Complexity

When used correctly, the Technology Radar becomes more than a visualisation.

It becomes a mechanism to:
- Reduce tool sprawl
- Improve cross-team collaboration
- Increase visibility of approved and used tools
- Align tooling with quality goals
- Make testing results more reliable
- Scale quality sustainably

**There is more to quality than just tests.**  

Quality does not emerge from tools alone — and it certainly does not emerge from tests alone.

It emerges from intentional decisions, shared understanding, and systems that people can actually operate, maintain, and trust.

The question is not how many tools your organisation uses.  
The question is whether your teams understand them, trust them, and can evolve them together.

Uncontrolled tool adoption adds complexity faster than teams can absorb it. Over time, confidence erodes, signals become unreliable, and quality becomes harder to scale.

A Technology Radar is not a silver bullet. But when used with purpose, it creates shared context, slows down the tooling avalanche, and gives teams — especially testers — better weapons than tests alone.

If testing results feel unreliable, if environments behave differently, or if tool decisions keep being rediscovered instead of shared, the problem may not be your tests — it may be your tooling strategy.

In the next article, I’ll dive deeper into one of the most visible symptoms of this problem: **flaky tests** — why they are often blamed on test code, and how they are frequently a signal of deeper system and tooling issues.

That is how quality becomes intentional, scalable, and sustainable.

