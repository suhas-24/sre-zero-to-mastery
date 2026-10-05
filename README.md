# Zero-to-Mastery SRE

This repository teaches Site Reliability Engineering through concrete situations, visual explanations and experiments. It assumes every technical term may be new and explains supporting ideas when the learner needs them.

Read the [learning design](docs/LEARNING-DESIGN.md) and [scenario learning path](docs/roadmap/01-scenario-learning-path.md). The numbered topics below are a coverage and reference catalog, not prerequisite gates.

## Current state

- `Topic 0` is complete: the "Complete SRE Universe Map"
- `Topic 1` is complete: "What Is SRE?"
- The scenario-driven teaching contract is recorded; existing topic pages still need review and adaptation.
- Further material will be published incrementally, with coverage and verification status visible.
- use authoritative primary sources; verify version-sensitive claims against current sources

## Repository layout

- `docs/LEARNING-DESIGN.md` - current teaching contract
- `docs/roadmap/01-scenario-learning-path.md` - proposed experience path
- `docs/roadmap/00-complete-sre-universe-map.md` - topic coverage and reference map
- `docs/topics/topic-0-complete-sre-universe-map.md` - published Topic 0
- `docs/topics/` - one learner-facing file per major topic
- `docs/research/` - working research notes for each topic
- `docs/sources/` - topic-specific source logs
- `docs/templates/` - reusable authoring templates
- `skills/sre-topic-author/` - reusable Codex skill for future topic generation

## Authoring rules

Follow [AGENTS.md](AGENTS.md) and [the episode checklist](docs/templates/topic-template.md).

- Begin with a concrete situation and a clear user goal.
- Explain every new term at the point it matters, before relying on it.
- Teach Linux, networking, mathematics and other supporting ideas inside the situation; do not require separate prerequisite courses.
- Connect topics where they explain the same problem, and revisit them with increasing depth.
- Blend prose, diagrams, predictions, experiments and feedback around one question.
- Include failure modes, edge cases, trade-offs and recovery evidence.
- Keep technical research current and sources traceable. Record coverage and known gaps.

## Review and publish gate

Before publishing learner-facing topic changes:

1. Log the live research and primary references.
2. Check the current teaching contract and mapped subtopic coverage.
3. Obtain a fresh independent sub-agent review, checking entry without prerequisites, first-use definitions, connected reasoning, technical accuracy, edge cases and media consistency.
4. Fix issues, record what was tested and what remains unverified, then commit and push.

The clarified user contract supersedes older isolated-topic and mandatory-order instructions. The existing authoring skill continues to supply research and review guidance under that contract.

## 33-topic roadmap

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

## Publishing workflow

1. research the episode’s mapped concepts and verify claims that can change
2. update the relevant research notes and source log
3. write the coherent learner experience and update its mapped reference coverage
4. complete independent review and applicable checks
5. commit the change set and push to GitHub

## Source anchors

- Google SRE hub: https://sre.google/
- Google SRE resources: https://sre.google/resources/
- Google SRE books: https://sre.google/books/
- DORA 2024 State of DevOps: https://cloud.google.com/devops/state-of-devops/
- Catchpoint: https://www.catchpoint.com/
- CNCF landscape: https://landscape.cncf.io/
- OpenTelemetry docs: https://opentelemetry.io/docs/
