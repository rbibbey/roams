# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Finalize Phase 2 memory operations by adding a canonical candidate-memory artifact, explicit update triggers and review flow, and a verification scenario that exercises discard, stage, and promote decisions.

### Status

- state: complete
- owner: Manager
- complexity: standard

### Success Criteria

- memory updates are explicitly staged before promotion.
- candidate memory has a canonical home and review workflow.
- `AGENTS.md` defines memory promotion, pruning, stale-memory detection, and bucket-selection rules.
- a dedicated memory-ops guidance module or skill exists.
- the verification suite includes a memory promotion test that exercises discard, stage, and promote decisions.
- long-term memory remains selective and resistant to noise.
- verification evidence is recorded.
- review reaches a clear acceptance decision.

### Risks

- memory rules could become too heavy for routine use.
- staged memory guidance must clarify where temporary notes live without turning memory into a dumping ground.

### Steps

1. Add a canonical `memory/candidates.md` artifact with review and promotion workflow.
2. Extend `AGENTS.md` and `memory-ops` guidance with candidate staging location, update triggers, and review flow.
3. Update the verification scenario so it exercises discard, stage, and promote decisions.
4. Register any memory-documentation updates in the high-level docs and roadmap/status state.
5. Run checks on the candidate-memory artifact, memory rules, and verification coverage.
6. Close the task with validation and review evidence.

### Validation

- commands run: `Test-Path memory/candidates.md`, `Test-Path skills/memory-ops/SKILL.md`, `Select-String` for candidate-memory and update-trigger sections in `AGENTS.md`, `Get-Content` review of `examples/verification/memory-promotion-test.md`, `git diff` on memory-operations files
- tests executed: none
- manual checks: reviewed the memory-promotion scenario against the completed Phase 2 model and confirmed the rules support discard, stage, and promote decisions with explicit bucket guidance and a canonical candidate-memory staging location
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: updated memory rules, memory-ops skill, memory verification test, validation evidence, acceptance decision
- open questions: none

### Notes

This task should complete the operational memory workflow without adding noisy long-term memory entries.
Memory test result: item 1 discard, item 2 promote to `lessons`, item 3 promote to `decisions`, item 4 discard, item 5 stage in `memory/candidates.md` targeting `style` or `lessons` pending more evidence.

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
