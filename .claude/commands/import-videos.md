---
description: Template — import your own YouTube/podcast/blog content into the vault as per-item notes
argument-hint: [optional flags: --force, --dry-run, --limit N]
---

> This is a template slash-command. It points at a script you own (a YouTube importer, a podcast feed importer, etc.). Adapt to whatever import workflow you use.

If you don't have a content importer, delete this file or replace it with one that fits your stack.

A common pattern:

1. You have a script at `~/your-tool/import.py` that pulls items from your channel/feed and writes them as markdown notes to `00 Notes/Videos/` or `00 Notes/podcasts/`.
2. Each note follows the standard wiki format (TLDR, Counter-Arguments, Mentioned in).
3. The slash-command runs the script, reports what got imported, and (optionally) runs `/sync` over the new files to inject wikilinks.

Until you wire your own importer, this command is a no-op. Delete this file or fill it in with your specifics.
