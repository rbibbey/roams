# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Implement Phase 2 memory operations: add staged memory promotion rules, pruning guidance, bucket-selection guidance, a memory-ops capability, and a focused verification scenario.

### Status

- state: complete
- owner: Manager
- complexity: standard

### Success Criteria

- memory updates are explicitly staged before promotion.
- `AGENTS.md` defines memory promotion, pruning, stale-memory detection, and bucket-selection rules.
- a dedicated memory-ops guidance module or skill exists.
- the verification suite includes a memory promotion versus non-promotion test.
- long-term memory remains selective and resistant to noise.
- verification evidence is recorded.
- review reaches a clear acceptance decision.

### Risks

- memory rules could become too heavy for routine use.
- staged memory guidance must clarify where temporary notes live without turning memory into a dumping ground.

### Steps

1. Extend `AGENTS.md` with staged memory operations, promotion checklist, pruning cadence, stale-memory rules, and bucket guidance.
2. Add a memory-ops skill that explains how the Manager evaluates and applies memory changes.
3. Add a verification scenario that tests promote versus do-not-promote decisions.
4. Register the new memory test in the verification index and update high-level docs if needed.
5. Run checks on the new memory rules, skill, and verification coverage.
6. Close the task with validation and review evidence.

### Validation

- commands run: `Test-Path skills/memory-ops/SKILL.md`, `Select-String` for three-state memory sections in `AGENTS.md`, `Get-Content` review of `examples/verification/memory-promotion-test.md`, `git diff` on memory-operations files
- tests executed: none
- manual checks: reviewed the memory-promotion scenario against the new three-state model and confirmed the rules support discard, stage, and promote decisions with explicit bucket guidance
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: updated memory rules, memory-ops skill, memory verification test, validation evidence, acceptance decision
- open questions: none

### Notes

This task implements the first decision-making layer of Phase 2 rather than changing the existing memory entries themselves.
The memory-promotion verification passed after clarifying that the scenario is testing promotion logic rather than duplicate detection.

## Plan Template

### Task

Short description of the goal.

### Status

- state: planned | in_progress | blocked | validating | complete
- owner: Manager
- complexity: trivial | standard | complex

### Success Criteria

- criterion 1
- criterion 2

### Risks

- risk 1

### Steps

1. Gather the required context.
2. Implement the smallest viable slice.
3. Verify the result.
4. Refine only if needed.

### Validation

- commands run:
- tests executed:
- manual checks:
- review status:

### Handoffs

- from:
- to:
- deliverable:
- open questions:

### Notes

Only record facts that remain useful while the task is active.
