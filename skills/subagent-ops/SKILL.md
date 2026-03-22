---
name: subagent-ops
description: Subagent delegation and orchestration guidance for ROAMS. Use when Codex needs to decide whether to delegate bounded work to a real subagent, define a safe delegation contract, keep ownership clear, and merge or review parallel outputs without losing Manager control.
---

# Subagent Ops

Use subagents for bounded parallel leverage, not as a default.

## Workflow

1. Decide whether role-mode is sufficient.
2. Confirm that the work is substantial, parallelizable, and independently reviewable.
3. Define a delegation contract with a clear ownership boundary.
4. Ensure no other subagent owns the same unresolved scope.
5. Review or reconcile the returned outputs before acceptance.

## Delegation Contract

Provide:

- goal
- ownership boundary
- expected deliverable
- validation expectations
- handback format

## Allowed Cases

- separated modules
- independent review or validation
- bounded research or diagnosis
- independent design exploration

## Disallowed Cases

- trivial work
- tightly coupled edits
- duplicated exploration
- delegation used to defer a local decision

## Merge Rules

- review outputs before acceptance
- reconcile conflicts explicitly
- stop and redefine ownership if parallel work collides
