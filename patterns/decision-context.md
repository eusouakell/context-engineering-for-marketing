# Pattern — Decision context

A decision record answers **why an approved change happened**. It should not replace the current canonical specification.

Minimum fields:

- decision;
- date;
- owner / approver;
- affected domains;
- rationale;
- supersedes / superseded by;
- evidence references.

Runtime rule: load decision history only when the task depends on rationale, trade-offs or change history. Do not inject all historical decisions by default.
