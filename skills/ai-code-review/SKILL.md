---
name: ai-code-review
description: "Quickly understand and verify AI-generated code changes by analyzing behavior, execution flow, risks, and the minimum code requiring human review."
---
Analyze the current code changes.

The goal is to help me quickly understand and verify AI-generated code without reading every line.

Focus on:

**Understand → Visualize → Verify**

## 1. Overview

Summarize:

- What problem these changes solve
- Why the changes were made
- What changed
- Overall implementation approach

Keep this concise.

## 2. Before vs. After

Explain:

- Previous behavior
- New behavior
- Important observable behavior changes

Clearly distinguish confirmed behavior from assumptions.

Do not invent behavior that cannot be confirmed from the code.

## 3. Execution Flow

Identify:

- Entry point
- Core business logic
- Important decision branches
- Dependencies
- Database or data access
- External APIs or systems
- Final result

Create a Mermaid flowchart showing the main execution flow.

Requirements:

- Keep the diagram simple
- Focus on important paths
- Use actual class and method names when useful
- Show important decision branches
- Show database or external API interactions
- Skip boilerplate

After the diagram, briefly explain the important steps.

## 4. Changed Files

For each important changed file, show:

- File name
- Responsibility
- Why it changed
- Important methods
- Category

Classify files as:

- Core Logic
- Integration / Data Access
- Supporting Code
- Boilerplate

Prioritize Core Logic and Integration / Data Access.

De-emphasize boilerplate.

## 5. Risk Review

Identify meaningful risks involving:

- Business logic assumptions
- Behavior changes
- Data mutations
- External dependencies
- Error handling
- Security / permissions
- Concurrency
- Compatibility

Classify each risk as:

- High
- Medium
- Low

For each risk explain:

- Where it exists
- Why it matters
- What I should verify

Do not generate theoretical risks unrelated to the changes.

## 6. Minimum Reading Path

Recommend the minimum code I should personally read.

For each item show:

1. File and method
2. Why I should read it
3. What I should verify
4. Risk level

Prioritize High-risk business logic.

Skip files that provide little review value.

## 7. Verification Checklist

Create a concise checklist of what I should verify before accepting the changes.

Focus on:

- Business requirements
- Main logic
- Decision branches
- Data changes
- Error scenarios
- External dependencies
- Compatibility
- High-risk assumptions

## 8. Final Summary

End with:

### What Changed
One short explanation.

### How It Works
One short explanation.

### Highest Risk
The most important thing requiring human verification.

### Read First
The first file and method I should inspect.

### Confidence
High / Medium / Low, with a brief reason.

## General Rules

- Do not explain code line by line
- Skip boilerplate
- Prioritize behavior and business logic
- Prioritize high-risk areas
- Use actual file, class, and method names when available
- Separate confirmed behavior from assumptions
- Do not invent requirements
- Do not assume the implementation is correct
- Keep the response concise and developer-oriented

The review should let me answer these questions within a few minutes:

1. What changed?
2. Why did it change?
3. How does it work?
4. Where is the important code?
5. What could be wrong?
6. What code do I actually need to read?
7. What should I verify before accepting it?