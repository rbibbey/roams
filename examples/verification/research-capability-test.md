# Research Capability Test

Use this exercise to validate the Manager-owned research capability in isolation.

## Goal

Answer a focused technical question using canonical sources and distill the result into a compact Research Brief.

Question:

`What do official OpenAI sources say PLANS.md is for in Codex workflows, and when should it be used?`

## What The Capability Should Do

- identify the exact research question
- prefer official OpenAI sources
- avoid third-party summaries unless official sources are insufficient
- distinguish verified facts from inference
- return a short Research Brief that another role could use

## Expected Output

The research pass should return:

- question
- recommendation
- key findings
- sources
- constraints or caveats
- implementation impact
- open questions

## Pass Criteria

- official or canonical sources are used
- the brief is concise and decision-oriented
- verified findings are separated from inference
- the output is useful to the Manager or Coder without requiring raw source dumps

## Common Failure Signals

- relying on third-party summaries when official docs exist
- overlong notes instead of a distilled brief
- mixing verified facts with guesses
- no implementation impact section
