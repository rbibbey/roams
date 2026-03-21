# Verification Suite

This directory contains a reusable verification suite for the ROAMS operating model.

The suite is designed to answer two questions:

1. Can each role perform its core responsibility in isolation?
2. Can the full system execute a standard non-trivial workflow cleanly?

## Structure

- [manager-role-test.md](C:\git\codex-roams\examples\verification\manager-role-test.md): validates Manager orchestration behavior
- [ui-designer-role-test.md](C:\git\codex-roams\examples\verification\ui-designer-role-test.md): validates UI Designer design workflow
- [coder-role-test.md](C:\git\codex-roams\examples\verification\coder-role-test.md): validates implementation workflow
- [qa-role-test.md](C:\git\codex-roams\examples\verification\qa-role-test.md): validates testing and reporting workflow
- [reviewer-role-test.md](C:\git\codex-roams\examples\verification\reviewer-role-test.md): validates final review behavior
- [standard-workflow-test.md](C:\git\codex-roams\examples\verification\standard-workflow-test.md): validates the full Manager -> specialist -> validation -> review -> closure flow

## How To Use The Suite

Run the tests in this order:

1. role tests
2. standard workflow test

The role tests should be run first so each role can be tuned independently before validating orchestration across the full system.

## Evaluation Rules

For each test, capture:

- classification of task complexity
- role output
- verification evidence
- pass or fail decision
- friction or confusion observed
- candidate improvements to roles, memory, or workflow

## Promotion Guidance

Do not promote memory just because a test ran.

Promote only when a test reveals:

- a repeated ambiguity
- a missing operating rule
- a role boundary problem
- a reusable improvement to handoffs or validation
