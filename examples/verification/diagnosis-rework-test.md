# Diagnosis And Rework Test

Use this exercise to validate the shared failure taxonomy and evidence-driven rework loop.

## Goal

Verify that ROAMS can classify a failed pass, produce a narrow rework handoff, and avoid a blind retry.

## Scenario

Assume the following sequence:

1. A task requested a README section linking to `docs/status.md`.
2. The implementation added the section, but the link points to `docs/stats.md`.
3. QA caught the broken link by checking the actual README text.
4. The next pass should correct only the incorrect path and then re-run the specific verification that proved the failure.

## What The Test Should Check

- failure classification
- root-cause hypothesis
- whether diagnosis mode is required
- whether research should re-trigger
- the narrower next step
- the expected re-validation

## Expected Output

The test should return:

- failure class
- root-cause hypothesis
- evidence
- owning role
- narrower next step
- expected re-validation

## Pass Criteria

- the failure is classified as narrowly as possible
- the root-cause note describes the likely underlying cause rather than the symptom alone
- the retry is narrower than the original implementation pass
- research is not re-triggered unless the failure points to a wrong assumption

## Common Failure Signals

- classifying every failure as implementation failure without evidence
- broad retry instructions instead of a narrow fix
- unnecessary research re-triggering
- no explicit re-validation step
