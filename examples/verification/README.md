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
- [ui-designer-local-skill-test.md](C:\git\codex-roams\examples\verification\ui-designer-local-skill-test.md): validates UI Designer behavior when a project-local art skill is present
- [research-capability-test.md](C:\git\codex-roams\examples\verification\research-capability-test.md): validates canonical-source research and briefing
- [memory-promotion-test.md](C:\git\codex-roams\examples\verification\memory-promotion-test.md): validates staged memory promotion and bucket selection
- [documentation-review-test.md](C:\git\codex-roams\examples\verification\documentation-review-test.md): validates explicit docs-gate decisions before commit readiness
- [eval-retrospective-test.md](C:\git\codex-roams\examples\verification\eval-retrospective-test.md): validates post-verification process evaluation and remedy selection
- [skill-evolution-test.md](C:\git\codex-roams\examples\verification\skill-evolution-test.md): validates repeated-omission escalation into skill or verification updates
- [diagnosis-rework-test.md](C:\git\codex-roams\examples\verification\diagnosis-rework-test.md): validates failure classification and narrower rework
- [subagent-orchestration-test.md](C:\git\codex-roams\examples\verification\subagent-orchestration-test.md): validates bounded parallel delegation and merge rules
- [bootstrap-automation-test.md](C:\git\codex-roams\examples\verification\bootstrap-automation-test.md): validates fresh-repo bootstrap and lightweight setup behavior
- [cross-repo-eval-loop-test.md](C:\git\codex-roams\examples\verification\cross-repo-eval-loop-test.md): validates repo-state plus issue-driven next-task evaluation
- [implementation-loop-test.md](C:\git\codex-roams\examples\verification\implementation-loop-test.md): validates bounded implementation plus commit-readiness gates and stop-before-publish behavior
- [roadmap-governance-test.md](C:\git\codex-roams\examples\verification\roadmap-governance-test.md): validates roadmap, status, and active-plan separation
- [standard-workflow-test.md](C:\git\codex-roams\examples\verification\standard-workflow-test.md): validates the full Manager -> specialist -> validation -> review -> closure flow

## How To Use The Suite

Run the tests in this order:

1. role tests
2. capability tests
3. evaluation and automation-loop tests
4. governance tests
5. standard workflow test

The role tests should be run first so each role can be tuned independently before validating capability behavior, commit-readiness gates, automation-loop behavior, document governance, and orchestration across the full system.

## Evaluation Rules

For each test, capture:

- classification of task complexity
- role output
- verification evidence
- pass or fail decision
- friction or confusion observed
- candidate improvements to roles, memory, or workflow
- whether the result exposed a shared-skill, local-skill, or verification improvement

## Promotion Guidance

Do not promote memory just because a test ran.

Promote only when a test reveals:

- a repeated ambiguity
- a missing operating rule
- a role boundary problem
- a reusable improvement to handoffs or validation
