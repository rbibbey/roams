# Subagent Orchestration Test

Use this exercise to validate bounded parallel delegation rules.

## Goal

Verify that ROAMS can identify when subagent use is appropriate, define a safe delegation contract, and keep parallel outputs from colliding.

## Scenario

Assume the following task:

`Add a new docs page explaining verification strategy while also refining the verification index in the README.`

Assume:

- one worker could update `docs/verification.md`
- another worker could update `examples/verification/README.md`
- the Manager remains responsible for final integration and review

## What The Test Should Check

- whether subagent use is justified
- ownership boundary for each delegated worker
- expected deliverables
- completion criteria
- validation expectations
- handback format
- how final reconciliation happens
- whether the handback is detailed enough for the Manager to decide on escalation without asking the user by default

## Expected Output

The test should return:

- role-mode or subagent decision
- delegation contracts, if subagents are used
- merge or review plan
- reason subagent use is allowed or disallowed
- how child-agent handbacks return to the Manager without user intervention
- required handback fields that let the Manager decide whether to close, rework, or escalate

## Pass Criteria

- subagent use is justified only because the work is bounded and parallelizable
- ownership boundaries do not overlap
- the Manager remains the acceptance owner
- parallel outputs require review before closure
- child agents report back to the delegating agent rather than waiting on direct user feedback
- handbacks include decision-ready detail rather than pushing ambiguity to the user

## Common Failure Signals

- delegating trivial work
- overlapping ownership boundaries
- no handback or merge plan
- treating parallel outputs as automatically compatible
- child threads left awaiting user feedback when the Manager could consume the result
