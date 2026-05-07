---
description: On-demand vault refinement — walk notes interactively to enrich, delete, merge, or recategorize across all stub types and note categories
argument-hint: [optional scope: companies, people, places, concepts, vehicles, sources, email-threads, saved-chats, research, projects, or specific file/folder path]
---

Read the full skill instructions at `05 Skills/refine.md` and execute the /refine workflow.

Scope: $ARGUMENTS

If no scope provided, ask pluto to choose with counts displayed for each scope so he can pick a manageable batch (e.g., "companies (32 notes), people (21), concepts/trading (11), etc.").

Walk each note in scope alphabetically by filename within folders. For each, gather context (incoming wikilinks, references across saved-chats / email-threads / sources / research, frontmatter), propose an action (KEEP / DELETE / ENRICH / MERGE / MOVE / RENAME) with one-line reasoning, and ask pluto to confirm or choose differently.

Save progress to `00 Notes/lint-reports/refine-progress-<YYYY-MM-DD>.json` so the run can be paused (`quit`) and resumed.

Honor permission boundaries: delete only with explicit per-file confirmation, never modify journal/voice-sample/saved-chat bodies (pluto's writings are protected), update wikilinks across the vault when a file is renamed or merged so no dead links result.

On completion, write the action log to `00 Notes/lint-reports/refine-<YYYY-MM-DD>.md` and update `index.md` if structure changed.
