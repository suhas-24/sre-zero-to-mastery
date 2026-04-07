# Complete SRE Universe Map

You are at the start of the SRE journey.

This map exists so the learner never mistakes the path for a pile of disconnected tools. SRE is not "Prometheus plus Kubernetes plus on-call." It is a layered operating model for building, measuring, defending, and evolving production systems.

## Why this map matters

If you skip the foundations, you can operate dashboards but not systems.

If you skip SLOs and error budgets, you will confuse activity with reliability.

If you skip observability, you will be blind during incidents.

If you skip incident management, every outage becomes improvisation.

If you skip cloud, containers, and Kubernetes, you will be underprepared for most modern production environments.

If you skip performance, capacity, and security, your systems may stay "up" while still failing users.

If you skip soft skills, you may be technically strong but ineffective in real organizations.

## The 11 layers and why each becomes critical

### Layer 1 - Foundations

This layer teaches what SRE is, how Linux and networking actually work, and why automation is mandatory rather than optional.

This becomes critical the first time a process is OOM-killed, a DNS record goes bad, or a script needs to replace a human runbook at 3 a.m.

### Layer 2 - Core SRE Concepts

This layer teaches the mental model of modern reliability: SLOs, error budgets, toil, failure patterns, and distributed systems.

This becomes critical when product teams want more features, leaders want more uptime, and the system cannot satisfy both without explicit tradeoffs.

### Layer 3 - Observability

This layer teaches how to see systems clearly through metrics, logs, traces, profiling, and alerts.

This becomes critical the moment "the site is slow" is the only symptom anyone can provide.

### Layer 4 - Incident Management

This layer teaches how teams respond under stress, recover services, and learn without blame.

This becomes critical when impact is rising faster than understanding.

### Layer 5 - Cloud and Infrastructure

This layer teaches how modern production systems are hosted and controlled: cloud primitives, IaC, containers, and Kubernetes.

This becomes critical as soon as infrastructure itself becomes software.

### Layer 6 - CI/CD and Deployment

This layer teaches safe delivery.

This becomes critical when the fastest way to break production is your release process.

### Layer 7 - Chaos Engineering

This layer teaches how to test resilience before users do it for you.

This becomes critical when systems look healthy only because they have not been stressed realistically.

### Layer 8 - Performance and Capacity

This layer teaches how systems degrade, saturate, and run out of room.

This becomes critical when "up" is still too slow for users.

### Layer 9 - Security in SRE

This layer teaches why secure systems are part of reliable systems.

This becomes critical when identity, secrets, certificates, or supply chain failures become production outages.

### Layer 10 - Modern and Advanced SRE

This layer teaches where the field is moving: platform engineering, AI-assisted operations, FinOps, database reliability, and multi-cloud complexity.

This becomes critical when the problem is no longer "how do we operate one service?" but "how do we enable an entire engineering organization?"

### Layer 11 - Soft Skills and Career

This layer teaches the human side of reliability: communication, trust, influence, interviewing, and career growth.

This becomes critical on every bad day in production and every career transition.

## The full 33-topic roadmap

### Layer 1 - Foundations

1. What Is SRE?
2. Linux Fundamentals for SRE
3. Networking for SRE
4. Programming and Automation for SRE

### Layer 2 - Core SRE Concepts

5. SLIs, SLOs, SLAs, and Error Budgets
6. Toil - The Enemy of SRE
7. Reliability Engineering Patterns
8. Distributed Systems Fundamentals

### Layer 3 - Observability

9. The Three Pillars - Metrics, Logs, Traces
10. Metrics and Monitoring in Depth
11. Logging at Scale
12. Distributed Tracing
13. eBPF - The Future of Observability
14. Alerting Strategy and On-Call

### Layer 4 - Incident Management

15. Incident Response
16. Postmortems - Learning from Failure

### Layer 5 - Cloud and Infrastructure

17. Cloud Platforms for SRE
18. Infrastructure as Code
19. Containers and Docker
20. Kubernetes for SRE

### Layer 6 - CI/CD and Deployment

21. CI/CD Pipelines
22. Deployment Strategies

### Layer 7 - Chaos Engineering

23. Chaos Engineering

### Layer 8 - Performance and Capacity

24. Performance Engineering
25. Capacity Planning

### Layer 9 - Security in SRE

26. Security Reliability (DevSecOps / SecSRE)

### Layer 10 - Modern and Advanced SRE

27. Platform Engineering
28. AIOps and AI-Driven SRE
29. FinOps and Cost Reliability
30. Database Reliability Engineering
31. SRE for Multi-Cloud and Hybrid Environments

### Layer 11 - Soft Skills and Career

32. SRE Soft Skills and Culture
33. SRE Career Path and Certifications

## What breaks in production if you skip the foundations

Skip Topic 1 and you may treat SRE as a toolchain instead of a discipline.

Skip Topic 2 and you may misread host-level failure, resource starvation, or kernel behavior.

Skip Topic 3 and you may blame applications for DNS, TCP, TLS, routing, or load balancing failures.

Skip Topic 4 and you may stay trapped in toil because every fix remains manual.

Skip Topic 5 and you may never know whether the service is truly meeting user expectations.

Skip Topic 8 and you may keep deploying into distributed-system traps you do not recognize.

Skip Topics 9 through 14 and you may not know what is broken, where, or whether someone should be paged.

Skip Topics 15 through 16 and you may recover slowly and learn poorly.

Skip Topics 17 through 20 and you may be unable to reason about the infrastructure most employers now use.

## What matters most for getting hired in 2025-2026

Based on current cloud-native adoption data, recent job descriptions, and community discussion, the highest-value hiring cluster is:

1. Linux and networking fundamentals
2. Kubernetes and containers
3. Cloud platform depth, usually AWS first, then GCP or Azure
4. Infrastructure as Code, especially Terraform
5. Observability, especially Prometheus, Grafana, logs, tracing, and OpenTelemetry
6. Incident response, on-call maturity, and postmortem quality
7. CI/CD and deployment safety
8. SLOs, error budgets, and alerting discipline
9. Automation in Python, Go, and shell
10. Security basics integrated with platform and operations

This is an inference from multiple sources rather than a single canonical ranking. The signal is strong: CNCF reports show Kubernetes is foundational, DORA highlights platform engineering and developer productivity, community job postings repeatedly call for Terraform plus Kubernetes plus observability, and Catchpoint's recent reports keep emphasizing reliability practices over tool sprawl.

## Where AI agents are making the biggest impact right now

The strongest current impact is not full autonomous SRE. It is assisted SRE.

The most credible AI use cases in 2025-2026 are:

1. Alert deduplication and noise reduction
2. Incident timeline summarization
3. Runbook drafting and search
4. Query generation for logs, traces, and metrics
5. Suggested remediation and rollback guidance with human approval
6. Dependency graph analysis and probable root-cause ranking
7. Postmortem draft generation
8. Platform self-service interfaces backed by workflow engines

The community signal is cautious. Recent discussions in SRE and DevOps communities describe AI as a useful junior operator or analyst, but not a safe unsupervised incident commander. That matches current product reality: the best results come from human-in-the-loop systems, not blind autonomy.

## What the industry is debating right now

Several debates are active across Reddit, InfoQ, The New Stack, CNCF content, and conference programming:

- Whether "SRE," "DevOps," and "Platform Engineering" are actually distinct roles or mostly organizational packaging around overlapping work.
- Whether OpenTelemetry should become the default telemetry control plane for most teams.
- Whether eBPF-based observability and continuous profiling should be considered first-class signals, not optional extras.
- Whether AI in operations is genuinely useful or still mostly marketing outside summarization and correlation.
- Whether internal platforms should be tightly opinionated paved roads or flexible frameworks.

## The practical framing for this roadmap

This curriculum is intentionally ordered like a production stack:

1. Learn how machines and networks behave.
2. Learn how reliability is defined and traded.
3. Learn how to observe reality.
4. Learn how to respond when reality goes wrong.
5. Learn how modern infrastructure is built and changed.
6. Learn how to scale safety, performance, security, and organizational leverage.

That order matters. If you reverse it, you get surface familiarity without operational depth.

## Latest signals shaping this roadmap

- Google's SRE resource hub still anchors the field, especially the original SRE book, the Workbook, and secure-and-reliable-systems material.
- DORA's 2024 report keeps platform engineering and developer experience in the center of software delivery performance.
- Catchpoint's 2025 and 2026 SRE reports emphasize that degraded performance is often as damaging as hard downtime and that the field is shifting from managing more tools to building stronger foundations for automation plus human judgment.
- CNCF's 2024 and 2026 survey material shows Kubernetes is now the common substrate of modern infrastructure, including AI workloads.
- OpenTelemetry has solidified as the standard interoperability layer for telemetry, and profiling is being folded into that ecosystem.
- eBPF has moved from specialist tooling into mainstream observability and performance workflows through projects and products around Cilium, Pixie, Parca, Pyroscope, and OTel-related integrations.
- Platform engineering is no longer fringe; it is increasingly how larger organizations scale SRE impact without turning SRE teams into ticket queues.

## Recommended source spine

- Google SRE hub: https://sre.google/
- Google SRE resources: https://sre.google/resources/
- Google SRE book, "Embracing Risk": https://sre.google/sre-book/embracing-risk/
- DORA 2024 State of DevOps: https://cloud.google.com/devops/state-of-devops/
- DORA 2024 announcement summary: https://cloud.google.com/blog/products/devops-sre/announcing-the-2024-dora-report
- Catchpoint SRE Report 2025: https://www.catchpoint.com/learn/sre-report-2025
- Catchpoint SRE Report 2026: https://www.catchpoint.com/learn/sre-report-2026
- CNCF Annual Survey 2024: https://www.cncf.io/reports/cncf-annual-survey-2024/
- CNCF Annual Cloud Native Survey 2026: https://www.cncf.io/reports/the-cncf-annual-cloud-native-survey/
- OpenTelemetry profiling announcement via CNCF: https://www.cncf.io/blog/2024/03/19/opentelemetry-announces-support-for-profiling/
- InfoQ on OpenTelemetry continuous profiling: https://www.infoq.com/news/2024/08/otel-continuousprofiling-elastic/
- The New Stack on Grafana Beyla and OTel: https://thenewstack.io/grafanas-ebpf-beyla-future-hinges-on-opentelemetry/
- CNCF on platform engineering evolution: https://www.cncf.io/blog/2025/07/22/from-yaml-to-intelligence-the-evolution-of-platform-engineering/
- Martin Fowler on platform execution prerequisites: https://martinfowler.com/articles/platform-prerequisites.html

## Final orientation

This roadmap starts by teaching you how systems work, then how reliability is defined, then how to see and improve reality under production pressure.

That is the difference between memorizing tools and becoming an SRE.

This is your map. You will never feel lost. Say "next" to begin Topic 1.

