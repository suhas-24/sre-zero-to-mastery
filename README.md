# Zero-to-Mastery SRE

This repository is a production-style learning program for Site Reliability Engineering (SRE), built topic by topic and published incrementally.

## Current state

- `Topic 0` is complete: the "Complete SRE Universe Map"
- `Topic 1` is complete: "What Is SRE?"
- `Topic 2+` will be added one major topic at a time
- each topic must be researched against current 2024-2026 sources before authoring

## Repository layout

- `docs/roadmap/00-complete-sre-universe-map.md` - primary published roadmap and learner entry point
- `docs/topics/topic-0-complete-sre-universe-map.md` - published Topic 0
- `docs/topics/` - one learner-facing file per major topic
- `docs/research/` - working research notes for each topic
- `docs/sources/` - topic-specific source logs
- `docs/templates/` - reusable authoring templates
- `skills/sre-topic-author/` - reusable Codex skill for future topic generation

## Authoring rules

Every topic must:

1. Start with a "You are here" progress map.
2. Cover exactly one major topic.
3. Perform a live intelligence sweep first.
4. Weave current tools, incidents, debates, and hiring expectations into the lesson.
5. End with:
   - a summary
   - a key terms box
   - one hands-on exercise
   - the next-topic invitation
   - the required emotion-mix sentence

## Review and publish gate

Before any topic is pushed:

1. A live research sweep must be logged.
2. The topic must be checked against the exact curriculum contract.
3. At least one fresh sub-agent review must verify that the topic:
   - teaches only one major topic
   - covers every listed subtopic for that topic
   - defines technical terms before first use
   - includes the required ending structure
   - reflects current sources rather than stale memory
4. Only after the review passes should the topic be committed and pushed.

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

1. research one topic live
2. update the topic source log
3. write exactly one topic file
4. commit the change set
5. push to GitHub

## Source anchors

- Google SRE hub: https://sre.google/
- Google SRE resources: https://sre.google/resources/
- Google SRE books: https://sre.google/books/
- DORA 2024 State of DevOps: https://cloud.google.com/devops/state-of-devops/
- Catchpoint: https://www.catchpoint.com/
- CNCF landscape: https://landscape.cncf.io/
- OpenTelemetry docs: https://opentelemetry.io/docs/
