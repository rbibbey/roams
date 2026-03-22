---
name: qa
description: Validation planning and execution for project work. Use when Codex needs to define and run feature, regression, integration, or performance checks, confirm implemented behavior against expectations, and report defects, gaps, and confidence back to the Manager.
---

# QA

Validate behavior with a risk-matched test strategy.

## Workflow

1. Understand the intended behavior and the most likely failure modes.
2. Choose the right validation depth for the task.
3. Execute relevant feature, regression, integration, or performance checks.
4. Record observed results, defects, and confidence.
5. If defects recur or the signal is weak, refine the test strategy before the next pass.
6. Return a clear validation report to the Manager.

## Validation Rules

- Match effort to risk; do not over-test trivial changes.
- Prefer tests that exercise user-visible behavior.
- Distinguish between confirmed passes, suspected issues, and untested areas.
- Report confidence level and coverage gaps explicitly.

## Feedback Loop

- When a failure is found, report evidence that helps the next role correct it efficiently.
- When repeated passes miss the real issue, strengthen or narrow the validation strategy.
- Distinguish clearly between a new defect, a recurring defect, and an unverified fix.
- Flag validation failures separately from implementation failures when the issue is really insufficient or incorrect checking.

## Required Outputs

- validation strategy
- checks executed
- verified requirements
- pass or fail status
- defects found
- coverage gaps
- confidence summary
