# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Implement Phase 5 bootstrap automation: define a standardized new-project bootstrap workflow, add reusable bootstrap guidance, and verify that a fresh repo can be initialized from this template with minimal manual setup.

### Status

- state: complete
- owner: Manager
- complexity: standard

### Success Criteria

- `README.md` defines a lightweight bootstrap workflow for initializing a new ROAMS-enabled repository.
- bootstrap guidance includes template-copy and setup checklist, memory seeding guidance, and roadmap/status initialization guidance.
- a dedicated bootstrap skill or reusable setup procedure exists.
- the verification suite includes a fresh-repo bootstrap scenario.
- bootstrap guidance keeps setup minimal and preserves clean separation between roadmap, status, and active-plan artifacts.
- verification evidence is recorded.
- review reaches a clear acceptance decision.

### Risks

- bootstrap guidance could become too heavy and over-provision process for new repositories.
- automation guidance must stay useful even when users are bootstrapping manually rather than through a product-specific automation feature.

### Steps

1. Refresh the active plan for the Phase 5 bootstrap task.
2. Extend `README.md` with a standardized bootstrap workflow and optional automation prompt.
3. Add a bootstrap guidance skill or reusable setup procedure.
4. Add a verification scenario for starting a fresh repo from the template.
5. Update roadmap/status state to reflect Phase 5 progress and completion.
6. Run checks on the bootstrap guidance, skill, verification coverage, and resulting repo state.

### Validation

- commands run: `Test-Path skills/bootstrap/SKILL.md`, `Test-Path skills/bootstrap/agents/openai.yaml`, `Test-Path examples/verification/bootstrap-automation-test.md`, `Select-String` checks in `README.md`, `docs/roadmap.md`, and `docs/status.md`, `git diff` on bootstrap files
- tests executed: none
- manual checks: reviewed the new bootstrap workflow, skill, and verification scenario and confirmed they keep setup minimal, preserve separation between roadmap, status, and active-plan artifacts, and provide both a manual checklist and reusable bootstrap prompt
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: bootstrap workflow guidance, reusable bootstrap skill, verification test, validation evidence, acceptance decision
- open questions: none

### Notes

This task should make setup repeatable without creating an overbuilt automation subsystem.
The bootstrap flow should work both as a manual checklist and as a reusable prompt that applies ROAMS to a fresh repository.
Phase 5 result: bootstrap guidance now lives in `README.md`, reusable procedure guidance lives in `skills/bootstrap/SKILL.md`, and fresh-repo validation lives in `examples/verification/bootstrap-automation-test.md`.

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
