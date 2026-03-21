# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Create or update `docs/status.md` so it summarizes the repository's current purpose, current stage, near-term goals, and open questions. Update `README.md` to link to the status document from the repository layout.

### Status

- state: complete
- owner: Manager
- complexity: standard

### Success Criteria

- `docs/status.md` exists.
- `docs/status.md` includes sections for purpose, current stage, near-term goals, and open questions.
- `README.md` links to `docs/status.md` from the repository layout section.
- verification evidence is recorded.
- review reaches a clear acceptance decision.

### Risks

- `docs/status.md` already exists from a prior role test and must be updated rather than recreated.
- README changes should remain minimal and avoid duplicating the status content inline.

### Steps

1. Gather current repository context from `README.md` and `docs/status.md`.
2. Update `docs/status.md` to match the requested section set.
3. Add the `docs/status.md` link to the README repository layout.
4. Run QA checks on file existence, section coverage, and link presence.
5. Run Reviewer acceptance checks and close the task.

### Validation

- commands run: `Test-Path docs/status.md`, `Select-String` for required headings in `docs/status.md`, `Select-String` for the `docs/status.md` link in `README.md`, `git diff` on the task files
- tests executed: none
- manual checks: reviewed updated `docs/status.md` content for requested coverage and confirmed the README layout entry
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: updated status doc, README link, validation evidence, acceptance decision
- open questions: none

### Notes

This task reuses an existing `docs/status.md` created during an earlier role test.
QA passed and Reviewer accepted the changes without material findings.

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
