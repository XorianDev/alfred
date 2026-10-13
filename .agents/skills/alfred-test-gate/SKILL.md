---
name: alfred-test-gate
description: Verify that an approved change meets its specification through meaningful tests and validation evidence. Use before handoff of a feature, bug fix, schema change, or risky refactor; do not use as a substitute for defining acceptance criteria.
---

Run a specification-focused test gate.

1. Read the approved specification, task list, applicable `AGENTS.md`, changed
   files, and existing tests.
2. Map each acceptance criterion to an existing check, a proposed test, a
   manual verification, or an explicit gap.
3. Inspect test assertions for weak oracles that merely repeat current code
   behavior rather than the intended behavior.
4. Run the required repository checks and focused tests that are in scope.
5. Return this format:

   ```markdown
   # Test gate: <feature>
   | Acceptance criterion | Evidence | Result |
   ## Commands and results
   ## Oracle or coverage gaps
   ## Drift decision
   ```

If validation fails, identify whether the code or specification is wrong.
Do not suppress failures, remove tests, or claim a check ran when it did not.
