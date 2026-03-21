---
name: memory-ops
description: Memory staging, promotion, pruning, and bucket-selection guidance for ROAMS. Use when Codex needs to decide whether new information should be promoted into long-term memory, where it belongs, when to defer it as a candidate, and when existing memory should be reviewed or pruned.
---

# Memory Ops

Keep long-term memory selective, durable, and reviewable.

## Workflow

1. Identify the new information or lesson being considered.
2. Decide whether it is temporary working context, a memory candidate, or durable long-term memory.
3. If it is only a candidate, stage it without promoting it yet.
4. If it is durable, choose the correct memory bucket.
5. Apply the promotion checklist before updating long-term memory.
6. Periodically review memory for stale, duplicate, or no-longer-useful entries.

## Memory Categories

- Temporary working context: task-local notes that belong in `.agent/PLANS.md` or a task artifact, not long-term memory.
- Candidate memory: potentially reusable signal that is not yet proven durable enough for promotion.
- Long-term memory: durable guidance that should persist across future work.

## Bucket Rules

Use `memory/style.md` for:

- stable preferences about how work should be done
- repeated workflow or communication preferences

Use `memory/decisions.md` for:

- project-level choices that affect future implementation
- concise rationale that prevents repeated debate

Use `memory/lessons.md` for:

- repeated success or failure patterns
- lessons that change future execution behavior

Use no long-term memory bucket when:

- the information is task-local
- the information is obvious from the code or docs
- the pattern has not repeated or is not clearly durable

## Promotion Checklist

Promote only if the information is:

- likely to matter again
- not already captured elsewhere
- specific enough to guide future behavior
- stable enough to remain useful
- short enough to stay reviewable

If any of those are unclear, stage it as a candidate instead of promoting it immediately.

## Pruning And Review Rules

- Remove stale entries that no longer reflect actual practice.
- Merge duplicate entries that express the same rule.
- Rewrite overly long entries into shorter operational guidance.
- Prefer deleting weak memory over keeping low-signal clutter.

## Feedback Loop

- A failed task can produce a candidate lesson before it produces a durable lesson.
- Repeated candidate patterns should be promoted when evidence becomes strong enough.
- If memory starts accumulating noise, tighten promotion rather than adding more buckets.
