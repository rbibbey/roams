# ROAMS Roadmap

This document is the source of truth for post-v1 ROAMS feature sequencing.

Use the three-document model:

- `docs/status.md` for the current project snapshot
- `docs/roadmap.md` for long-horizon roadmap sequencing and phase definitions
- `.agent/PLANS.md` for the active execution plan of work currently in flight

## Roadmap Principles

- Keep the roadmap capability-first, not role-forward.
- Add new roles only after repeated evidence shows a capability needs its own ownership boundary.
- Keep active implementation detail in `.agent/PLANS.md`, not in the roadmap.
- Keep `docs/status.md` short and focused on current state, not future backlog.
- Move completed phases to concise historical notes rather than leaving them in the active backlog.
- When a phase begins, the Manager should spin a task-specific execution plan from this roadmap into `.agent/PLANS.md`.
- Roadmap entries should define intended capability, sequencing, and acceptance criteria before implementation begins.

## Current Phase

Current roadmap state:

- completed: v1 foundation
- completed: Manager-owned research capability
- completed: Phase 2 - Memory Operations
- completed: Phase 3 - Rework And Diagnosis Taxonomy
- completed: Phase 4 - Subagent Orchestration Rules
- completed: Phase 5 - Bootstrap Automation
- completed: Phase 6 - Commit-Readiness Gates And Retrospective Loops
- next active phase: Phase 7 - Cross-Repo Evaluation And Implementation Loops

Phase 7 can now build on the explicit commit-readiness gates and self-improvement rules added in Phase 6.

## Planned Phases

### Phase 2: Memory Operations

Goal:

Make memory updates deliberate, reviewable, and resistant to noise.

Deliverables:

- candidate memory staging flow before promotion
- explicit memory promotion checklist
- memory pruning and review workflow
- stale-memory detection rules
- memory update triggers for success, failure, and repeated patterns
- guidance for when information belongs in `style`, `decisions`, `lessons`, or nowhere

Required additions:

- update `AGENTS.md` memory rules
- add a new skill or guidance module for memory operations if the workflow becomes large enough
- add at least one verification scenario focused on promotion versus non-promotion decisions

Acceptance criteria:

- ROAMS can distinguish temporary working notes from durable memory
- memory updates are rule-driven rather than ad hoc
- repeated noise does not accumulate in long-term memory

### Phase 3: Rework And Diagnosis Taxonomy

Goal:

Make failure handling precise, shared, and more effective than blind retry.

Deliverables:

- failure classification categories
- diagnosis-mode trigger rules
- rework handoff template
- root-cause recording rules
- distinction between implementation failure, validation failure, design failure, and wrong-assumption failure
- guidance for when research should re-trigger during rework

Required additions:

- extend `AGENTS.md` escalation and rework sections
- update Manager, Coder, QA, and Reviewer skills to use the same failure vocabulary
- add verification scenarios that intentionally fail and require one rework cycle

Acceptance criteria:

- ROAMS has a consistent vocabulary for failure and recovery
- rework is narrower and more evidence-driven than a blind retry
- repeated failures can trigger diagnosis mode predictably

### Phase 4: Subagent Orchestration Rules

Goal:

Enable bounded parallel execution without weakening Manager control or causing duplicate work.

Deliverables:

- explicit delegation contract format
- ownership-boundary rules for parallel work
- allowed and disallowed subagent cases
- handoff artifact expectations
- merge and review rules for independently produced work
- Manager guidance for deciding role-mode versus subagent execution

Required additions:

- update `AGENTS.md` role-versus-subagent section
- add Manager guidance for subagent invocation decisions
- add at least one workflow verification scenario with parallel bounded delegation

Acceptance criteria:

- subagents are only used when work is parallelizable and independently reviewable
- handoffs are concrete enough to avoid duplicated or conflicting work
- Manager remains the orchestration authority

### Phase 5: Bootstrap Automation

Goal:

Make new-project setup consistent, lightweight, and repeatable.

Deliverables:

- standardized new-project bootstrap workflow
- template-copy and setup checklist
- initial memory seeding guidance
- initial roadmap and status initialization guidance
- optional automation prompt for starting a new ROAMS-enabled repo

Required additions:

- extend `README.md` bootstrap instructions
- add a bootstrap skill or reusable setup procedure if needed
- add a verification scenario for starting a fresh repo from the template

Acceptance criteria:

- a new project can be initialized consistently with minimal manual setup
- bootstrap does not over-provision roles, memory, or process
- the initial repo starts with clean separation between roadmap, status, and active-plan artifacts

### Phase 6: Commit-Readiness Gates And Retrospective Loops

Goal:

Make documentation review, memory review, and retrospective review explicit lifecycle gates instead of optional reminders.

Deliverables:

- explicit documentation review rules in the operating model
- explicit memory review as a required pre-commit gate
- explicit retrospective and evaluation loop after validation
- skill-evolution guidance for shared-skill and verification refinement
- verification scenarios covering docs, memory, retrospective, and repeated omission patterns

Required additions:

- update `AGENTS.md` lifecycle and Definition of Done rules
- add skills for documentation review, retrospective evaluation, and skill evolution if the workflow benefits from explicit capability modules
- expand `examples/verification/` to cover the new gates and evaluation loop

Acceptance criteria:

- non-trivial tasks are not considered commit-ready until the three gates run
- retrospective can recommend no change, a candidate improvement, or a required skill/process update
- repeated omissions can be routed into shared-skill, local-skill, verification, or roadmap updates

### Phase 7: Cross-Repo Evaluation And Implementation Loops

Goal:

Turn ROAMS into a bounded planning and execution loop that can inspect repository state, evaluate next work, and stop safely before publish.

Deliverables:

- reusable cross-repo evaluation-and-planning loop guidance
- bounded implementation loop guidance that consumes one approved plan item at a time
- issue-aware repo evaluation inputs and output format
- stop-before-publish decision gate
- verification scenarios covering issue-driven planning and commit-ready loop behavior

Required additions:

- add explicit automation-loop guidance modules or skills
- expand `README.md` with automation loop layering
- add verification scenarios for cross-repo evaluation and implementation-loop gates

Acceptance criteria:

- the evaluation loop can combine roadmap, active plan, memory, retrospective output, and issue context into one clear next-step recommendation
- the implementation loop includes validation plus documentation, memory, and retrospective gates
- the loops stop before publish and return a decision-ready handoff rather than auto-publishing

## Promotion Candidates

These are not committed roadmap phases. They are capability-first promotion candidates.

### Researcher

- current capability owner: Manager via the `research` capability
- trigger for promotion: research repeatedly becomes a substantial bounded task requiring independent synthesis before implementation
- non-promotion default: keep research Manager-owned and hand distilled briefs to downstream roles
- evidence needed before promotion: repeated research-heavy tasks, sustained context pressure on the Manager, or repeated need for independent comparative analysis

### Automation

- current capability owner: Manager with bootstrap and workflow automation support
- trigger for promotion: recurring setup, maintenance, or orchestration work justifies its own operating mode
- non-promotion default: keep automation as a capability invoked by the Manager through bounded evaluation and implementation loops
- evidence needed before promotion: repeated automation patterns across projects and stable handoff requirements

### Debugger Or Diagnostician

- current capability owner: Manager plus QA and Coder through diagnosis and rework workflows
- trigger for promotion: diagnosis work becomes large enough that existing Manager, QA, and Coder guidance is no longer sufficient
- non-promotion default: keep diagnosis distributed across current roles with shared failure taxonomy
- evidence needed before promotion: repeated multi-pass failures where root-cause isolation becomes a substantial independent task

## Deferred Items

- additional specialist roles beyond the current operating model
- autonomous publishing beyond bounded evaluation and implementation support
- role promotion without repeated evidence
- broad MCP integrations not yet justified by repeated use
- expanded design asset workflows until UI work requires them regularly

## Exit Criteria Per Phase

Each roadmap phase is complete only when:

- the intended capability is documented in the operating model
- related skills or guidance modules are updated consistently
- at least one targeted verification scenario exists for the phase
- the phase acceptance criteria are met
- the next phase can begin without reopening unresolved decisions from the completed one
