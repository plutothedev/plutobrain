---
type: meta
created: {{TODAY}}
status: active
tags: [meta, index, registry]
---

# Index — Canonical Note Registry

> Registry of canonical notes for entities (people, companies, places, concepts) that Claude should treat as the single source of truth. When `/sync` or `/ingest` extracts an entity, it checks here first to avoid creating duplicate stubs.

## How this file is used

**Lookup before stub creation.** Any process that creates entity stubs (`/sync`, `/ingest`, `/autoresearch`) checks this index first:
1. Search for entity name (case-insensitive, partial-match acceptable)
2. If found → use the listed canonical path; do NOT create a duplicate
3. If not found → either create a stub (if entity is significant) or skip

**Maintained by `/refine`.** When you canonicalize a note (mark it as the source-of-truth for an entity), `/refine` adds an entry here. When you merge duplicates, the survivor's entry stays; the deleted note's entry is removed.

**Also lists "in-vault terminology" — internal jargon that should resolve to canonical notes.** E.g. if you call your business "the shop" sometimes and use its formal name other times, link both to one canonical note.

## Format

Each entry: `- [[Canonical Note Name]] — type — aliases / context`

---

## People

(empty — populated as you build out `00 Notes/people/`)

## Companies

(empty — populated as you build out `00 Notes/companies/`)

## Places

(empty — populated as you build out `00 Notes/places/`)

## Concepts

(empty — populated as you build out `00 Notes/concepts/`)

## Projects

(empty — auto-populated by `/new-project`)

## Vehicles / Major Possessions

(empty — populated as you add them)

---

## Aliases / shorthand

*Map your in-vault shorthand to canonical entries. E.g. "the boss" → [[Jane Smith]].*

(empty)
