# Case study — Knowledge operating system for AI-native marketing

## Problem

A B2B marketing knowledge base contained brand strategy, market research, commercial decisions, proof, vendor material and execution artifacts.

Agents could access the files, but access alone did not establish:

- authority;
- freshness;
- provenance;
- context boundaries;
- publication rules.

## Design

The system separated knowledge into bounded contexts and adopted:

```text
SPEC
→ CONCEPTS
→ DECISIONS + EVIDENCE
→ VIEWS
→ APPLICATIONS
```

It also introduced:

- progressive disclosure;
- deterministic checks;
- semantic evals;
- human gates;
- a `RESEARCH → PLAN → IMPLEMENT → VERIFY` workflow.

## Context Engineering contribution

The core work was not prompt writing. It was deciding:

- where knowledge lives;
- which source wins;
- what an agent loads;
- how much it loads;
- how conflicts are surfaced;
- how claims retain evidence;
- how outputs are checked before publication.

## Public boundary

The architecture is documented here as a reusable pattern. Proprietary company knowledge, client identities and confidential evidence are deliberately excluded.
