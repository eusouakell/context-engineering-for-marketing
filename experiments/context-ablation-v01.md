# Marketing Context Benchmark v0.1 — Context Ablation

## Research question

Does routed context produce better marketing knowledge-work output than prompt-only execution and indiscriminate full-context loading?

## Conditions

- **A — Prompt only:** task instruction only.
- **B — Full context dump:** task plus all available documents, including derived/stale examples.
- **C — Routed context:** task plus bundle produced by the context router.
- **D — Routed context + verification:** condition C plus deterministic and semantic verification criteria.

## Primary outcomes

- task success;
- factual / claim grounding;
- brand consistency;
- audience fit;
- evidence precision;
- human revision count.

## Efficiency outcomes

- input tokens;
- selected source count;
- excluded source count;
- latency;
- cost when available.

## Failure outcomes

- unsupported claims;
- stale-context adoption;
- instruction conflict;
- source-authority violation;
- overlong / generic output.

## Experimental discipline

Keep model, model settings, task wording, evidence set and output constraints constant where possible. Run multiple repetitions when the model is stochastic.

Do not claim that routed context wins unless the results support it.

## Pilot task

The first runnable task is an executive article brief about agent governance for a fictional B2B technology consultancy. All context in the executable companion repository is synthetic.
