# Standard Workflow Test

Use this exercise to validate the full ROAMS workflow for a standard non-trivial task.

## Goal

Add a small but complete repository improvement that requires planning, implementation, validation, review, and closure.

Task:

`Create a docs/status.md file that summarizes the repository's current purpose, current stage, near-term goals, and open questions. Then update README.md to link to the new file from the repository layout section.`

## Why This Is A Good Standard Test

This task is large enough to require:

- Manager classification and planning
- Coder implementation
- QA verification
- Reviewer acceptance

But it is still small enough to execute quickly and reason about clearly.

## Expected Workflow

1. Manager

- classify the task as standard
- gather context from `README.md` and current repository structure
- decide to use a lightweight plan
- assign implementation to Coder
- define validation and review expectations

2. Coder

- create `docs/status.md`
- update `README.md`
- verify the new file and link
- return implementation summary

3. QA

- confirm both file changes exist
- confirm `README.md` links to `docs/status.md`
- confirm `docs/status.md` includes the requested sections
- report confidence and any gaps

4. Reviewer

- confirm the result matches the task request
- confirm the changes are minimal and maintainable
- identify any missing requirement or quality issue

5. Manager

- summarize the outcome
- decide whether any memory should be promoted

## Success Criteria

- `docs/status.md` exists
- `docs/status.md` includes sections for purpose, current stage, near-term goals, and open questions
- `README.md` includes a link to `docs/status.md` in the repository layout
- verification evidence is recorded
- review reaches a clear acceptance decision
- the Manager closes the task cleanly

## Suggested Evidence To Capture

- final classification
- short active plan
- implementation summary
- validation report
- review result
- final closure summary

## Common Failure Signals

- no plan for a standard task
- weak role handoffs
- missing verification evidence
- Reviewer acting like a second implementer
- Manager closing the task without clear acceptance
