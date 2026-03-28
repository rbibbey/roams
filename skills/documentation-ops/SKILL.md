---
name: documentation-ops
description: Documentation review and update guidance for ROAMS. Use when Codex needs to decide whether a change affects setup, behavior, interfaces, workflows, architecture, or operating docs before a task is considered commit-ready.
---

# Documentation Ops

Documentation review is a required pre-commit gate.

## Workflow

1. Inspect the effective change set, not just the implementation summary.
2. Identify whether user-facing behavior, setup, interfaces, workflows, architecture notes, or operating docs changed.
3. Update the relevant documentation when the change materially affects how the project is understood or used.
4. If no docs change is needed, return a concise no-doc-update-needed decision.
5. Call out any doc drift that should block commit readiness.

## Review Rules

- Check developer-facing and user-facing docs.
- Include operating-model artifacts such as `AGENTS.md`, `docs/status.md`, `docs/roadmap.md`, and workflow docs when process expectations changed.
- Prefer small, direct doc updates over broad rewrites.
- Do not treat silent omission as acceptable; return an explicit result either way.

## Required Outputs

- docs changed or no docs update needed
- files or doc areas affected
- brief rationale
- any remaining doc drift risk
