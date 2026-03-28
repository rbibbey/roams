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
- documentation review
- memory review
- retrospective review

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
- return `accepted` or `rework required` to the Manager without waiting on the user
- include a recommended Manager action and escalation reason only when a human decision is truly needed

5. Manager

- summarize the outcome
- consume reviewer output and either close the task or route rework
- run documentation review and record whether docs changed or no docs update was needed
- run memory review and record whether memory changed or no durable update was needed
- run retrospective review and record whether the process needs no change, a candidate improvement, or a required skill/process update
- involve the user only when the review handback identifies a genuine escalation case
- decide whether any memory, skill, verification, or roadmap guidance should change

## Success Criteria

- `docs/status.md` exists
- `docs/status.md` includes sections for purpose, current stage, near-term goals, and open questions
- `README.md` includes a link to `docs/status.md` in the repository layout
- verification evidence is recorded
- review reaches a clear acceptance decision
- documentation review result is recorded
- memory review result is recorded
- retrospective result is recorded
- the Manager closes the task cleanly
- no child thread requires user intervention when the Manager can proceed
- specialist handbacks are detailed enough for the Manager to decide whether user involvement is necessary

## Suggested Evidence To Capture

- final classification
- short active plan
- implementation summary
- validation report
- review result
- documentation review result
- memory review result
- retrospective result
- final closure summary
- any rework handoff, if review fails

## Common Failure Signals

- no plan for a standard task
- weak role handoffs
- missing verification evidence
- missing gate decisions after verification
- Reviewer acting like a second implementer
- Manager closing the task without clear acceptance
- Reviewer or Manager leaving the task in a user-facing waiting state without a real escalation
