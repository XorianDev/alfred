---
name: alfred-context-retrieval
description: Assemble a small, grounded context packet for repository research, planning, or review. Use when the relevant information is distributed across code, documents, decisions, or prior run artifacts; do not use to dump the entire repository into context.
---

Build the smallest context packet that can support the assigned decision.

1. State the exact question the packet must answer.
2. Read applicable `AGENTS.md` files first, then search for primary source
   files, current decisions, tests, and configuration relevant to that question.
3. Prefer current implementation and authoritative project documents. Treat
   old run logs and generated summaries as secondary evidence.
4. Return this format:

   ```markdown
   ## Context packet: <question>
   - Source: <file and relevant location> — <fact or constraint>
   - Source: ...
   ## Gaps / freshness concerns
   ## Recommended next reader or action
   ```

5. Keep excerpts minimal and preserve source locations.

Do not index sensitive material, infer missing facts, or include unrelated
files merely because they are available.
