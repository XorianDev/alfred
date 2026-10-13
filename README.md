# Alfred

Alfred is a project-agnostic development companion with reusable orchestration rules, skills, specialist profiles, and workflow templates. To use this kit in a repository, copy its **contents** into that repository's root. Keep the dot-prefixed directories. The resulting layout is:

```text
repository/
  AGENTS.md
  .agents/skills/alfred-*/SKILL.md
  .codex/agents/alfred*.toml
  .alfred/templates/*.md
```

Start a new Codex session in the receiving repository after copying. `AGENTS.md` provides the orchestration rules, `.agents/skills/` contains five reusable workflows, `.codex/agents/` contains six optional specialist profiles, and `.alfred/templates/` contains the run artifact templates. Codex supports these repository locations for [instructions and skills](https://developers.openai.com/blog/skills-agents-sdk) and [project-scoped custom agents](https://learn.chatgpt.com/docs/agent-configuration/subagents).

For development work without a repository, use the same operating principles and keep any work artifacts in a location chosen for that task. The repository paths above are a convenient way to carry Alfred into a codebase, not a prerequisite for using Alfred.

For a new run, copy the templates into `.alfred/runs/<identifier>/` with these names:

| Template                 | Run file       |
| ------------------------ | -------------- |
| `feature-spec.md`        | `spec.md`      |
| `implementation-plan.md` | `plan.md`      |
| `tasks.md`               | `tasks.md`     |
| `test-gate.md`           | `test-gate.md` |
| `run-summary.md`         | `summary.md`   |

The kit contains no application code, project decisions, prior run logs, credentials, or CI/deployment configuration. Its instructions do not prescribe a stack, architecture, repository layout, or testing tool.

Keep project-specific facts in the receiving project's own instructions and documentation. Alfred reads those when relevant to a task. Create `.alfred/runs/<identifier>/` for multi-step work using the included templates. The skills and templates do not require an `.alfred/profile.json`; add one only if a concrete workflow needs it.

Copying these files does not create a repository, change an existing Alfred installation, or publish anything.
