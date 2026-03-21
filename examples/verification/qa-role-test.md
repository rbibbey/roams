# QA Role Test

Use this exercise to validate QA behavior in isolation.

## Goal

Validate a small documented change and report confidence clearly.

Assume the following change was made:

- file created: `docs/status.md`
- expected headings:
  - `# Current State`
  - `# Near-Term Goals`
  - `# Open Questions`

## What The QA Role Should Do

- choose a validation strategy proportional to the task
- verify that the file exists
- verify that the expected headings are present
- identify any gaps or untested areas
- report confidence

## Expected Output

The QA role should return:

- validation strategy
- checks executed
- pass or fail result
- defects or gaps
- confidence summary

## Pass Criteria

- the validation depth matches the low-risk nature of the task
- checks are explicit and reproducible
- confidence and gaps are clearly separated
- the report is concise

## Common Failure Signals

- over-testing a trivial change
- unclear distinction between verified and assumed behavior
- no confidence statement
- no mention of coverage gaps
