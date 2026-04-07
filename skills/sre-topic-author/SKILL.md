---
name: sre-topic-author
description: "Generate or review one SRE curriculum topic at a time with live research, strict topic scope, complete subtopic coverage, required closing sections, and a sub-agent review gate before commit or push."
---

# SRE Topic Author

Use this skill when authoring, updating, or reviewing any topic in this repository.

## Goal

Produce exactly one topic per run. Do not merge topics unless the user explicitly asks.

Honor the curriculum contract strictly, not approximately.

## Required Workflow

1. Read the repository roadmap and identify the exact topic number and title.
2. Perform a live research sweep before writing anything.
3. Update or create topic research notes under `docs/research/`.
4. Update or create a topic-specific source log under `docs/sources/`.
5. Write the learner-facing topic page under `docs/topics/`.
6. Keep the teaching aligned with the repository template.
7. Run a fresh sub-agent review before commit or push.
8. Fix any contract violations the review finds.

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
8. tools or startups from the last 6 months that may be changing practice, while being explicit if signal quality is weak

## Writing Rules

- Start with a warm welcome and a clear "You are here" progress marker.
- Define every technical term before first use.
- Cover every listed subtopic for that topic.
- Use plain language first, then technical precision.
- Include real examples where useful.
- Be explicit about opinionated versus widely accepted practices.
- Use analogies, system diagrams in words, and production war stories where they help learning.
- Treat the learner as starting from zero knowledge.
- End with:
  - tight summary
  - key terms to know
  - try this
  - invitation to continue
  - one sentence explaining how the requested emotion mix shaped the teaching

## Exact Contract To Enforce

The topic must follow the repository template and the user contract exactly enough that a reviewer can check:

- one major topic only
- no listed subtopic skipped
- current web research happened first
- community and AI-workflow signals were checked
- claims that may have changed were verified live
- real tools and incidents are woven into the lesson
- the closing sentence for Topic 0 remains:
  - `This is your map. You will never feel lost. Say "next" to begin Topic 1.`

## Required Review Gate

Before any commit or push for a topic:

1. Spawn at least one fresh sub-agent.
2. Ask it to review the topic for compliance with the curriculum contract.
3. Treat its output as independent review, not as a rubber stamp.
4. Fix issues and rerun review if needed.

Use prompts like:

- `Review docs/topics/topic-01-what-is-sre.md against the curriculum contract in skills/sre-topic-author/SKILL.md and list any violations or missing requirements.`

Do not skip this gate just because the topic looks good locally.

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
- When community discussion is noisy or inaccessible, say that and rely on stronger sources instead of pretending confidence.
