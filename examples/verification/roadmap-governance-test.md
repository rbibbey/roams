# Roadmap Governance Test

Use this exercise to validate that ROAMS tracks future work through a dedicated roadmap artifact rather than mixing roadmap, status, and active execution state.

## Goal

Verify that the repository clearly separates:

- current project state
- long-horizon roadmap sequencing
- active task execution planning

## What The Test Should Check

- `docs/roadmap.md` exists
- `docs/roadmap.md` includes the fixed roadmap sections
- the roadmap identifies the current next active phase accurately instead of asserting a stale phase
- `docs/status.md` remains a current-state snapshot rather than a backlog
- `.agent/PLANS.md` remains the active execution document rather than a long-horizon roadmap
- promotion candidates are capability-first and not pre-committed roles
- commit-readiness and automation-loop roadmap additions remain roadmap-level guidance rather than active-task detail

## Expected Output

The test should return:

- pass or fail status
- verified roadmap structure
- verified sequencing
- separation-of-concerns findings
- any overlap or ambiguity between roadmap, status, and plan documents

## Pass Criteria

- the roadmap clearly separates future work from current state
- each planned phase has acceptance criteria and sequencing
- promotion candidates are framed as candidates, not roadmap commitments
- the three-document model is explicit and non-overlapping
- roadmap sequencing reflects the repository's actual current state

## Common Failure Signals

- roadmap content mixed into `docs/status.md`
- active execution detail mixed into `docs/roadmap.md`
- stale phase sequencing left behind after roadmap changes
- future roles committed without promotion criteria
- missing phase ordering or acceptance criteria
