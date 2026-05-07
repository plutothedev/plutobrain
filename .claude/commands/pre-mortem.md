---
description: Run a decision pre-mortem — imagine the decision failed in 6 months, identify causes, warning signs, preventative actions
argument-hint: <decision being pre-mortemed>
---

Read the full skill instructions at `05 Skills/pre-mortem.md` and execute the pre-mortem workflow.

Decision: $ARGUMENTS

If the decision argument is missing or vague, ask pluto to state it as a single sentence first.

Walk through the 5 questions in order, one at a time, waiting for each answer. Then write the structured output to `04 Reviews/pre-mortems/YYYY-MM-DD-<decision-slug>.md` per the skill spec. Have pluto mark the decision-after-pre-mortem checkbox. If "Proceed with modifications," surface those modifications when the corresponding project/commitment is later created.
