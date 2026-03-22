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
- return a terminal handback to the Manager

## Expected Output

The Reviewer should return:

- acceptance status
- findings ordered by severity, if any
- residual risks
- review confidence
- recommended Manager action: close, route rework, or escalate
- escalation reason, only if escalation is recommended
- if the work is not ready, a rework handoff with failure class, evidence, owning role, narrower next step, and expected re-validation

## Pass Criteria

- review focuses on correctness and requirement coverage first
- findings are specific and actionable
- the Reviewer explicitly states when no material findings exist
- style-only feedback does not overshadow correctness
- the Reviewer ends in `accepted` or `rework required`
- the Reviewer does not ask the user for feedback when the Manager can proceed
- the Reviewer gives the Manager enough detail to decide whether escalation is actually necessary

## Common Failure Signals

- vague critique without concrete impact
- focusing on style before correctness
- no explicit acceptance decision
- restating the implementation without reviewing it
- asking the user to decide the next step instead of handing back to the Manager
