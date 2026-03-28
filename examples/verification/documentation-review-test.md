# Documentation Review Test

Use this exercise to validate ROAMS documentation review behavior.

## Goal

Verify that ROAMS treats documentation review as an explicit pre-commit gate.

## Scenario

Assume a task changed:

- the command used to start the development server
- a small internal helper implementation that does not affect behavior

## What The Test Should Check

- whether the startup-command change triggers a docs update
- whether the internal helper refactor can produce an explicit no-doc-update-needed decision
- whether the review inspects operating docs when process expectations changed

## Expected Output

- docs-changed or no-doc-update-needed decision per change
- affected doc areas when updates are required
- brief rationale
- any remaining doc drift risk

## Pass Criteria

- behavior or setup changes trigger a docs update decision
- no-change cases still return an explicit gate result
- the gate is treated as required before commit readiness

## Common Failure Signals

- assuming docs are optional
- changing behavior without reviewing docs
- returning no explicit gate result
