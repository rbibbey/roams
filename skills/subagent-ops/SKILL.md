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
5. Ensure each child agent reports back to the delegating agent instead of waiting on the user.
6. Review or reconcile the returned outputs before acceptance.

## Delegation Contract

Provide:

- goal
- ownership boundary
- expected deliverable
- completion criteria
- validation expectations
- handback format

The handback format should identify the exact artifact returned to the delegating agent.
It should also include the recommended next action for the delegating agent and any escalation reason if user involvement is necessary.

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
- consume child-agent handbacks without exposing user-facing waits when the delegating agent can proceed
- treat handbacks that lack decision-ready detail as incomplete and return them for clarification
