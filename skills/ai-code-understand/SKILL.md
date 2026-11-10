---
name: ai-code-understand
description: "Quickly understand the purpose, scope, and behavior changes of the current code changes."
---
Analyze the current code changes.

The goal is to quickly understand what changed and why without reading every line.

Explain:

## Purpose

- What problem do these changes solve?
- Why were the changes made?
- What behavior or requirement do they implement?

## Before vs. After

- What was the previous behavior?
- What is the new behavior?
- What observable behavior changed?
- What behavior remains unchanged?

## Important Changes

For each important changed file, explain:

- Responsibility
- Why it changed
- Important class or method
- Whether it contains core logic or supporting code

## Summary

End with:

- What Changed
- Why It Changed
- Core Logic Location
- Important Assumptions

## Rules

- Do not explain code line by line
- Skip boilerplate
- Prioritize behavior over implementation details
- Use actual file, class, and method names when available
- Separate confirmed behavior from assumptions
- Do not invent requirements
- Keep the response concise