---
description: Generate or extend Obsidian Canvas (.canvas) files for visual maps of vault content
argument-hint: [subcommand and args, e.g., "from goldbach" or "new project-overview"]
---

Read the full skill instructions at `05 Skills/canvas.md` and execute the /canvas action.

Subcommand and arguments: $ARGUMENTS

Recognized forms:
- `/canvas` (no args) — open or create the vault map at `00 Notes/canvases/Wiki Map.canvas`
- `/canvas new <name>` — create a new canvas at `00 Notes/canvases/<name>.canvas`
- `/canvas add note <wikilink>` — add a vault note as a card
- `/canvas add text "<content>"` — add a text card
- `/canvas add image <path-or-url>` — add an image node
- `/canvas add pdf <path>` — add a PDF preview node
- `/canvas zone <name>` — add a labeled zone group
- `/canvas connect <node-a> <node-b>` — draw an edge
- `/canvas from <topic>` — auto-build a canvas of all notes related to topic (uses index.md + wikilinks)

Honor the locked color coding (1=red, 2=orange, 3=yellow, 4=green, 5=cyan, 6=purple). Auto-place new nodes in next free 350×200 cell to avoid overlapping existing ones. Validate JSON before writing. Update `index.md` with the canvas entry.
