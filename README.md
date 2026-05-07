# 🧠 PlutoBrain

**A personal AI knowledge OS.** Obsidian vault + Claude Code + 14 skills + a self-awareness layer + a bias-fighting divergence pass.

> Build a real second brain on your machine in ~30 minutes. No coding required. Free.

---

## What this is

PlutoBrain is a fork-able template for building your own AI second brain. It's the system Pluto uses every day — sanitized, generalized, and packaged so you can clone it.

What's in the box:

- **Obsidian vault** structured for capture → store → think → act
- **Claude Code** integration that reads and writes to your notes directly
- **14 custom skills**: `/sync`, `/ingest`, `/query`, `/save`, `/refine`, `/lint`, `/canvas`, `/autoresearch`, `/pre-mortem`, `/weekly-update`, `/deep-context-fill`, `/new-project`, `/brain-setup`, `/divergence-check`
- **Two-Claude workflow** — Strategist Claude (terminal) + Editor Claude (in your editor of choice)
- **Self-awareness layer** — `patterns.md` tracks your recurring behavioral patterns and Claude flags them
- **Daily / weekly cadence** — designed to compound for years

## Why it's different

Most AI second brain tutorials show you how to chat with your notes. **This one teaches your AI to chat back at you about your patterns and challenge its own conclusions.**

- **`patterns.md`** — Claude proposes patterns it observes (impulsive project starts, conflict avoidance, scope creep, etc.). You approve. Future sessions surface them by name when triggered.
- **`/divergence-check`** — bias-fighting skill. Steel-mans every concept page with the strongest counter-argument, surfaces tensions between notes, identifies data gaps. Combats the silent confirmation bias that ossifies most personal wikis.
- **TLDR + Counter-Arguments format** — every wiki note opens with a one-sentence TLDR (saves tokens via index-scan) and concept pages must include a `## Counter-Arguments & Data Gaps` section.
- **Token-budget tiers (L0-L3)** — explicit progressive disclosure. Skills don't load full articles until tier 0-2 indicates need. Faster, cheaper sessions.
- **Layered editability** — explicit boundaries between immutable raw sources, synthesized notes, and registry files. Skills enforce these boundaries.
- **`hot.md`** — session cache so Claude orients fast.
- **`index.md`** — canonical-note registry preventing duplicate stubs.
- **`_blocklist.md`** — privacy filter that blocks specific entities from auto-stub creation.
- **`log.md`** — append-only audit trail of every skill run.

## Quick start

1. Clone or download this repo
2. Move the folder to `~/Documents/` (rename if you want)
3. Open it as a vault in Obsidian
4. Install Node.js (nodejs.org → LTS)
5. Install Claude Code: `npm install -g @anthropic-ai/claude-code`
6. Run `claude` in the vault directory
7. Tell Claude: `run the brain-setup skill in 05 Skills`
8. Follow the interview. Done.

**Full step-by-step:** see [SETUP_GUIDE.md](SETUP_GUIDE.md)

## Folder structure

```
PlutoBrain/
├── CLAUDE.md                       Root instructions for Claude
├── GOALS.md                        Your goals at 1/3/10-year horizons
├── patterns.md                     Self-awareness pattern library
├── hot.md                          Session cache
├── index.md                        Canonical note registry
├── _blocklist.md                   Privacy filter for entity stubs
├── log.md                          Append-only audit trail
├── SETUP_GUIDE.md                  Detailed setup walkthrough
├── 00 Notes/                       Entity notes & sources
│   ├── _NOTE_FORMAT.md             Universal note schema
│   ├── people/
│   ├── companies/
│   ├── places/
│   ├── concepts/
│   ├── vehicles/
│   ├── sources/                    Immutable - /ingest output
│   ├── saved-chats/                /save output
│   ├── research/                   /autoresearch output
│   ├── canvases/                   /canvas output
│   └── lint-reports/               /lint output
├── 01 Journals/
│   ├── _daily-template.md
│   └── daily/                      YYYY-MM-DD.md notes
├── 02 Chess Moves (Long-Term Planning)/
│   └── _chess-moves-template.md
├── 03 Projects/
│   └── _PROJECT_TEMPLATE/          Cloned by /new-project
├── 04 Reviews/                     Weekly/monthly/yearly reflections
├── 05 Skills/                      14 custom skills
├── inbox/                          Universal capture zone
├── media/                          Binary assets (images, PDFs, audio)
└── .claude/
    ├── commands/                   Slash command shortcuts
    ├── skills/                     Auto-discovered skills
    └── agents/                     Future use
```

## The 14 skills

| Skill | What it does |
|---|---|
| `/brain-setup` | Interview-driven CLAUDE.md generator. Run this first. |
| `/new-project` | Interview-driven project creation under `03 Projects/`. |
| `/weekly-update` | Refresh context across the brain. Run weekly. |
| `/deep-context-fill` | Gap-targeted CLAUDE.md depth interview. Run after 1 week of use. |
| `/pre-mortem` | Decision pre-mortem before significant commitments. |
| `/sync` | Universal inbox routing. Entity extraction, wikilink injection, stub creation. |
| `/save` | Save current conversation as a structured wiki note. |
| `/ingest` | Process a source (URL, PDF, paste) into a structured source note (with TLDR + Counter-Arguments). |
| `/query` | Run a question against the vault. Answers filed back as notes. |
| `/autoresearch` | 3-round autonomous web research with citations. |
| `/canvas` | Generate Obsidian Canvas (.canvas) visual maps. |
| `/lint` | Vault health check — orphans, dead links, missing TLDRs, missing counter-arguments, contradictions, stale claims. |
| `/refine` | Interactive vault cleanup + enrichment. |
| `/divergence-check` | Bias-check pass — steel-mans concept pages with counter-arguments and data gaps. Run quarterly. |

## Requirements

- **Computer** (Mac, Windows, or Linux)
- **Claude account** with Pro plan ($20/mo) OR Anthropic API credits
- **Obsidian** (free)
- **Node.js** (free — LTS version)
- **~30 minutes** for setup

## Customizing

The template is opinionated but every part is yours to change:

- **Folder structure** — rearrange to fit your work
- **CLAUDE.md** — replace every placeholder with your real life
- **Skills** — write your own in `05 Skills/`. Claude can help.
- **Daily template** — strip what you don't use, add what you do
- **patterns.md** — populate with patterns Claude observes about you
- **GOALS.md** — your goals, your gates, your trajectory

The system rewards customization. Make it yours.

## License

MIT. Use freely, modify, share.

## Contributing

Found a bug, wrote a great new skill, want to suggest a pattern improvement? PRs welcome.

## About

Built by Pluto. The system that runs my life — packaged so you can run yours.

[@plutothedev](https://github.com/plutothedev)
