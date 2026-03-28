# Codex Roams

ROAMS is the name of the operating model used by this template:

- `R`oles
- `O`rchestration
- `A`ctive State
- `M`emory
- `S`kills

This repository is a lightweight template for building an agentic project operating model.

The v1 design is intentionally simple:

- a `Manager` role leads most work
- specialist roles handle bounded responsibilities
- active work is tracked in one plan file
- durable knowledge is promoted into selective memory files

In practice, ROAMS is a small AI operating system for project delivery:

- `Roles` define who owns what
- `Orchestration` keeps the Manager in control of lifecycle and delegation
- `Active State` tracks current work and progress
- `Memory` stores only durable signal
- `Skills` let the system specialize and grow over time

The system is also feedback-driven:

- failed QA sends work back with evidence
- failed review sends work back with actionable findings
- the owning role adjusts its next pass instead of repeating the same attempt
- repeated failures can trigger re-planning or diagnosis mode
- documentation review, memory review, and retrospective review act as explicit commit-readiness gates
- repeated process misses can trigger shared-skill, local-skill, or verification updates

## Repository Layout

- [AGENTS.md](C:\git\codex-roams\AGENTS.md): root operating contract
- [.agent/PLANS.md](C:\git\codex-roams\.agent\PLANS.md): active task template
- [memory/style.md](C:\git\codex-roams\memory\style.md): stable preferences
- [memory/decisions.md](C:\git\codex-roams\memory\decisions.md): important decisions
- [memory/lessons.md](C:\git\codex-roams\memory\lessons.md): durable lessons
- [memory/candidates.md](C:\git\codex-roams\memory\candidates.md): staged candidate memory awaiting promotion, defer, or discard
- [docs/status.md](C:\git\codex-roams\docs\status.md): current repository purpose, stage, goals, and open questions
- [docs/roadmap.md](C:\git\codex-roams\docs\roadmap.md): long-horizon feature sequencing and phase definitions
- [skills/README.md](C:\git\codex-roams\skills\README.md): shared skill sync and versioning contract
- [skills/manager/SKILL.md](C:\git\codex-roams\skills\manager\SKILL.md): orchestration skill
- [skills/diagnosis-ops/SKILL.md](C:\git\codex-roams\skills\diagnosis-ops\SKILL.md): shared failure classification and rework guidance
- [skills/memory-ops/SKILL.md](C:\git\codex-roams\skills\memory-ops\SKILL.md): staged memory promotion and pruning guidance
- [skills/documentation-ops/SKILL.md](C:\git\codex-roams\skills\documentation-ops\SKILL.md): pre-commit documentation review guidance
- [skills/eval-retrospective/SKILL.md](C:\git\codex-roams\skills\eval-retrospective\SKILL.md): post-verification retrospective and process evaluation guidance
- [skills/skill-evolution-ops/SKILL.md](C:\git\codex-roams\skills\skill-evolution-ops\SKILL.md): shared-skill and verification evolution guidance
- [skills/subagent-ops/SKILL.md](C:\git\codex-roams\skills\subagent-ops\SKILL.md): bounded subagent delegation and merge guidance
- [skills/research/SKILL.md](C:\git\codex-roams\skills\research\SKILL.md): Manager-owned research capability
- [skills/bootstrap/SKILL.md](C:\git\codex-roams\skills\bootstrap\SKILL.md): lightweight new-project setup workflow
- [skills/repo-eval-loop/SKILL.md](C:\git\codex-roams\skills\repo-eval-loop\SKILL.md): cross-repo evaluation and planning loop guidance
- [skills/implementation-loop/SKILL.md](C:\git\codex-roams\skills\implementation-loop\SKILL.md): bounded implementation loop guidance that stops before publish
- [skills/ui-designer/SKILL.md](C:\git\codex-roams\skills\ui-designer\SKILL.md): design skill
- [skills/coder/SKILL.md](C:\git\codex-roams\skills\coder\SKILL.md): implementation skill
- [skills/qa/SKILL.md](C:\git\codex-roams\skills\qa\SKILL.md): validation skill
- [skills/reviewer/SKILL.md](C:\git\codex-roams\skills\reviewer\SKILL.md): acceptance skill
- [examples/simple-workflow-task.md](C:\git\codex-roams\examples\simple-workflow-task.md): verification exercise
- [examples/verification/README.md](C:\git\codex-roams\examples\verification\README.md): reusable role and workflow verification suite

## Bootstrap Process

Use this sequence when starting a new project from this template:

1. Copy the template into the new project repository.
2. Update [AGENTS.md](C:\git\codex-roams\AGENTS.md) with project-specific constraints, conventions, and definitions of done.
3. Seed [memory/style.md](C:\git\codex-roams\memory\style.md) with stable preferences for how work should be done.
4. Leave [memory/decisions.md](C:\git\codex-roams\memory\decisions.md) and [memory/lessons.md](C:\git\codex-roams\memory\lessons.md) sparse until real project-level choices or repeated lessons exist.
5. Use [memory/candidates.md](C:\git\codex-roams\memory\candidates.md) to stage setup observations that might become durable later.
6. Rewrite [docs/status.md](C:\git\codex-roams\docs\status.md) to reflect the new repo's purpose, current stage, near-term goals, and open questions.
7. Rewrite [docs/roadmap.md](C:\git\codex-roams\docs\roadmap.md) so phases reflect the new project's actual sequencing rather than this template's internal roadmap.
8. Reset [.agent/PLANS.md](C:\git\codex-roams\.agent\PLANS.md) to the current active task only when non-trivial work begins.
9. Prefer project-local skills when a repository has specialist behavior that should extend a base role rather than overwrite it.
10. Treat shared ROAMS skills as the reusable base operating model and add repo-local skills only for project-specific behavior.
11. After meaningful work, run documentation review, memory review, and retrospective review before considering the work commit-ready.
12. Stage or promote only durable signal into the memory files.

## Standardized Bootstrap Workflow

Use ROAMS on itself when bootstrapping a fresh repo:

1. Manager classifies bootstrap as a standard task and opens `.agent/PLANS.md`.
2. Manager gathers only repo-specific context: purpose, constraints, initial architecture direction, and preferred workflow style.
3. Manager updates `AGENTS.md`, `docs/status.md`, `docs/roadmap.md`, and `memory/style.md` first.
4. Manager records only real initial decisions in `memory/decisions.md`; unknowns stay as open questions or candidate memory.
5. Manager keeps `.agent/PLANS.md` task-local and does not turn it into a backlog.
6. Manager checks whether the repo has project-local skills that should extend base roles such as `UI Designer`.
7. Manager verifies that roadmap, status, and active plan remain clearly separated before closing bootstrap.
8. Manager keeps shared-skill guidance centralized and avoids duplicating generic base-role rules into repo-local skills.

## Bootstrap Checklist

- template copied into the target repository
- `AGENTS.md` rewritten for project-specific constraints
- `docs/status.md` rewritten for the new project snapshot
- `docs/roadmap.md` rewritten for the new project's phase sequence
- `memory/style.md` seeded with stable working preferences
- `memory/decisions.md` updated only if real project decisions already exist
- `memory/candidates.md` used for uncertain but potentially durable setup observations
- `.agent/PLANS.md` reset to the current bootstrap or first implementation task
- project-local skills linked to the base roles they extend when they are the repo's source of truth
- shared-skill versus local-skill boundaries kept explicit
- documentation, memory, and retrospective gates present in the working model
- unnecessary roles, skills, or automation not added preemptively

## Shared Skill Model

ROAMS assumes a shared base operating model plus local extensions.

- shared ROAMS skills are the reusable source of truth for common role behavior
- project-local skills should add repo-specific rules, workflows, prompts, and references
- project-local skills should extend base roles rather than silently replacing them
- the Manager is responsible for checking local extensions before planning or delegation

## Commit-Readiness Gates

Every non-trivial task should pass these gates before it is considered commit-ready:

1. implementation completed
2. validation completed
3. documentation review completed
4. memory review completed
5. retrospective review completed

If a gate does not result in a file change, it should still produce an explicit no-change-needed decision.

## Optional Bootstrap Automation Prompt

Use this prompt when you want Codex to apply ROAMS to a new repository with the smallest practical setup:

```text
Bootstrap this repository from the ROAMS template using the framework on itself.

Goal:
- initialize the repo for its real purpose without over-provisioning process

Required outcomes:
- update AGENTS.md with project-specific constraints and definitions of done
- seed memory/style.md with stable workflow preferences
- keep memory/decisions.md and memory/lessons.md minimal unless real durable signal already exists
- rewrite docs/status.md for the current project snapshot
- rewrite docs/roadmap.md for the project's real phases and sequencing
- reset .agent/PLANS.md to the active bootstrap task
- verify clean separation between roadmap, status, and active-plan artifacts

Guardrails:
- prefer minimal, reviewable changes
- do not invent extra roles unless repeated work justifies them
- stage uncertain setup observations in memory/candidates.md instead of promoting them
- close with verification evidence and any remaining assumptions
```

For a reusable workflow, use [skills/bootstrap/SKILL.md](C:\git\codex-roams\skills\bootstrap\SKILL.md).

## Document Model

ROAMS uses three different planning/state documents with distinct responsibilities:

- [docs/status.md](C:\git\codex-roams\docs\status.md): current state, current stage, near-term goals, and open questions
- [docs/roadmap.md](C:\git\codex-roams\docs\roadmap.md): long-horizon feature sequencing, promotion candidates, and phase exit criteria
- [.agent/PLANS.md](C:\git\codex-roams\.agent\PLANS.md): active task execution plan for the work currently being performed

Keep these documents separate. Status is not backlog, roadmap is not active execution detail, and plans are not long-horizon strategy.

## Default Workflow

The current workflow is:

1. Manager classifies the task.
2. Manager gathers the minimum required context.
3. Manager checks for relevant project-local skill extensions.
4. Manager triggers research when external knowledge must be verified.
5. Manager creates or updates the active plan.
6. Manager delegates to specialist roles only when useful.
7. Specialist roles execute bounded work and return evidence.
8. QA and Reviewer validate non-trivial work.
9. Manager runs documentation review, memory review, and retrospective review.
10. Failed checks trigger rework with explicit evidence and a revised next step.
11. Manager closes the task and decides whether memory, shared skills, local skills, verification coverage, or roadmap guidance should change.

## Research Capability

Research is a Manager-owned capability rather than a standalone role in v1.

Use research when:

- implementation depends on external documentation or APIs
- current technical behavior must be verified
- multiple technical options need comparison
- a failed pass suggests an external assumption may be wrong

The default source preference is:

1. official and canonical sources
2. first-party technical artifacts
3. high-quality secondary sources
4. community or social sources only as a last resort

Research findings should usually be shared as a short Research Brief containing:

- question
- recommendation
- verified findings
- inference, if any
- sources
- constraints or caveats
- implementation impact
- open questions

## Automation Loops

ROAMS treats automation as a Manager-owned capability.

Recommended automation layering:

1. `repo-eval-loop`
- evaluate repo state, roadmap, active plan, memory, and GitHub issues
- recommend the next bounded task
- stop with a decision-ready summary before publish

2. `implementation-loop`
- execute one approved plan item
- validate the result
- run documentation, memory, and retrospective gates
- stop before publish

Automation should improve planning and execution discipline first.
Autonomous publishing stays out of scope until the evaluation harness proves the loops are reliable.

## Adding Roles Over Time

Add a new role only when one of these is true:

- a repeated task needs a distinct workflow
- a repeated task needs different validation rules
- the role needs different tools or context than existing roles
- the role needs to operate independently enough to justify a future subagent

When adding a role:

1. Create `skills/<role-name>/SKILL.md`.
2. Keep the skill concise and focused on workflow, rules, and outputs.
3. Define what the role owns and what it does not own.
4. Define what evidence it must return to the Manager.
5. Update [AGENTS.md](C:\git\codex-roams\AGENTS.md) only if the new role changes the system's default hierarchy or lifecycle.

Do not add a role just to mirror a job title. Add it when it creates clearer ownership or better outcomes.

## Verification Exercise

Use [examples/simple-workflow-task.md](C:\git\codex-roams\examples\simple-workflow-task.md) as a small end-to-end test of the operating model.

For more complete validation, use the suite in [examples/verification/README.md](C:\git\codex-roams\examples\verification\README.md). It separates role-level verification from a standard end-to-end workflow test so the operating model can be tuned incrementally.
