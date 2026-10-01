# Pattern — Tool-output context

Tool results are runtime context, not permanent truth by default.

Risks include large payloads, duplication, rapid staleness and irrelevant fields.

```text
TOOL RESULT
→ FILTER
→ STRUCTURE
→ RETAIN REQUIRED FIELDS
→ STORE FULL RESULT OUTSIDE WINDOW
→ PASS COMPACT CONTEXT FOR NEXT STEP
```

Keep identifiers or references that allow the agent to recover the full result when needed.
