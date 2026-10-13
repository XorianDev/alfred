---
name: alfred-sdd-plan
description: Create an implementation plan and atomic tasks from an approved specification. Use after requirements are clear and before a multi-file, risky, or multi-step implementation; do not use to bypass an approval gate.
---

Create a plan that makes implementation reviewable and bounded.

1. Read the approved specification, applicable `AGENTS.md` files, relevant
   architecture decisions, and only the source files needed to plan.
2. Check every proposed approach against repository invariants and identify
   paths that require approval.
3. Produce this output:

   ```markdown
   # Implementation plan: <feature>
   ## Approach
   ## Affected areas
   ## Validation strategy
   ## Risks and decisions
   ## Tasks
   1. <atomic task> — inputs, expected result, validator
   ```

4. Order tasks by dependency. Each task must be independently reviewable and
   have a concrete validator.
5. Recommend a skill or specialist subagent only where it materially reduces
   uncertainty or isolates specialized work.

Do not edit code, create dependencies, or treat a plan as approval to execute.
