# Memory Promotion Test

Use this exercise to validate ROAMS memory staging and promotion behavior.

## Goal

Verify that ROAMS can distinguish:

- temporary working notes
- candidate memory
- durable long-term memory

## Scenario

Assume the following observations from recent work:

Unless noted otherwise, assume none of these observations are already present in long-term memory.

1. A one-time shell command was needed to inspect a file during a task.
2. A repeated pattern emerged that vague UI tasks go better when the theme is defined before component work starts.
3. A project-level choice was made to keep research Manager-owned until repeated evidence justifies a separate Researcher role.
4. A transient test failure occurred once because of a typo in a local file path.

## What The Test Should Check

- which observations should not be promoted at all
- which should be staged as candidates
- which should be promoted immediately
- which memory bucket each promoted item belongs in

## Expected Output

The test should return:

- per-item classification
- promote, stage, or discard decision
- target memory bucket when applicable
- brief rationale

## Pass Criteria

- temporary or one-off task noise is not promoted
- durable preferences and decisions are routed to the correct buckets
- repeated patterns can be promoted or staged based on durability
- the rationale is short and rule-based rather than ad hoc

## Common Failure Signals

- promoting one-off task details
- confusing decisions with lessons
- promoting weak patterns directly without enough evidence
- treating all useful information as long-term memory
