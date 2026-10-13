---
name: alfred-sdd-intake
description: Turn a requested feature or multi-step change into a reviewable specification. Use when requirements are incomplete, risks are unclear, or implementation should not begin before intent is agreed; do not use for a simple factual answer.
---

Create a concise specification before planning or editing.

1. Read applicable `AGENTS.md` files and only the repository context needed to
   understand the request.
2. Separate stated requirements from assumptions. Ask concise questions only
   when an answer materially changes scope, behavior, risk, or acceptance.
3. Write the specification using this format:

   ```markdown
   # <feature or change>
   ## Goal
   ## In scope
   ## Out of scope
   ## Acceptance criteria
   ## Constraints and invariants
   ## Risks and approval gates
   ## Open questions
   ```

4. Make every acceptance criterion observable. Mark unknowns as open rather
   than resolving them by invention.
5. Stop after presenting the specification when approval is required.

Do not choose architecture, write an implementation plan, edit code, or
silently expand the request.
