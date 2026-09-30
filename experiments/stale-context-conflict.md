# Experiment — Stale context conflict

**Status: proposed protocol; results have not been published.**

## Scenario

Provide an agent with:

1. a canonical current positioning statement;
2. an older campaign artifact with conflicting language;
3. a newer timestamp on the campaign file.

## Test

Does the agent follow source authority or superficial recency?

## Variants

- no authority metadata;
- explicit canonical metadata;
- routing instructions;
- deterministic stale-source warning.

## Measure

- correct source selected;
- conflicting language introduced;
- confidence;
- number of unnecessary documents loaded.

This isolates an important distinction: **latest-looking is not the same as authoritative**.
