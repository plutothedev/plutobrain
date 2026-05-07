---
description: Process a single specified source (URL, PDF, file, or pasted text) into a structured source note
argument-hint: <url-or-path>
---

Read the full skill instructions at `05 Skills/ingest.md` and execute the /ingest workflow.

Source to ingest: $ARGUMENTS

If the argument is a URL: WebFetch the page content.
If it's a local file path: Read the file (use `pages` parameter for large PDFs).
If pluto typed `/ingest paste` (or similar), prompt him to paste the content into the chat.

Detect source type (article, paper, docs, tutorial, transcript, news, sales, forum), extract entities, build the structured note at `00 Notes/sources/YYYY-MM-DD-<source-slug>.md`, and update `index.md` + `hot.md`.

Inject wikilinks for entities matching existing canonical notes; create stubs for new significant entities.
