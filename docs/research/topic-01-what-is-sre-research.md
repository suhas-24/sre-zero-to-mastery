# Topic 01 Research Notes - What Is SRE?

## Purpose

Ground Topic 1 in current SRE history, role-definition debate, current industry reports, and current hiring signals.

## Core source takeaways

- Google still provides the canonical definition of SRE: ask software engineers to design and run an operations function, then use automation to replace manual labor wherever possible.
- Ben Treynor Sloss remains the key origin figure for the discipline and still frames SRE as engineering-led operations, not a renamed admin team.
- DORA's 2024 and 2025 findings reinforce that software delivery, developer experience, AI use, and platform engineering are now tightly linked.
- Catchpoint's SRE Report 2025 shows a stronger shift toward performance-aware reliability, not just uptime-focused reliability.
- Role boundaries remain debated: many companies still label general cloud/platform/ops work as "SRE" even when they do not apply SLOs, error budgets, or the engineering-first model.

## Current signals worth weaving into the lesson

- Catchpoint's 2025 report frames "slow is the new down" and highlights SLO/XLO tracking as a growing priority.
- DORA's 2025 report says AI adoption is near-universal in surveyed teams, but also says platform quality and safety nets matter more than AI hype.
- Martin Fowler and Team Topologies-adjacent material continue to influence platform engineering conversations: platform teams should operate as self-service product teams, not ticket queues.
- Community discussion on Reddit and Hacker News continues to debate whether SRE is a true discipline or just a title applied to DevOps/platform roles.
- Community discussion on AI in SRE is cautiously optimistic: summarization, query generation, and runbook assistance are accepted faster than autonomous remediation.

## Real incident anchors for Topic 1

- Cloudflare's November 18, 2025 outage showed how failures in major internet infrastructure providers can create wide blast radius quickly.
- AWS public post-event summaries remain useful examples of how mature cloud providers communicate, analyze, and learn from reliability failures.

## Hiring signal summary

- Repeated market signals point to Linux, networking, Kubernetes, Terraform, observability, incident response, and automation as the most common SRE-adjacent expectations.
- Platform engineering is gaining salary and organizational momentum, but it does not replace the need for SRE concepts.
- There is still no single universally respected "SRE certification path"; Kubernetes and cloud certifications remain the strongest adjacent signals.
