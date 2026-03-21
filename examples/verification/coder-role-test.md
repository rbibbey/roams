# Coder Role Test

Use this exercise to validate Coder behavior in isolation.

## Goal

Implement a small documentation feature with local verification.

Task:

`Create a new file at docs/status.md with three sections: Current State, Near-Term Goals, and Open Questions. Add one short placeholder sentence under each heading.`

## What The Coder Should Do

- identify the minimal change set
- create the file
- keep the implementation simple and consistent with repository style
- verify the file exists and has the requested sections
- return a concise handoff

## Expected Output

The Coder should return:

- implementation summary
- files changed
- verification performed
- known limitations or assumptions

## Pass Criteria

- only the required file is created or changed
- the content matches the request
- verification is explicit
- the handoff is concise and useful

## Common Failure Signals

- making unnecessary extra changes
- omitting verification
- vague handoff notes
- introducing extra structure beyond the task
