---
name: diagnosis-ops
description: Shared failure classification and rework guidance for ROAMS. Use when Codex needs to classify a failed pass, record a root-cause hypothesis, decide whether to re-trigger research, narrow the next step, and route work back with an evidence-driven rework handoff.
---

# Diagnosis Ops

Turn failed passes into narrower, better-informed retries.

## Workflow

1. Identify the failed pass and the evidence that proves it failed.
2. Classify the failure using the shared taxonomy.
3. Record the most likely root-cause hypothesis.
4. Decide whether the next step needs diagnosis mode.
5. Decide whether research should re-trigger.
6. Produce a rework handoff with one narrower next step.

## Failure Taxonomy

- `requirements_failure`
- `implementation_failure`
- `validation_failure`
- `design_failure`
- `wrong_assumption_failure`

Choose the narrowest class that best explains the failure.

## Diagnosis Mode Triggers

- repeated failures of the same class
- low confidence after a failed pass
- unclear root cause
- expanding scope during retries

## Rework Handoff

Return:

- failure class
- root-cause hypothesis
- evidence
- owning role
- narrower next step
- expected re-validation

## Rework Rules

- narrow the next pass instead of retrying broadly
- revisit research when the failure points to a wrong assumption
- change validation strategy when the failure is primarily validation-related
- keep the root-cause note short and revisable
