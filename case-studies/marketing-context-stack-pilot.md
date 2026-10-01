# Case study — From knowledge repository to runtime context system

## Initial state

The first public version of the Marketing Context System documented bounded contexts, canonical source rules, progressive disclosure, deterministic checks, semantic evals and human gates.

This solved an important problem: **knowledge authority**.

It did not yet implement the second half of Context Engineering: deciding what enters a specific model call at runtime.

## V2 intervention

A minimal context router was added with four responsibilities:

1. filter invalid or superseded context;
2. rank candidates using authority + relevance;
3. enforce a context budget;
4. produce a provenance manifest explaining inclusion and exclusion.

The router does not attempt semantic perfection. Its purpose is to make context selection **inspectable and testable**.

## Why this matters

Without an executable selector, progressive disclosure remains a documentation principle.

With a router, the system can now produce evidence about which sources were selected, which were excluded, why each decision happened, how much context was consumed and whether a derived artifact displaced a canonical source.

That makes it possible to evaluate the thesis instead of only describing it.

## Next validation

Run the same task under prompt-only, full dump, routed context and routed context + verification.

Publish the result even if routed context does not outperform the alternatives.
