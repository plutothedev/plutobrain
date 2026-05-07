---
description: 3-round autonomous web research on a topic with citations and structured output
argument-hint: <topic>
---

Read the full skill instructions at `05 Skills/autoresearch.md` and execute the /autoresearch 3-round loop.

Topic to research: $ARGUMENTS

Round 1: broad WebSearch → fetch top 3–5 authoritative results → build working summary.
Round 2: identify gaps → targeted searches → fetch additional sources → update summary.
Round 3: verify each major claim against ≥2 independent sources, flag disputed claims.

Output: `00 Notes/research/YYYY-MM-DD-<topic-slug>.md` with TL;DR, key concepts, frameworks, claims (high-confidence + disputed), source citations, and open questions.

Update `index.md` and `hot.md`. Create stubs for new significant concepts/entities surfaced.

If `00 Notes/setup/autoresearch-config.md` exists, honor its source preferences and confidence rules.
