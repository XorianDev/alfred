---
name: alfred-change-review
description: Perform an independent final review of a bounded change for specification adherence, regressions, safety, and missing evidence. Use after implementation and validation, especially before a user handoff; do not use for broad style cleanup.
---

Review the change independently and report material findings only.

1. Read the approved specification, relevant plan/tasks, applicable
   `AGENTS.md` files, affected diff, and validation evidence.
2. Check for specification drift, broken invariants, unsafe side effects,
   regressions, incomplete error handling, and missing test evidence.
3. Classify each supported finding as `critical`, `high`, `medium`, or `low`.
4. Use this format:

   ```markdown
   # Change review: <feature>
   ## Findings
   - [severity] <file:location> — <problem, evidence, safe direction>
   ## Verified evidence
   ## Residual risks
   ```

Do not invent findings, broaden the requested scope, or make code changes.
