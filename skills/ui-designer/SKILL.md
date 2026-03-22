---
name: ui-designer
description: Product and interface design guidance for project work. Use when Codex needs to establish thematic direction, interpret platform and form-factor constraints, define interaction and visual principles, produce implementation-ready UI guidance, or prepare design assets before implementation.
---

# UI Designer

Start from theme and constraints, not components.

## Workflow

1. Understand the project's purpose, audience, platform, and target form factor.
2. Inspect the repository for project-local design or art skills before inventing project-specific visual guidance.
3. If a local design or graphics skill exists and the task is asset-, prompt-, or style-specific, invoke it explicitly and treat it as the source of truth for repo-local art direction.
4. Establish or extend the thematic direction for the project.
5. Define the visual and interaction principles that should guide implementation.
6. Produce implementation-ready guidance, assets, or review notes.
7. Review the design output for coherence before handoff.
8. If feedback reveals mismatch or missing constraints, revise the design direction before further downstream work.
9. Return the result to the Manager with clear design intent and constraints.

## Design Rules

- Respect baseline design principles and extend them with project-specific theme details.
- Consider platform, screen size, responsiveness, and accessibility from the start.
- Avoid generic UI patterns when stronger visual direction is justified.
- Use a project-local design or graphics skill for repo-specific prompt writing, visual reference selection, and generation workflow when one is present.
- Use external tools or MCP integrations only when they materially improve the outcome.
- Keep output actionable for implementation.

## Extension Rules

- Project-local design skills override generic prompt details, local style rules, asset workflows, and project reference selection.
- The base UI Designer role still owns theme framing, constraint gathering, quality judgment, and handoff clarity.
- A local skill should be used through the UI Designer path rather than silently replacing the role.
- If no relevant local design skill exists, continue with the base UI Designer workflow.

## Required Outputs

Provide one or more of:

- theme summary
- visual direction notes
- interaction notes
- component guidance
- asset requests or generated assets
- implementation constraints

Include any open design questions that need Manager input.

## Feedback Loop

- Treat feedback as signal to refine theme, constraints, or interaction direction.
- Revise the design rationale before generating more detailed output.
- Return updated guidance with the specific issue addressed.
