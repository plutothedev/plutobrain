---
description: Process inbox/ — extract entities, generate wikilinks, create stubs, route content to its proper home
---

Read the full skill instructions at `05 Skills/sync.md` and execute the /sync workflow end-to-end against the current state of `inbox/` in this vault.

Use the standing permissions documented in the skill: create stub notes for new entities, create new files and folders as routing requires, update `index.md` and `hot.md` after routing.

Walk pluto through each unprocessed item interactively (filename, type, extracted entities, proposed destination) and let him approve or redirect.

If pluto types `/sync rebuild-index`, instead do a full regeneration of `index.md` from a fresh vault scan.

Arguments (optional): $ARGUMENTS
