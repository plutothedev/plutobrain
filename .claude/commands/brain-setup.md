---
description: Interview-driven setup of CLAUDE.md, GOALS.md, and patterns.md — the foundational skill for any new PlutoBrain
argument-hint: [optional: "express" for a 4-round version]
---

Read the full skill instructions at `05 Skills/brain-setup.md` and execute the brain-setup workflow.

If the user passes "express" as $ARGUMENTS, run only Rounds 1, 3, 5, 8, 10 (the express subset) — and mark the resulting CLAUDE.md with a TODO note that a full setup is recommended within a week.

This skill produces THREE files: `CLAUDE.md`, `GOALS.md`, `patterns.md` (and optionally seeds `hot.md`). Generate them in that order, show each to the user for review, only write after explicit approval.

The bar: a stranger reading the resulting CLAUDE.md should be able to describe the user's life situation, predict roughly how they'd react to common decisions, name 2 patterns the user wants flagged, and quote the prime directive. If the output isn't that specific, the interview wasn't deep enough — push for more honesty before writing files.
