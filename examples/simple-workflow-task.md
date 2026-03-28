# Simple Workflow Task

Use this task to verify that the current operating model works end to end.

## Goal

Create a small `hello.txt` file in the repository root with a one-line greeting that includes the repository name.

Expected content:

`Hello from codex-roams`

## Intended Workflow

1. Manager

- classify the task as trivial or standard
- decide whether a full plan is needed
- hand implementation to Coder if delegation is used

2. Coder

- create the file
- verify the content matches the expected output
- report the implementation result

3. QA

- confirm the file exists
- confirm the content is correct

4. Reviewer

- confirm the task requirements were satisfied
- confirm no unnecessary work was introduced

5. Manager

- summarize the result
- decide that no memory promotion is needed unless the workflow exposed a reusable lesson

## Success Criteria

- `hello.txt` exists in the repository root
- the file contains exactly `Hello from codex-roams`
- the task is completed without unnecessary process overhead

## Why This Task Exists

This task is deliberately simple. It is meant to test:

- Manager-led orchestration
- specialist handoffs
- basic verification discipline
- the decision of whether a task is small enough to avoid extra process
