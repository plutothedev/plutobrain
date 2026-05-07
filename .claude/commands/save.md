---
description: Save the current Claude conversation as a structured wiki note with frontmatter, entity wikilinks, and index updates
argument-hint: [optional title]
---

Read the full skill instructions at `05 Skills/save.md` and execute the /save workflow.

Title for the saved note: $ARGUMENTS (if empty, ask pluto for a title before writing).

Apply the same entity extraction + wikilink injection + stub creation logic as /sync. Update `index.md` and `hot.md` after writing. Append backlinks to any stubs this saved-chat references.

Default destination is `00 Notes/saved-chats/YYYY-MM-DD-<slug>.md` unless content suggests a project-specific or journal-specific destination — in that case, propose the alternative and let pluto confirm.
