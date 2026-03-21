# Manager Role Test

Use this exercise to validate Manager behavior in isolation.

## Goal

Given a small but non-trivial feature request, produce a clean orchestration package without implementing the feature.

Feature request:

`Add a project status summary section to the README that explains what the repository is for, what stage it is in, and what the next likely milestones are.`

## What The Manager Should Do

- classify the task
- gather the minimum necessary context
- decide whether a plan is needed
- identify which roles are needed
- define bounded ownership for each role
- state risks, assumptions, and success criteria

## Expected Output

The Manager should return:

- task classification
- short plan or explicit decision not to create one
- role assignments
- success criteria
- notable risks or open questions
- closure conditions

## Pass Criteria

- the task is classified reasonably
- the plan is proportional to the task
- delegation is purposeful and bounded
- success criteria are specific enough to validate
- the Manager does not over-implement the work itself

## Common Failure Signals

- vague role assignments
- unnecessary process overhead
- missing success criteria
- unclear handoff expectations
- jumping into implementation instead of orchestration
