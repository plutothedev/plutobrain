---
description: Read-only vault health check — orphans, dead wikilinks, unexpanded stubs, duplicate names, missing frontmatter, index drift
argument-hint: [optional folder to scope the scan]
---

Read the full skill instructions at `05 Skills/lint.md` and execute the /lint workflow.

Scan scope: $ARGUMENTS (if empty, scan the entire vault).

Run all 8 health categories: orphans, dead wikilinks, unexpanded stubs, duplicate-name candidates, missing frontmatter, stubs without backlinks, stale time-sensitive claims, index drift.

Write the report to `00 Notes/lint-reports/YYYY-MM-DD-lint.md` with counts and per-issue listings. Don't modify any other files — lint is read-only by default.

After writing the report, offer pluto specific fixes (e.g., "expand or archive these 5 stubs?", "auto-fix index drift?"). Apply fixes only with explicit per-fix confirmation.
