---
description: Run a question against the pluto-mind vault as a knowledge base — search, synthesize, file the answer back as a durable wiki page so explorations compound
argument-hint: [the question, in plain English]
---

Read the full skill instructions at `05 Skills/query.md` and execute the /query workflow against the question: $ARGUMENTS

If no question was provided as an argument, ask pluto: "What's the question?"

Multi-pass retrieval: index lookup → wikilink graph traversal → keyword grep → existing query results. Aim to read 5–15 pages before synthesizing. The answer goes to `00 Notes/saved-chats/query-YYYY-MM-DD-<slug>.md` as a durable page so future queries can build on it.

Honor the immutable-layers convention: do not edit body content of source notes, daily journals, email threads, or voice-sample transcripts. Cite them via wikilinks in the answer.

After filing, append a one-line entry to `log.md`.
