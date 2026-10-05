# Learn SRE inside the situation

Teaching contract clarified by the project owner on 5 October 2026.

## The learner promise

You can begin with an everyday situation and learn the technical ideas as they become useful. You will not be told to finish Linux, networking, programming or mathematics before understanding the problem in front of you. Every technical term may be new. Each episode supplies the background needed to reason about its question.

The audience is anyone learning SRE. Examples must not depend on the project owner's work experience. Use a range of clearly fictional services and properly sourced real cases. Keep personal history and internal employer details outside the curriculum.

This is a design contract for future authoring and revisions. Existing topic pages have not yet been converted to this approach merely because this document exists.

## Two ways to navigate the same knowledge

**The experience path** follows situations: a page waits, a request is repeated, a queue grows, a release goes wrong, a recovery loses data. One situation can draw on several technical topics. The recommended sequence helps the story develop but does not lock later episodes behind completed chapters.

**The reference catalog** organizes the same ideas under Linux, networking, SLOs, observability, databases and the other curriculum topics. It supports lookup, deeper study and coverage tracking. Topic numbers are identifiers, not prerequisites.

Link both directions: from each episode to its contributing topics, and from each topic to episodes that use it. Keep coverage visible so storytelling does not drop difficult material.

## How an episode unfolds

1. Put the learner in a concrete situation with a clear user goal and visible symptom.
2. Ask for an initial guess that requires only the explanation already provided.
3. Reveal a small part of the system. Define new words in ordinary language at the point they appear.
4. Let the learner inspect evidence or change one meaningful variable.
5. Explain the result, including a worked example and the mechanism behind it.
6. Introduce a failure or exception that challenges the first explanation.
7. Compare possible responses, their costs and their limits. Verify the chosen response with evidence.
8. Ask the learner to explain or predict a new situation. Offer feedback that explains the reasoning.
9. Offer deeper branches and a connected next situation without making either a mandatory detour.

This is an authoring rhythm, not a set of headings to repeat mechanically. The learner should experience a connected story. Small sections and pauses remain useful; a single enormous page is not the goal.

## Explain terms where they are used

Use a meaning-first sentence, then introduce the name. Example: “The app sends a message asking another computer to do something. We call that message a request.” Before relying on “server,” explain that it is the program or computer answering requests in this example.

Expanding an abbreviation is not an explanation. “SLO means Service Level Objective” must be followed by what that target says, who agrees to it and how the learner would check it.

For each new term, give its plain meaning, its role in the current situation and a concrete observation. A diagram label, code comment or chart axis can introduce jargon too; review those surfaces as carefully as the prose.

If a definition needs another unfamiliar idea, unpack that idea immediately. Use a short inline explanation or an expandable example. Never make a tooltip, external link or earlier lesson the only place that essential meaning is available. In Markdown, put the essential explanation in the reading flow.

When an episode is entered directly, briefly reintroduce the necessary terms even if the recommended sequence introduced them earlier. A glossary is a reminder and reference, not a repair for unexplained prose.

## Blend formats around one question

Use short text for meaning and qualifications, diagrams for relationships, an interactive model for cause and effect, and animation for sequences. Choose formats because they help answer the current question. A video is not automatically better than a paragraph.

Keep definitions, names, units and numbers consistent across every format. Provide captions and transcripts for videos, text descriptions for diagrams and keyboard/touch alternatives for controls. Respect reduced-motion preferences. A reader without audio must still get the complete explanation.

A simulation must say what it models and what it omits. Teach how the simplified model differs from production behavior before asking the learner to apply it. Provide expected results and cleanup instructions for runnable labs.

## Revisit ideas with increasing depth

Meet waiting time first as “how long this action takes.” Later revisit it as a distribution across users, then as a percentile, a queueing effect, a deadline budget across dependencies and a measurement affected by omitted requests.

Do not front-load all of these definitions. Do not permanently remove the difficult parts either. Track each revisit and the new depth it supplies.

Make advanced material enterable through a local explanation. A consistency lesson, for example, can start with two people seeing different balances and introduce replicas only when it explains that observation.

## Edge cases belong in the experience

Every substantial episode should include at least one change that breaks a tempting assumption. Across the complete topic coverage, include relevant boundary cases, partial failures, missing evidence, concurrency, timing, recovery, scale and human constraints.

For each failure case, explain:
- what the learner observes;
- at least one plausible explanation and a meaningful alternative;
- evidence that distinguishes them;
- an appropriate bounded action and its risks;
- how recovery would be verified;
- what remains uncertain.

Do not label every unusual event an edge case and move on. Show why it matters. Do not promise an exhaustive list of all possible failures; identify known gaps and keep extending coverage.

## Quality checks

Review a lesson in reading order and mark the first use of every technical term. Check that the explanation arrives before the learner must use it to make a decision.

Try entering through a later episode without reading the earlier ones. The essential reasoning must still be possible. Optional deeper branches may offer more detail, but must not contain missing steps required by the main explanation.

Ask a reviewer to identify unsupported jumps, decorative interactions, incorrect analogies, missing assumptions and edge cases that could reverse the conclusion. Keep the repository's fresh independent-review gate for topic changes.

Preserve primary-source research and verify version-sensitive technical claims. Research notes can record current tools, incidents, debates and career signals. Include them in the learner flow only where they illuminate the situation; avoid a mandatory news or hiring digression in every episode.

The aim is a smooth, coherent experience with demonstrable understanding. Do not claim flawless teaching solely because a template or automated check passed.
