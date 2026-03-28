# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Implement commit-readiness gates, retrospective and skill-evolution loops, shared-skill guidance, and bounded automation-loop capabilities across the ROAMS template.

### Status

- state: complete
- owner: Manager
- complexity: complex

### Success Criteria

- `AGENTS.md` defines documentation review, memory review, and retrospective review as explicit gates before commit readiness.
- shared-skill versus local-skill boundaries are documented in the core operating model and bootstrap guidance.
- new skills exist for documentation review, retrospective evaluation, skill evolution, repo evaluation loops, and implementation loops.
- the verification suite covers docs-gate, retrospective, skill-evolution, cross-repo evaluation, and bounded implementation-loop scenarios.
- roadmap and status docs reflect the new self-improvement and automation-loop direction.
- verification evidence is recorded.

### Risks

- the framework could over-document automation before real execution tooling exists.
- new gates could become ceremonial if they are not reflected consistently across skills and verification prompts.
- shared-skill and local-skill boundaries could become muddy if bootstrap guidance is not updated with the core contract.

### Steps

1. Update the core operating contract and Manager/memory/bootstrap skills to enforce the new gates and skill-evolution responsibilities.
2. Add new capability skills and reusable prompts for documentation review, retrospective evaluation, skill evolution, repo evaluation, and bounded implementation loops.
3. Update README, roadmap, and status docs to describe the shared-skill model, commit-readiness gates, and automation-loop direction.
4. Expand the verification suite with scenarios that exercise the new gates and self-improvement loops.
5. Validate file presence and key rule markers, then review the diffs.

### Validation

- commands run: `git status --short`, `Get-ChildItem -Recurse -File`, `Get-Content` on core docs and skills, `Select-String` checks for new gate and automation markers in `AGENTS.md`, `README.md`, and `docs/roadmap.md`, `Test-Path` checks for all new skills and verification files, `git diff --stat`, `git diff` on representative files, `git diff --check`, and an inline PowerShell contract-validation script covering required files and key lifecycle markers
- tests executed: `git diff --check`, inline contract-validation script result `CONTRACT_VALIDATION: PASS`
- manual checks: reviewed the updated lifecycle, README guidance, roadmap sequencing, new capability skills, and verification prompts to confirm the new gates and self-improvement loop are reflected consistently; corrected stale verification prompts before the final validation pass
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: updated operating model, new capability skills, expanded verification suite, validation evidence, acceptance decision
- open questions: none

### Notes

This implementation keeps ROAMS capability-first: it adds explicit gates and bounded automation loops without introducing autonomous publishing or a new specialist role prematurely.
The new loop design is documented as Manager-owned guidance rather than executable infrastructure so downstream repos can adopt it incrementally.

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
