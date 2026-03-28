# Eval Retrospective Test

Use this exercise to validate ROAMS retrospective and process-evaluation behavior.

## Goal

Verify that ROAMS evaluates process quality even when the code result itself is acceptable.

## Scenario

Assume a task was completed successfully, but:

- the user had to remind the system to update documentation
- the first validation pass missed an obvious regression
- the final code change was still correct after rework

## What The Test Should Check

- whether the retrospective compares the plan versus actual execution
- whether the repeated or meaningful misses are treated as process findings
- whether the output chooses the right recommendation state
- whether the remedy is routed to memory, skill guidance, verification, or roadmap refinement

## Expected Output

- plan-versus-execution summary
- process findings
- failure class when applicable
- recommendation state
- remedy location

## Pass Criteria

- correct code does not suppress process evaluation
- user nudges and missed gates are treated as evidence
- the recommendation is decision-ready for the Manager

## Common Failure Signals

- skipping retrospective because the implementation succeeded
- treating process friction as noise
- failing to identify a remedy location
