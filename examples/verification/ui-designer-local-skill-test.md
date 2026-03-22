# UI Designer Local Skill Test

Use this exercise to validate UI Designer behavior when a repository includes a project-local art or design skill.

## Goal

Verify that UI Designer stays responsible for design orchestration while explicitly using the local skill as the source of truth for repo-specific asset direction.

## Scenario

Assume the following task:

`Design a new sewer-themed score plate for a game repository that includes a local art-generation skill with project-specific style rules and reference assets.`

Assume:

- the repository contains a local skill for project-specific art direction
- the task is asset-specific rather than a general product-design exercise
- the local skill defines style anchors, prompt structure, and generation workflow

## What The Test Should Check

- whether UI Designer explicitly chooses the local skill
- whether UI Designer cites the local skill as the source of truth for repo-specific prompt and asset details
- whether the response still frames the theme, constraints, and handoff clearly
- whether the response avoids duplicating the local skill's detailed prompt rules
- whether implementation-ready guidance still returns to the Manager or downstream implementer

## Expected Output

The UI Designer should return:

- decision to use the local skill
- high-level theme and task framing
- relevant design constraints
- local references or source-of-truth note
- concise handoff guidance for implementation or generation

## Pass Criteria

- the local skill is invoked explicitly
- project-specific visual guidance is delegated to the local skill rather than reinvented
- UI Designer remains the orchestration and quality layer
- the output is specific enough to hand off without copying the local skill wholesale

## Common Failure Signals

- ignoring the local skill and improvising generic art prompts
- copying the local skill verbatim instead of orchestrating through it
- losing theme framing or implementation handoff clarity
- treating the local skill as a full replacement for UI Designer
