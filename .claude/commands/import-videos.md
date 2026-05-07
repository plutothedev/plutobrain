---
description: Import pluto's YouTube channel videos into the pluto-mind vault as per-video markdown notes
argument-hint: [optional flags: --force to overwrite existing notes, --dry-run to preview, --limit N for newest N only]
---

Run the YouTube channel importer at `C:\Users\pluto\content-automation\tools\import_youtube_channel.py`. The tool is shared with `agents/uploader.py` via `lib/video_note.py`; both use the same OAuth token at `config/youtube-token.json` (refresh token is permanent under Production status).

Invocation (from project root):
```
cd C:\Users\pluto\content-automation
.venv\Scripts\python.exe tools\import_youtube_channel.py $ARGUMENTS
```

Default behavior:
- Fetches the full uploads playlist for channel `UClgz9Mc0jFUWo-8CAzG3Mdw` via YouTube Data API v3.
- Writes one note per video to `00 Notes/videos/<YYYY-MM-DD>-<title-slug>.md`.
- **Idempotent** — skips notes whose filename already exists. Use `--force` to overwrite (e.g. to refresh view counts).
- Auto-matches voice-sample transcripts at `03 Projects/content-workflow/inputs/voice-samples/` to parent videos via overlap-coefficient title similarity.
- Reads manual overrides from `tools/transcript_overrides.json` for cases where titles diverged or one video has multiple transcripts.
- Auto-extracts ICT concept wikilinks from matched transcripts via deterministic basename match against `00 Notes/concepts/`.

Common usage:
- `--force` — refresh all existing notes (pulls latest stats)
- `--dry-run` — preview what would be written without touching disk
- `--limit 5` — only process the 5 newest videos
- `--channel-id UC...` — different channel
- `--out "C:/path/to/videos"` — different output dir

After running, report the summary line (`N written, N skipped, N transcripts attached`) and any unmatched-transcript warnings to pluto. If new videos were added, suggest `/sync` may be useful to enrich the new notes' Concepts referenced sections beyond the deterministic basename match.

Do not run `--force` without explicit pluto consent — it overwrites the existing notes' frontmatter (which may contain manual edits like additional transcript_link entries).

After completion, append a one-line entry to `log.md` at the vault root:
- Format: `## [YYYY-MM-DD HH:MM] import-videos | <summary>`
- Example: `## [2026-04-30 11:17] import-videos | --force | 16 written, 0 skipped, 8 transcripts attached, 0 unmatched`
- Append-only — never edit existing log entries.
