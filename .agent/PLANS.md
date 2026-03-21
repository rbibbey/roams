# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Add `docs/roadmap.md` as the source of truth for post-v1 ROAMS feature work, document the three-document model, and add roadmap-focused verification coverage.

### Status

- state: complete
- owner: Manager
- complexity: standard

### Success Criteria

- `docs/roadmap.md` exists and includes the agreed roadmap structure.
- `docs/roadmap.md` sequences the remaining feature program with acceptance criteria.
- promotion candidates are tracked as capability-first candidates rather than committed roles.
- `README.md` documents the roadmap and the three-document model.
- the verification suite includes a roadmap-specific test.
- verification evidence is recorded.
- review reaches a clear acceptance decision.

### Risks

- roadmap content could drift into active implementation detail rather than long-horizon sequencing.
- the roadmap and status docs must remain clearly separated in responsibility.

### Steps

1. Add `docs/roadmap.md` with the agreed sections, phases, promotion candidates, deferred items, and exit criteria.
2. Update `README.md` to reference the roadmap and explain the roadmap/status/active-plan split.
3. Update `docs/status.md` so the current snapshot reflects the existence of the roadmap and the next active phase.
4. Add a roadmap-focused verification scenario and register it in the verification index.
5. Run checks on document presence, roadmap structure, ordering, and separation of concerns.
6. Close the task with validation and review evidence.

### Validation

- commands run: `Select-String` for fixed sections and Phase 2 in `docs/roadmap.md`, `Select-String` for roadmap references and Document Model in `README.md`, `Test-Path` for `examples/verification/roadmap-governance-test.md`, `git diff` on roadmap-related files
- tests executed: none
- manual checks: reviewed `docs/roadmap.md` for phase ordering, capability-first promotion candidates, and explicit separation from `docs/status.md` and `.agent/PLANS.md`
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: roadmap doc, README/status updates, verification test, validation evidence, acceptance decision
- open questions: none

### Notes

This task establishes roadmap governance without beginning Phase 2 implementation itself.
QA-style structure checks passed and the roadmap-governance review found no material issues.

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
