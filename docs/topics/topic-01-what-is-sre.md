# Topic 1 - What Is SRE?

Welcome. This is the first real teaching stop in the SRE journey.

We are going to build one clean mental model: what **Site Reliability Engineering**, or **SRE**, actually is, why Google created it, how it differs from nearby roles, what SREs do in real companies, and why the role still matters so much in 2025 and 2026.

## You are here in the SRE journey

- Completed: `Topic 0 - Complete SRE Universe Map`
- Current stop: `Topic 1 - What Is SRE?`
- Current layer: `Layer 1 - Foundations`
- Next stop: `Topic 2 - Linux Fundamentals for SRE`

This lesson teaches only one major topic: what SRE is.

## The live picture before we begin

The original Google definition of SRE still anchors the field, but the surrounding industry has shifted in important ways.

The strongest 2024-2026 signals from Google, Catchpoint, CNCF, and current community discussion are:

- reliability is increasingly judged by user experience, not just raw uptime
- platform engineering is becoming a formal discipline, not just an informal team label
- AI is helping with incident summaries, runbook drafting, and telemetry triage, but it is not replacing core SRE judgment
- companies still blur the boundaries between SRE, DevOps, platform engineering, and operations, so titles are noisy even when the underlying work is real

That means we need two levels of truth at once:

- the canonical definition of SRE
- the modern reality of how companies actually use the label

## Start with the simplest definition

**Site Reliability Engineering (SRE)** is the practice of using **software engineering** to make production systems more reliable, scalable, and efficient.

Let us define that carefully.

- **Software engineering** means solving problems with code, automation, system design, testing, and repeatable technical mechanisms instead of repeated human effort.
- **Reliable** means the system keeps doing what users need it to do.
- **Scalable** means the system can handle growth in users, traffic, and data without collapsing.
- **Efficient** means the system stays healthy without wasting people, time, or infrastructure.

Here is the beginner version:

SRE is what happens when running systems stops being treated as mostly manual support work and starts being treated as an engineering problem.

## The origin story: how Google invented SRE

Google coined the term **Site Reliability Engineering**, and **Ben Treynor Sloss** is widely credited with founding the discipline there. A well-known Google description says SRE is what happens when a software engineer is asked to design an operations function.

Why did Google need that?

Because large internet services outgrew the old model of manual operations.

Imagine a city where traffic lights fail all the time.

- one model hires more people to drive around fixing broken lights by hand
- the SRE model fixes urgent problems, but also writes the control software, adds monitoring, redesigns failure-prone intersections, automates common recovery steps, and prevents the same class of failure from recurring

That was Google's key insight:

internet-scale operations could not be sustained by adding more humans to perform repeated manual actions.

They needed engineers who could:

- automate repetitive operations
- define reliability targets
- improve system design
- work directly with developers
- reduce operational pain at its source

Google's SRE book also makes a core philosophical point that still matters: **reliability is a product feature**. If a product is available only sometimes, or slow enough to feel broken, users do not care that the codebase exists. From their point of view, the product failed.

## SRE vs DevOps vs traditional Ops vs Platform Engineering

This is the part that confuses almost everyone at first.

### Traditional Ops

**Operations**, often shortened to **Ops**, is the work of running systems in production.

Historically, traditional ops teams often handled:

- server provisioning
- deployments
- monitoring
- backups
- incident response
- access requests
- production ticket queues

Traditional operations is not "bad." Many great engineers built serious systems this way.

The main weakness of the older ops model was structural:

- too much manual work
- too much separation from developers
- too much knowledge trapped in people instead of systems

In the old anti-pattern, developers shipped code and operations inherited the consequences.

### DevOps

**DevOps** is best understood as a philosophy and operating culture, not a single strict role.

Its core idea is that development and operations should collaborate across the whole lifecycle of software instead of working as isolated camps.

DevOps emphasizes:

- shared ownership
- automation
- fast feedback
- continuous improvement
- smaller and safer changes
- less blame and fewer silos

Google's SRE Workbook uses a famous phrase: `class SRE implements interface DevOps`.

In plain language, that means:

- DevOps is the broad philosophy
- SRE is one concrete way to implement that philosophy

So SRE is not the opposite of DevOps. It is a more specific, more opinionated execution model inside the same general world.

### SRE

SRE is more specific than DevOps because it comes with stronger operating rules.

For example, SRE gives you concrete mechanisms such as:

- **Service Level Objectives (SLOs)**, which are explicit targets for service reliability or performance
- **error budgets**, which are limits on acceptable unreliability
- toil caps
- blameless postmortems
- engineering time protection

DevOps says, "development and operations should collaborate and automate."

SRE says, "yes, and here is how we decide how reliable a service must be, when we slow down releases, how much reactive work is too much, and what must be engineered instead of repeated manually."

### Platform Engineering

**Platform engineering** is the discipline of building internal products and self-service systems that help developers build, ship, and operate software safely.

A platform team often builds:

- reusable infrastructure modules
- internal developer portals
- standard deployment paths
- default telemetry and logging
- built-in security guardrails
- paved or golden paths

A **golden path** or **paved road** is a supported default way to build and operate software that makes the safe and standard approach easier than the custom one.

The cleanest beginner distinction is:

- SRE asks, "How do we keep production reliable?"
- platform engineering asks, "How do we make reliable delivery easier by default for many teams?"

In real organizations, these roles overlap a lot.

This is one of the biggest current industry debates. Some companies move classic SRE responsibilities into platform teams. Others keep SRE separate. Others blend both. There is no single universal org chart, but the concepts are still different enough to be useful.

## The SRE mindset: "hope is not a strategy"

One of the clearest SRE attitudes is that **hope is not a strategy**.

That means you do not trust production to luck, memory, or good intentions.

Weak production thinking sounds like this:

- "hopefully the deploy is fine"
- "hopefully somebody notices if latency spikes"
- "hopefully the runbook still works"

SRE thinking sounds like this:

- what is the failure mode?
- how will we detect it?
- what is the rollback path?
- what is still manual, and why?
- what happens under heavy load?
- what do users experience if a dependency fails?

This is the heart of SRE:

software engineering applied to operations.

An SRE does not stop at "the system works right now." An SRE asks:

- how it fails
- how often it fails
- how painful the failure is for users
- how quickly the team can detect it
- whether the design encourages the same failure to happen again

## What SREs actually do day to day

Many beginners imagine SRE as only on-call firefighting. That is incomplete.

A real SRE week usually mixes four categories of work.

### 1. On-call work

**On-call** means being the person or team responsible for responding when production issues need urgent human attention.

That can include:

- investigating alerts
- mitigating incidents
- escalating to experts
- communicating status
- documenting what happened

### 2. Toil reduction

**Toil** is manual, repetitive, automatable work that keeps recurring and creates little enduring value.

Examples:

- restarting the same failed job every day
- manually applying the same cloud change again and again
- clearing the same class of low-value operational tickets repeatedly

SRE teams are supposed to reduce toil, not normalize it.

### 3. Reliability work

This is the deeper engineering layer:

- improving alert quality
- designing safer deployments
- removing single points of failure
- improving backup and restore paths
- strengthening dependency behavior
- improving capacity and resilience

### 4. Project work

SREs also do planned engineering projects, such as:

- writing internal automation
- building tooling
- improving deployment systems
- adding instrumentation
- strengthening shared reliability platforms

So the real job is not "watch dashboards and wait for disaster."

The real job is:

run production, learn from pain, and engineer the pain out of the system over time.

## The 50% rule: why SREs must spend at least half their time on engineering

One of the most important SRE ideas is the **50% rule**.

The rule says an SRE team should spend no more than about half of its time on operational toil or reactive work. At least half should remain available for engineering.

Why is that so important?

Because a team that spends all its time reacting never gets time to remove the reasons it keeps reacting.

That creates a trap:

1. incidents happen
2. manual work grows
3. engineering time disappears
4. automation never gets built
5. the same pain keeps returning

That is a form of **operational debt**, meaning future pain created by not fixing recurring operational problems properly.

Google's toil chapter treats this as a real cultural guardrail, not a vague aspiration. If a team called SRE spends nearly all its time responding manually, it may still be doing valuable work, but it is not yet living the full SRE model.

## SRE team structures: embedded vs centralized vs consulting vs enabling

There is no single universally correct SRE org structure.

### Embedded SRE

An **embedded** SRE team works closely with a specific service or product team.

Benefits:

- deep system context
- strong developer partnership
- faster incident understanding

Risks:

- duplicated work
- weak consistency across the company

### Centralized SRE

A **centralized** SRE organization supports many services from a shared group.

Benefits:

- strong standards
- reusable tools
- concentrated expertise

Risks:

- distance from product context
- more ticket-driven relationships if handled badly

### Consulting SRE

A **consulting** SRE model advises teams, reviews designs, and helps them adopt reliability practices without fully owning their daily operations.

Benefits:

- scales scarce expertise
- spreads good practices widely

Risks:

- recommendations may be ignored
- ownership can become blurry

### Enabling SRE

An **enabling** SRE model focuses on helping product teams become more self-sufficient.

This often overlaps with platform engineering.

Benefits:

- improves long-term scale
- reduces dependency on a small SRE team
- encourages broader operational maturity

Risks:

- teams may be given responsibility before they are ready

Google's workbook discusses this problem directly: once you have many product teams and many reliability stakeholders, structure becomes an intentional design choice rather than an accident.

## The SRE book stack

If you want the essential reading stack, it is this:

### 1. Google SRE Book

Use it for:

- the philosophy of SRE
- reliability thinking
- toil
- incident learning
- production design at scale
- Service Level Objectives (SLOs)
- error budgets

### 2. Google SRE Workbook

Use it for:

- how SRE relates to DevOps
- how to apply SRE outside Google
- engagement and operating models
- practical implementation choices

### 3. Implementing SRE

Use it for:

- introducing SRE in real organizations
- team design
- adoption strategy
- role boundaries and ownership

If the SRE Book teaches the worldview, the Workbook teaches adaptation, and Implementing SRE teaches organizational execution.

## Latest industry reports and what they tell us

This is where Topic 1 becomes modern instead of only historical.

### Catchpoint SRE Report 2025

Catchpoint's 2025 report is valuable because it shows current practitioner concerns.

Two notable signals stand out:

- respondents treat poor performance as nearly as serious as downtime
- reported toil increased again instead of disappearing under AI hype

That second point is especially important. It means the industry is still struggling with the basic SRE problem: repeated operational pain does not vanish just because smarter tooling exists.

### DORA and State of DevOps

The **DORA** research program studies which practices correlate with strong software delivery and operational performance.

Recent Google Cloud DORA material continues to highlight:

- platform engineering as a meaningful organizational force
- the importance of strong software delivery systems
- AI as a workflow change, not a replacement for sound engineering

This matters because SRE is not just about uptime. It sits inside the broader system of how software gets built, tested, shipped, and supported.

### CNCF and current cloud-native signals

The **Cloud Native Computing Foundation (CNCF)** is a major industry body in cloud-native software.

Its survey and certification activity matters here for two reasons:

- cloud-native infrastructure remains the normal environment for modern reliability work
- platform engineering is becoming formalized enough that CNCF now offers dedicated certification around it

That is a strong career signal. In 2025 and 2026, many employers expect SREs to understand not just incidents and monitoring, but also Kubernetes, infrastructure as code, cloud delivery, and platform thinking.

## What recent incidents teach us about why SRE exists

If SRE still sounds abstract, recent outages make it concrete.

Cloudflare's official write-up of its November 18, 2025 outage is a strong modern case study. The beginner lesson is not the deep root-cause detail. The beginner lesson is this:

when a major infrastructure provider fails, the blast radius can spread very quickly across many customers and many dependent services.

That is why SRE exists.

Not to create perfect systems. That is impossible.

But to make systems:

- better designed
- better measured
- safer to change
- faster to recover
- less dependent on luck

AWS continuing to publish public post-event summaries matters for the same reason. Mature reliability cultures accept that failures happen and focus on learning, hardening, and recovery.

## What SRE is not

The label is used loosely in the market, so this matters.

SRE is not automatically:

- any job that touches Kubernetes
- any operations role with Python
- any on-call engineer
- any DevOps title
- any platform team

A team can be called SRE and still not really practice SRE.

Warning signs include:

- endless manual toil
- no explicit reliability targets
- no protected engineering time
- no serious automation effort
- weak partnership with developers
- no measurement discipline

Titles are noisy. Practices matter more.

## Where AI agents fit into Topic 1 right now

Because this curriculum is current, we should say this directly.

AI is already changing SRE workflows.

The most credible practical uses right now are:

- incident summarization
- draft runbook generation
- telemetry query assistance
- dependency surfacing during investigation

Current CNCF writing in 2025 frames this as increasing SRE impact, not simply reducing headcount. That is the most defensible way to understand the trend today.

So if you ask, "Will AI replace SRE?"

The honest answer is:

- it can automate some repetitive analysis
- it can speed up investigation
- it can lower the effort required for some operational tasks
- but it does not replace judgment, system design, accountability, or tradeoff thinking

AI is changing the tools around SRE faster than it is changing the essence of SRE.

## A system diagram in words

Picture a modern production path like this:

`user -> CDN -> load balancer -> API service -> cache -> database -> queue -> worker -> third-party API`

Now picture four groups looking at the same path:

- traditional ops asks, "Which part is down?"
- DevOps asks, "How do we improve delivery and collaboration across the whole path?"
- SRE asks, "What reliability target should this path meet, how do we measure it, what failure modes threaten it, and what engineering removes repeated pain?"
- platform engineering asks, "How do we make the safe way to build and operate this path the default experience for every team?"

That is one of the cleanest ways to see the difference.

## The honest caveat

You will hear people say:

- "SRE is just DevOps"
- "DevOps is dead"
- "platform engineering replaced both"

Those statements are usually too absolute.

The honest answer is:

- there is real overlap
- there is title inflation
- there is vendor marketing
- there are still useful conceptual differences

If you remember one thing, remember this:

SRE is not defined by specific tools.

SRE is defined by an engineering approach to reliability.

## Tight summary

SRE began at Google as a way to run production with software engineering instead of scaling manual operational labor forever. It differs from traditional operations by insisting on engineering over repeated manual work, differs from DevOps by being more concrete and opinionated, and differs from platform engineering by focusing more directly on production reliability instead of internal platform products. Real SRE work combines on-call response, toil reduction, reliability engineering, and project work, with the 50% rule protecting time for actual engineering. Current 2025-2026 signals show that SRE remains highly relevant, increasingly overlaps with platform engineering, and is being augmented, not replaced, by AI tooling.

## Key terms to know

- **Site Reliability Engineering (SRE)**: using software engineering to make production systems reliable, scalable, and efficient
- **software engineering**: solving problems with code, automation, system design, and repeatable technical mechanisms
- **reliability**: the ability of a system to keep serving users correctly and consistently
- **scalability**: the ability of a system to handle growth without breaking down
- **operations (Ops)**: the work of running systems in production
- **DevOps**: a philosophy and operating culture focused on collaboration, automation, and shared ownership across development and operations
- **platform engineering**: building internal platforms and self-service systems that help developers ship and operate software safely
- **on-call**: scheduled responsibility for responding to urgent production issues
- **toil**: repetitive, manual, automatable work with little enduring value
- **Service Level Objective (SLO)**: a target for how reliable or fast a service should be
- **error budget**: the amount of unreliability a service can consume before more stability work should take priority
- **golden path / paved road**: a supported default way to build and operate software safely
- **operational debt**: future pain created by not engineering recurring operational problems away

## Try this

Pick one app you use every day, such as YouTube, WhatsApp, GitHub, or your bank app, and answer these four questions in writing:

1. What would "reliable" mean for that app from a user's point of view?
2. What kinds of failure would feel worst: downtime, slowness, wrong results, or lost data?
3. Which of those failures sound like repeated manual operations problems, and which sound like engineering problems?
4. If you were the first SRE on that app, what repeated pain would you automate first?

If you do this honestly, you have already started thinking like an SRE.

Ready for the next topic? Just say "next" or tell me which topic you want to deep-dive further.

## Sources

- [Google SRE Book Preface](https://sre.google/sre-book/preface/)
- [Google SRE Workbook: How SRE Relates to DevOps](https://sre.google/workbook/how-sre-relates/)
- [Google SRE Workbook: Engagement Model](https://sre.google/workbook/engagement-model/)
- [Google SRE Book: Eliminating Toil](https://sre.google/sre-book/eliminating-toil/)
- [Catchpoint SRE Report 2025](https://www.catchpoint.com/learn/sre-report-2025)
- [Google Cloud DORA Research Hub](https://cloud.google.com/devops/state-of-devops/)
- [CNCF CNPA Certification](https://www.cncf.io/training/certification/cnpa/)
- [CNCF: What LLMs Can Do for SREs in Cloud Native Infrastructure](https://www.cncf.io/blog/2025/04/14/what-llms-can-do-for-sres-in-cloud-native-infrastructure/)
- [Cloudflare Outage on November 18, 2025](https://blog.cloudflare.com/18-november-2025-outage/)

This mix of passionate, enthusiastic, calm, reflective, and laser-focused emotions made me teach this SRE topic like this: by opening with energy and safety, then steadily tightening the concepts until the role boundaries, philosophy, and modern industry shifts became precise enough to support everything that comes next.
