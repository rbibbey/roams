---
name: implementation-loop
description: Bounded implementation-loop guidance for ROAMS. Use when Codex needs to execute one approved plan item, verify it, run commit-readiness gates, and stop before publish.
---

# Implementation Loop

Execute one approved task slice and stop before publish.

## Workflow

1. Consume one approved bounded plan item.
2. Implement the smallest viable slice.
3. Run relevant verification.
4. Run documentation review.
5. Run memory review.
6. Run retrospective review.
7. Prepare a commit-ready summary.
8. Stop before publish.

## Rules

- Do not silently broaden scope beyond the approved plan item.
- If verification or a gate fails, route the work back through rework rather than pretending the loop is complete.
- Treat commit readiness and publish readiness as different states.

## Required Outputs

- implementation summary
- verification summary
- documentation review result
- memory review result
- retrospective result
- commit-readiness state
- explicit stop-before-publish decision
