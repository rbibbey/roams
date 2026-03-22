---
name: bootstrap
description: Lightweight new-project setup workflow for applying ROAMS to a fresh repository. Use when Codex needs to initialize or refresh a repo from the template without over-provisioning memory, roles, or process.
---

# Bootstrap

Initialize the project with the smallest process that still creates a clean ROAMS starting point.

## Workflow

1. Confirm the repository purpose, constraints, and near-term direction.
2. Update `AGENTS.md` with project-specific operating rules and definitions of done.
3. Seed `memory/style.md` with stable workflow preferences.
4. Keep `memory/decisions.md` and `memory/lessons.md` sparse unless real durable signal already exists.
5. Stage uncertain setup observations in `memory/candidates.md`.
6. Rewrite `docs/status.md` as the current project snapshot.
7. Rewrite `docs/roadmap.md` so it reflects the new project's real sequencing.
8. Reset `.agent/PLANS.md` to the active bootstrap or first implementation task.
9. Verify clean separation between roadmap, status, and active-plan artifacts before closure.

## Bootstrap Rules

- Prefer minimal edits over broad template rewrites.
- Do not add specialist roles, skills, or automation until repeated work justifies them.
- Treat bootstrap as a standard task unless repo complexity clearly demands more.
- Use real project facts for decisions; keep unknowns as open questions or candidate memory.
- Keep the roadmap capability-first and the active plan task-local.

## Required Outputs

Return:

- updated bootstrap plan
- repo-specific document changes
- any initial decisions or candidate memory created
- verification evidence
- remaining assumptions or open questions

## Failure Signals

- status, roadmap, and active plan contain overlapping or duplicated content
- memory is pre-filled with speculative lessons
- extra roles or process are added before they are needed
- bootstrap leaves no clear current task for the Manager
