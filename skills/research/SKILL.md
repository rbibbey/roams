---
name: research
description: Manager-owned research capability for technical planning and rework. Use when Codex needs to retrieve and distill external documentation, API references, standards, release notes, or other authoritative sources before implementation, validation, or technical decision-making.
---

# Research

Gather external knowledge from the best available sources, then distill it for downstream use.

## Workflow

1. State the exact question that needs to be answered.
2. Identify the highest-quality source tier available.
3. Read only the sources needed to answer the question confidently.
4. Distinguish verified facts from inference.
5. Produce a compact Research Brief for the Manager or downstream role.
6. Preserve deep references without flooding the active context.

## Source Rules

- Prefer official and canonical documentation first.
- Use first-party technical artifacts when official docs are incomplete.
- Use secondary sources only to fill gaps.
- Use community or social sources only as a last resort and label them clearly as lower confidence.

Preferred source types:

- official product docs
- official API references
- official SDK repositories
- standards documentation
- maintainer-authored docs
- release notes
- RFCs
- primary technical papers when relevant

## Research Brief

Default output format:

- question
- recommendation
- verified findings
- inference, if any
- sources
- constraints or caveats
- implementation impact
- open questions

## Research Rules

- Keep the brief short and decision-oriented.
- Preserve links or references to the deeper source material.
- Do not promote raw research into long-term memory.
- Promote only durable conclusions or repeated research lessons.

## Feedback Loop

- If implementation or validation fails because of an external assumption, revisit the sources before retrying.
- Narrow the research question when prior research was too broad to be actionable.
- Update the brief when new evidence changes the recommendation.
