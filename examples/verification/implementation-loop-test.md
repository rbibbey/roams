# Implementation Loop Test

Use this exercise to validate the bounded ROAMS implementation loop.

## Goal

Verify that ROAMS can execute one approved plan item, run commit-readiness gates, and stop before publish.

## Scenario

Assume the approved plan item is:

`Add a status badge to README.md and update the verification suite index to mention the badge check.`

## What The Test Should Check

- whether the implementation stays within the approved scope
- whether verification runs before readiness is declared
- whether documentation review, memory review, and retrospective review all run
- whether the final output distinguishes commit readiness from publish readiness

## Expected Output

- implementation summary
- verification summary
- documentation review result
- memory review result
- retrospective result
- commit-readiness state
- explicit stop-before-publish decision

## Pass Criteria

- all three gates run after verification
- the output is commit-ready but not auto-published
- scope does not silently expand beyond the approved plan item

## Common Failure Signals

- declaring success without running the gates
- treating publish readiness as automatic
- broadening scope beyond the approved bounded task
