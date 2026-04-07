---
name: sre-topic-author
description: Generate one topic at a time for an SRE zero-to-mastery curriculum by first performing a live research sweep across official docs, incidents, CNCF ecosystem sources, and current community discussion, then writing the topic in a strict teaching format with source logging.
---

# SRE Topic Author

Use this skill when authoring or updating any topic in this repository.

## Goal

Produce exactly one topic per run. Do not merge topics unless the user explicitly asks.

## Required Workflow

1. Read the repository roadmap and identify the exact topic number and title.
2. Perform a live research sweep before writing anything.
3. Update or create topic research notes under `docs/research/`.
4. Update or create a topic-specific source log under `docs/sources/`.
5. Write the learner-facing topic page under `docs/topics/`.
6. Keep the teaching aligned with the repository template.

## Mandatory Live Research Sweep

Prioritize primary sources first:

- official docs
- project maintainers
- vendor postmortems
- CNCF project docs
- published incident reports

Then gather current discussion signals from:

- X / Twitter
- Reddit
- Hacker News
- CNCF blog
- The New Stack
- InfoQ
- Martin Fowler

For each topic, explicitly look for:

1. latest standards and best practices
2. recent incidents or case studies
3. current tools and CNCF projects
4. emerging trends or paradigm shifts
5. hiring expectations, certifications, or role standards
6. AI-agent or LLM-driven changes relevant to that topic
7. orchestration frameworks being used for agentic or automated workflows when relevant

## Writing Rules

- Start with a warm welcome and a clear "You are here" progress marker.
- Define every technical term before first use.
- Cover every listed subtopic for that topic.
- Use plain language first, then technical precision.
- Include real examples where useful.
- Be explicit about opinionated versus widely accepted practices.
- End with:
  - tight summary
  - key terms to know
  - try this
  - invitation to continue
  - one sentence explaining how the requested emotion mix shaped the teaching

## File Conventions

- Topic pages: `docs/topics/topic-NN-topic-slug.md`
- Research notes: `docs/research/topic-NN-topic-slug-research.md`
- Source logs: `docs/sources/topic-NN-sources.md`
- Roadmaps or cross-topic framing pages can live under `docs/roadmap/`
- Use `docs/templates/topic-template.md` as the structural checklist

## Quality Bar

- If a claim may have changed recently, verify it live.
- If a source is weak or indirect, say so.
- Do not present unsettled industry debates as settled facts.
- Keep the topic self-contained so it can be published independently.
