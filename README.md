# AskNebula Claude Workflow — Cook Book

A practical visual guide for the FE team on how to use the two Claude Code orchestrator skills:

- `/refactoring-workflow` — restructuring existing code
- `/new-feature-workflow` — net-new functionality

Both skills auto-adapt to one of three modes (**SMALL / MEDIUM / FULL**) decided by `requirements-agent` after Phase 1, following Anthropic's Router pattern.

## Live

Once GitHub Pages + DNS are configured: **https://asknebula-claude-workflow.com**

GitHub Pages default URL (always works): https://xvivs.github.io/asknebula-claude-workflow/

## Local preview

```bash
open index.html
```

Single self-contained HTML — no build step, no dependencies, no JS framework.

## Source of truth

The skills themselves live in the codebase at:

```
~/asknebula_spa/.claude/skills/
├── refactoring-workflow/SKILL.md
└── new-feature-workflow/SKILL.md
```

Plus supporting agents in `~/asknebula_spa/.claude/agents/`:

- `pre-flight-auditor.md` — Phase 0 (refactor)
- `feature-reuse-auditor.md` — Phase 0 (feature)
- `requirements-agent.md` — Phase 1 (+ Complexity Classification §6)
- `tech-design-agent.md` — Phase 2
- `tasks-agent.md` — Phase 3
- `implementation-agent.md` — Phase 4
- `retrospective-agent.md` — Phase 7

This page documents the *user-facing protocol*. The skills are the executable spec.

## Updating the page

Edit `index.html` directly. It's intentionally a single file — easier to share, easier to diff.

When the underlying skills evolve (v2 after first FULL feature run), update the Cook Book accordingly and push. GitHub Pages auto-deploys from `main`.

## Versioning

The `eyebrow` text in the hero shows current version + last updated date. Bump on substantive changes.

---

*Internal documentation. Generated 2026-05-05 from CHAT-5953 post-mortem + Anthropic engineering best practices.*
