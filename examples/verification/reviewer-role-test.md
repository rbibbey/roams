# Reviewer Role Test

Use this exercise to validate Reviewer behavior in isolation.

## Goal

Review a small completed task for readiness and correctness.

Assume the following implementation summary:

- created `docs/status.md`
- added requested headings and placeholder text
- verified that the file exists and contains the expected headings

## What The Reviewer Should Do

- compare the result to the original request
- check for missing requirements
- check for unnecessary complexity
- assess obvious quality or maintainability issues
- return acceptance findings

## Expected Output

The Reviewer should return:

- acceptance status
- findings ordered by severity, if any
- residual risks
- review confidence

## Pass Criteria

- review focuses on correctness and requirement coverage first
- findings are specific and actionable
- the Reviewer explicitly states when no material findings exist
- style-only feedback does not overshadow correctness

## Common Failure Signals

- vague critique without concrete impact
- focusing on style before correctness
- no explicit acceptance decision
- restating the implementation without reviewing it
