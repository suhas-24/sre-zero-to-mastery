---
name: sre-topic-author
description: "Research, write, or review scenario-led SRE learning material with just-in-time explanations, connected concepts, edge cases, traceable sources, and independent review."
---

# SRE Topic Author

Use this skill when authoring, updating, or reviewing learner-facing SRE content in this repository.

## Teaching goal

Help any learner understand a real SRE problem, even when every term is new. Follow `docs/LEARNING-DESIGN.md` and `AGENTS.md`; those documents record the clarified project-owner contract and supersede older prerequisite-first or siloed-topic instructions.

Begin with a coherent user or operator situation. Introduce the background as the situation needs it. Connect ideas from multiple catalog topics when the problem requires them. A focused reference page can still explain one subject deeply, but no learner must finish it before entering another page or episode. Map what is taught to the catalog and state what remains for later coverage.

## Workflow

1. Read `AGENTS.md`, `docs/LEARNING-DESIGN.md`, the scenario path, the curriculum map and the authoring checklist.
2. Choose a learner goal or operational question. Map its contributing concepts and coverage limits.
3. Research version-sensitive claims and relevant current practice before drafting. Prefer official specifications, maintainer documentation, primary incident reports and original research. Keep a source log and research notes for substantive lessons.
4. Write in the format that best supports the question. Explain terms before they are needed, including terms in diagrams, code, controls and captions.
5. Include observable evidence, a worked example, a meaningful exception, trade-offs, and a way to check the result. Distinguish fictional scenarios from sourced incidents.
6. Review entry without prerequisites, technical accuracy, first-use explanations, edge cases, source quality, accessibility and consistency across media. Obtain an independent fresh review for learner-facing lesson changes, then address findings.
7. Report what is drafted, reviewed, tested, or still unknown. Do not imply that a mention equals full topic coverage or that a planned lab was run.

A run may update related roadmap, research, source-log and lesson files when needed for one coherent change. Keep changes focused and map cross-topic work explicitly.

## Research guidance

Prioritize authoritative and primary sources. Check current standards, tool behavior and project documentation when these can change. Use incident reports and case studies to make mechanisms concrete. Community discussions, hiring signals, certifications and AI workflow developments are useful when they answer the learner's question; record them as context rather than forcing unrelated news into every lesson. Identify weak or inaccessible signals and do not present them as consensus.

## Writing guidance

- Use plain, direct language, then add precise terminology.
- Explain a term in context: what it means here, why it matters, and what the learner can observe.
- An expanded acronym alone is not a definition.
- Never rely on a glossary, analogy, tooltip, earlier page or external link for a step needed in the current explanation.
- Let prediction, inspection, experiment, explanation and feedback form one connected experience when useful; do not force repetitive headings.
- Include assumptions, boundaries, partial failures, alternative explanations, action risks and recovery checks where they matter.
- Keep analogies subordinate to the real mechanism. Mark simplifications and simulation limits.
- Choose text, diagrams, interactive models or video for a clear learning purpose. Provide equivalent text, captions, keyboard access and reduced-motion support as applicable.
- Do not add formulaic emotional self-description to learner-facing content.

## Independent review gate

Before committing or pushing a learner-facing lesson change, ask at least one fresh independent reviewer to check the change against the contract. For curriculum-policy-only edits, perform an independent consistency review appropriate to the change. Review is not a rubber stamp: resolve material findings or record why a suggestion does not apply.

## File conventions

- Topic pages: `docs/topics/topic-NN-topic-slug.md`
- Research notes: `docs/research/topic-NN-topic-slug-research.md`
- Source logs: `docs/sources/topic-NN-sources.md`
- Learning paths: `docs/roadmap/`
- Authoring checklist: `docs/templates/topic-template.md`

## Quality bar

If a claim may have changed, verify it against a current authoritative source. Distinguish broad agreement from team-specific choices and unsettled debate. Lessons must be enterable on their own and technically precise. When research is incomplete, say what is missing.
