---
name: eval-retrospective
description: Post-verification retrospective and process-evaluation guidance for ROAMS. Use when Codex needs to compare intended plan versus actual execution, identify process misses, and recommend whether framework, skill, verification, or roadmap changes are warranted.
---

# Eval Retrospective

Retrospective is a required gate after verification and before closure or publish readiness.

## Workflow

1. Compare the intended plan with the actual execution path.
2. Inspect failures, rework cycles, user corrections, manual nudges, and missed gates.
3. Identify where skills, prompts, checklists, role rules, or verification coverage were insufficient.
4. Use the narrowest applicable failure class when the miss is best explained as a requirements, implementation, validation, design, or wrong-assumption failure.
5. Decide whether the remedy belongs in memory, a shared skill, a local skill, verification coverage, or roadmap refinement.
6. Return a clear recommendation state.

## Recommendation States

- no framework change
- candidate improvement
- required skill or process update

## Review Rules

- Evaluate the process even when the code outcome is correct.
- Treat repeated user nudges as evidence, not as noise.
- Prefer the smallest durable process correction.
- Keep the output decision-ready for the Manager.

## Required Outputs

- comparison of plan versus execution
- process findings
- failure class when applicable
- recommended remedy location
- recommendation state
