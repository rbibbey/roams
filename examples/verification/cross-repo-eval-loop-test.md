# Cross-Repo Eval Loop Test

Use this exercise to validate the ROAMS cross-repo evaluation-and-planning loop.

## Goal

Verify that ROAMS can combine repo state, plans, memory, and issue context into one clear next-task recommendation.

## Scenario

Assume a repository has:

- a partially complete `.agent/PLANS.md`
- `docs/roadmap.md` indicating the next active phase
- `docs/status.md` showing a near-term goal that is now stale
- one GitHub issue describing a bug
- one GitHub issue describing a roadmap-aligned improvement
- a recent retrospective recommending tighter verification coverage

## What The Test Should Check

- whether repo state is reconciled before choosing the next task
- whether issue inputs are ranked against roadmap and active-plan context
- whether retrospective findings influence the recommendation
- whether the loop stops with a decision-ready summary rather than auto-publishing anything

## Expected Output

- repo-state summary
- one next recommended bounded task
- rationale for why it is next
- blockers or risks
- active-plan update or proposed delta
- any process-improvement candidate
- explicit stop-before-publish decision

## Pass Criteria

- multiple inputs are reconciled into one clear recommendation
- the recommendation is bounded and actionable
- the loop remains evaluation-first rather than execution-first

## Common Failure Signals

- choosing work without reconciling repo state
- ignoring issue context or retrospective findings
- blurring evaluation with implementation or publish actions
