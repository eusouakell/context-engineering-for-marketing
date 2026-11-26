# The seed pattern

A minimum sufficient implementation of a context system for one brand or project.

## Shape

- `raw/` — sources (PRDs, decision archives, selected corpus). Immutable once ingested; every file carries provenance (origin, date, author).
- `concepts/` — compiled knowledge: thesis, lexicon, voice, principles, tokens. Versioned, readable by people and agents.
- `index.md` — what exists and where. The only file an agent reads before choosing what to fetch.
- `LOG.md` — decision log. Every change to compiled knowledge records the source it came from.

## Skills

- **ingest**: source → `raw/`. No interpretation, no summarizing into concepts.
- **query**: retrieve the minimum sufficient context for a task, starting from the index.
- **lint**: check compiled concepts against raw sources; flag contradictions and stale claims.

## Rules

1. Source and compiled knowledge are different layers. Nothing enters `concepts/` without a raw source behind it.
2. Progressive disclosure: index first, concepts on demand, raw only when a concept is contested.
3. Verification is part of the pattern, not an add-on: lint runs before compiled knowledge is trusted downstream.
4. Sites, newsletters and channels are validation surfaces for the knowledge, not systems of record.

## Relation to the Marketing Context Stack

The seed pattern is the stack reduced to layers 1-2 (business context, knowledge authority) with a thin runtime-selection practice (index-first retrieval). Governance and evaluation exist only as the log and the lint. Grow toward the full stack only when a concrete failure demands it.
