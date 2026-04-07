---
name: sre-curriculum-author
description: Create or update one topic at a time for a zero-to-mastery Site Reliability Engineering curriculum. Use when a user wants the next SRE topic authored with a mandatory live research sweep, current tool and incident context, practical examples, and the exact teaching structure defined by the curriculum.
metadata:
  short-description: Author one SRE topic with live research
---

# SRE Curriculum Author

Use this skill when authoring the SRE curriculum in this repository.

## Scope

Author exactly one major topic per response or per file update.

Do not merge topics unless the user explicitly asks.

## Required workflow

1. Read the roadmap in `docs/roadmap/00-complete-sre-universe-map.md`.
2. Read `docs/templates/topic-template.md`.
3. Perform a live intelligence sweep before drafting.
4. Prefer official and primary sources for technical claims.
5. Weave current incidents, tools, debates, and hiring expectations into the lesson.
6. Save each topic as its own markdown file under `docs/topics/`.

## Research checklist

Always check:

- Google SRE resources
- CNCF materials and relevant project blogs
- official docs for the tooling being discussed
- recent incident or postmortem material for the topic
- current community debate across Reddit, Hacker News, X, InfoQ, The New Stack, and Martin Fowler where relevant and accessible
- current hiring or certification signals if the topic affects career expectations

## Output contract

Every authored topic must include:

- a warm opening
- a "You are here" progress indicator
- one-topic-only coverage
- plain-language explanation first
- defined technical terms before first use
- real examples
- edge cases and gotchas
- source links
- the required five-part ending from the template

## Notes

- Be explicit when a statement is an inference rather than a direct source claim.
- When X search results are noisy or inaccessible, say that clearly and rely on stronger accessible sources instead of pretending certainty.
- Favor practical production reasoning over vendor marketing.

