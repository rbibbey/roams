# Skill Evolution Test

Use this exercise to validate ROAMS skill and verification evolution behavior.

## Goal

Verify that repeated omissions can trigger shared-skill, local-skill, verification, or roadmap changes without waiting for a user to propose the improvement manually.

## Scenario

Assume the last three non-trivial tasks showed this pattern:

1. Documentation review was skipped until the user asked for it.
2. Memory review happened only after the user explicitly requested learnings.
3. The same omission appeared in two separate repositories using the shared Manager guidance.

## What The Test Should Check

- whether the pattern is strong enough to justify more than a one-off note
- whether the remedy should target shared skill guidance, local skill guidance, verification coverage, or roadmap sequencing
- whether the chosen remedy is the smallest durable fix

## Expected Output

- repeated pattern summary
- evidence threshold judgment
- selected remedy target
- brief rationale

## Pass Criteria

- repeated omissions can trigger a framework-improvement decision
- the remedy is routed to the correct target
- one-off frustration is not over-promoted without evidence

## Common Failure Signals

- waiting for the user to request the improvement manually
- always adding memory instead of improving skills or verification
- overreacting to a single isolated miss
