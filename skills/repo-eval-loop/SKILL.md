---
name: repo-eval-loop
description: Cross-repo evaluation and planning loop guidance for ROAMS. Use when Codex needs to inspect repo state, active plans, roadmap, memory, and issue context to recommend the next bounded task and stop with a decision-ready summary.
---

# Repo Eval Loop

Evaluate first, then recommend the next bounded task.

## Inputs

- local repository state
- `.agent/PLANS.md`
- `docs/status.md`
- `docs/roadmap.md`
- memory files
- issue tracker context such as GitHub issues
- recent retrospective outputs when available

## Workflow

1. Classify the current repo state.
2. Reconcile roadmap, active plan, memory, and codebase reality.
3. Inspect issue context for work candidates, stale items, blockers, contradictions, and sequencing pressure.
4. Identify unresolved process problems from recent retrospective outputs.
5. Recommend one next bounded task or one narrower rework step.
6. Refresh or propose the active plan.
7. Identify whether any shared-skill or local-skill improvement should be staged.
8. Stop with a decision-ready summary before publish.

## Required Outputs

- repo-state summary
- next recommended task
- rationale for why it is next
- risks or blockers
- plan update or proposed plan delta
- any process-improvement candidate
- explicit stop-before-publish decision
