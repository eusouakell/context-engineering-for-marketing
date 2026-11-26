# Experiment: cereja-ingest-validation-v01

Status: proposed.

## Origin

Proposed after a real restructuring event [E]: on 2026-11-26, a single-brand operation consolidated its durable brand and product decisions into one archive document and deleted three over-engineered private repositories (knowledge system, editorial engine, site). The brand context is being rebuilt on the seed pattern.

Hypotheses [H]: at the single-brand stage, the maintenance cost of the full architecture exceeded its verification value; the seed pattern should cost less to keep current. This restructuring is not a benchmark result, and no measured advantage is claimed.

## Question

Can the seed pattern hold one brand's context with less operating effort than the previous multi-repo setup, while lint still catches contradiction and staleness?

## Setup

- Create `cereja-context` from the seed pattern.
- `raw/`: the brand decisions archive, the site PRD and the design-system specification (exported as files).
- Run ingest, then compile `concepts/` (thesis, lexicon, voice, principles, tokens) and build the index and log.

## Conditions

- C1 index-only: answer brand questions using only `index.md`.
- C2 index + concepts: answer the same questions with on-demand concept fetches.
- C3 lint pass: plant two contradictions between a raw source and a compiled concept; lint must flag both.

## Sample questions

- What is the official tagline, and which raw source evidences it?
- Which color tokens are canonical, and which file is their source of truth?
- What is the mascot's role relative to the brand mark?

## Measures

- Retrieval steps per correct answer (C1 vs C2).
- Contradictions caught out of two planted (C3).
- Staleness: edit one raw source; check whether the log and lint surface the affected concept.

## Falsification

The pattern fails at this scale if lint misses a planted contradiction, or if correct answers require dumping full sources instead of index-first retrieval.
