# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Implement layered UI Designer extension rules: make ROAMS explicitly defer to project-local art skills when present, add verification coverage, and wire SlappyButt's UI Designer path to its local asset-generation skill.

### Status

- state: complete
- owner: Manager
- complexity: standard

### Success Criteria

- `AGENTS.md` and `skills/ui-designer/SKILL.md` define the layered extension model for project-local design or art skills.
- `UI Designer` explicitly invokes project-local art skills for repo-specific asset work while retaining orchestration ownership.
- the verification suite includes a scenario for repos with a local design skill.
- `README.md` bootstrap guidance notes that project-local skills may extend base roles.
- SlappyButt's local operating rules explicitly route asset-facing UI design tasks through `$slappy-butts-asset-generation`.
- verification evidence is recorded.
- review reaches a clear acceptance decision.

### Risks

- the base `UI Designer` role could become too specific to a single project's art workflow.
- SlappyButt integration must avoid overwriting project-local style rules that are already working.

### Steps

1. Update ROAMS operating rules and the `ui-designer` skill to support project-local art skill extension.
2. Update ROAMS bootstrap and verification docs to cover the layered extension pattern.
3. Update SlappyButt's `AGENTS.md` so UI Designer explicitly invokes `$slappy-butts-asset-generation` for asset-facing tasks.
4. Validate the new role contract and review the diffs in both repositories.

### Validation

- commands run: `Select-String` checks in `AGENTS.md`, `skills/ui-designer/SKILL.md`, `README.md`, and `C:\git\SlappyButt\AGENTS.md`, `Test-Path examples/verification/ui-designer-local-skill-test.md`, `git diff` review in both repositories
- tests executed: none
- manual checks: reviewed the layered role contract and confirmed that ROAMS keeps `UI Designer` generic, the new verification scenario covers local-skill routing, and SlappyButt explicitly routes asset-facing UI design work through `$slappy-butts-asset-generation` while preserving the local skill as the style source of truth
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: updated UI Designer rules, layered extension verification test, SlappyButt integration guidance, validation evidence, acceptance decision
- open questions: none

### Notes

This task should keep the shared UI Designer role generic while letting downstream repos preserve stronger local art workflows.
SlappyButt is the first concrete integration of the layered extension pattern.
Expected task path for SlappyButt art work: `Manager -> UI Designer -> $slappy-butts-asset-generation -> handoff`.

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
