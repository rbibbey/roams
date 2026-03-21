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

## Repository Layout

- [AGENTS.md](C:\git\codex-roams\AGENTS.md): root operating contract
- [.agent/PLANS.md](C:\git\codex-roams\.agent\PLANS.md): active task template
- [memory/style.md](C:\git\codex-roams\memory\style.md): stable preferences
- [memory/decisions.md](C:\git\codex-roams\memory\decisions.md): important decisions
- [memory/lessons.md](C:\git\codex-roams\memory\lessons.md): durable lessons
- [docs/status.md](C:\git\codex-roams\docs\status.md): current repository purpose, stage, goals, and open questions
- [skills/manager/SKILL.md](C:\git\codex-roams\skills\manager\SKILL.md): orchestration skill
- [skills/research/SKILL.md](C:\git\codex-roams\skills\research\SKILL.md): Manager-owned research capability
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
3. Add or revise entries in [memory/style.md](C:\git\codex-roams\memory\style.md) to reflect how you want work performed.
4. Record any initial architecture choices in [memory/decisions.md](C:\git\codex-roams\memory\decisions.md).
5. Expand the role skills only when the project needs more specialized behavior.
6. For non-trivial work, instantiate the template in [.agent/PLANS.md](C:\git\codex-roams\.agent\PLANS.md) and let the Manager lead the lifecycle.
7. After meaningful work, promote only durable signal into the memory files.

## Default Workflow

The v1 workflow is:

1. Manager classifies the task.
2. Manager gathers the minimum required context.
3. Manager triggers research when external knowledge must be verified.
4. Manager creates or updates the active plan.
5. Manager delegates to specialist roles only when useful.
6. Specialist roles execute bounded work and return evidence.
7. QA and Reviewer validate non-trivial work.
8. Failed checks trigger rework with explicit evidence and a revised next step.
9. Manager closes the task and decides whether memory should change.

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
