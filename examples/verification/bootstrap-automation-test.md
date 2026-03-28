# Bootstrap Automation Test

Use this exercise to validate lightweight new-project bootstrap behavior.

## Goal

Verify that ROAMS can initialize a fresh repository consistently, keep setup minimal, and preserve clean separation between long-horizon, current-state, and active-task artifacts.

## Scenario

Assume the following task:

`Start a new ROAMS-enabled repository for a CLI release tool that needs clear delivery workflow rules but no extra specialist roles yet.`

Assume:

- the template has just been copied into the new repository
- the project purpose is known
- only a few stable workflow preferences are known at bootstrap time
- no durable lessons exist yet

## What The Test Should Check

- whether bootstrap is classified as a standard task
- whether `AGENTS.md` is updated with project-specific constraints
- whether `memory/style.md` is seeded without overfilling other memory files
- whether `docs/status.md` and `docs/roadmap.md` are rewritten for the new project
- whether shared-skill versus local-skill boundaries stay explicit
- whether documentation review, memory review, and retrospective review are present in the operating model after bootstrap
- whether `.agent/PLANS.md` is reset to the active bootstrap or first implementation task
- whether an optional automation prompt or reusable procedure can drive the same setup

## Expected Output

The test should return:

- bootstrap plan summary
- list of files that should change first
- memory seeding decision
- shared-skill versus local-skill boundary decision
- verification checks for document separation
- verification checks for commit-readiness gates
- reason the setup remains lightweight

## Pass Criteria

- bootstrap updates the repo consistently with minimal manual ambiguity
- status, roadmap, and active plan serve different purposes
- memory starts sparse and evidence-driven
- shared skills remain centralized while repo-specific behavior stays local
- no extra roles or automation layers are added without justification

## Common Failure Signals

- copying this template's roadmap phases directly into the new project
- pre-populating decisions or lessons with speculation
- using `.agent/PLANS.md` as backlog instead of active execution state
- blurring shared-skill and local-skill responsibilities
- adding more process than the new repository currently needs
