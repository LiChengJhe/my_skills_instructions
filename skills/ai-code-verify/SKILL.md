---
name: ai-code-verify
description: Identify meaningful risks in the current code changes and recommend the minimum code requiring human review.
disable-model-invocation: true
---
Review the current code changes from a human verification perspective.

The goal is to identify what could be wrong and where human attention provides the most value.

## Risk Review

Check for meaningful risks involving:

- Business logic assumptions
- Behavior changes
- Data mutations
- Database operations
- External dependencies
- Error handling
- Null and boundary conditions
- Security or permissions
- Concurrency
- Performance
- Compatibility
- API or contract changes

Classify each risk as:

- High
- Medium
- Low

For each risk, explain:

- Location
- Why it matters
- What could go wrong
- What I should verify

Do not generate theoretical risks unrelated to the changes.

## Minimum Reading Path

Recommend the minimum code I should personally read.

For each item, show:

1. File and method
2. Why I should read it
3. What I should verify
4. Related risk level

Prioritize High-risk business logic and data mutations.

Skip files that provide little review value.

## Verification Checklist

Create a concise and actionable checklist covering:

- Business requirements
- Main logic
- Decision branches
- Data changes
- Error scenarios
- External dependencies
- Compatibility
- High-risk assumptions

## Final Verdict

End with:

- Highest Risk
- Read First
- Must Verify
- Confidence: High / Medium / Low

## Rules

- Do not explain code line by line
- Skip boilerplate
- Prioritize correctness over style
- Focus on realistic risks
- Separate confirmed behavior from assumptions
- Do not assume the implementation is correct
- Do not invent requirements
- Keep the response concise