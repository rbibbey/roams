# PLANS.md

Use this file for non-trivial work.

Keep plans short and current. Replace stale detail with the latest verified state.

## Active Task

### Task

Implement Phase 4 subagent orchestration rules: add a delegation contract, parallel ownership rules, handoff and merge expectations, Manager guidance for role-mode versus subagent execution, and a bounded parallel-delegation verification scenario.

### Status

- state: complete
- owner: Manager
- complexity: standard

### Success Criteria

- `AGENTS.md` defines a delegation contract, ownership rules, allowed and disallowed subagent cases, and merge/review expectations.
- Manager guidance distinguishes role-mode execution from true subagent use.
- a dedicated subagent-orchestration guidance module or skill exists.
- the verification suite includes a bounded parallel-delegation scenario.
- subagent guidance keeps Manager as orchestration authority and avoids duplicate/conflicting work.
- verification evidence is recorded.
- review reaches a clear acceptance decision.

### Risks

- subagent rules could become too permissive and encourage over-delegation.
- the delegation contract must stay small enough to use routinely.

### Steps

1. Extend `AGENTS.md` with a delegation contract, ownership rules, allowed/disallowed subagent cases, and merge/review expectations.
2. Update Manager guidance to decide when to stay in role-mode versus when to spawn a subagent.
3. Add a subagent-orchestration guidance skill.
4. Add a verification scenario that exercises bounded parallel delegation.
5. Update roadmap/status state to mark Phase 4 in progress.
6. Run checks on the orchestration rules, skill, and verification coverage, then close the task.

### Validation

- commands run: `Test-Path skills/subagent-ops/SKILL.md`, `Select-String` for delegation and subagent sections in `AGENTS.md`, `Get-Content` review of `examples/verification/subagent-orchestration-test.md`, `git diff` on orchestration files
- tests executed: none
- manual checks: reviewed the bounded parallel-delegation scenario and confirmed the framework yields role-mode versus subagent guidance, non-overlapping ownership boundaries, a concrete handback format, and Manager-owned final reconciliation
- review status: accepted

### Handoffs

- from: Manager
- to: Coder, QA, Reviewer
- deliverable: delegation contract, subagent guidance, orchestration verification test, validation evidence, acceptance decision
- open questions: none

### Notes

This task should enable bounded parallelism without encouraging subagent use for tightly coupled or trivial work.
Subagent test result: delegation is allowed for separated documentation scopes, each worker owns one bounded artifact, and the Manager must review and reconcile the outputs before closure.

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
