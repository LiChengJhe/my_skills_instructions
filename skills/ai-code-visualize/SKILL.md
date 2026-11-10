---
name: ai-code-visualize
description: Visualize the main execution flow of the current code changes using a concise Mermaid diagram.
disable-model-invocation: true
---
Analyze the main execution flow of the current code changes.

Identify:

- Entry point
- Input and validation
- Core business logic
- Important decision branches
- Internal dependencies
- Database or data access
- External APIs or systems
- Final result
- Important failure paths

Create a Mermaid flowchart showing the main execution flow.

## Mermaid Requirements

- Keep the diagram simple
- Focus on important paths only
- Use actual class and method names when useful
- Show important decision branches
- Show database and external system interactions
- Skip boilerplate
- Avoid unnecessary implementation details

After the Mermaid diagram, briefly explain each important step.

For each step, show:

- File and method
- Responsibility
- Input and output
- Important side effects

End with:

- Entry Point
- Core Logic Location
- Main Dependency
- Final Result

## Rules

- Do not explain code line by line
- Do not create a full system architecture diagram
- Focus only on the current changes
- Do not invent behavior that cannot be confirmed
- Keep the response concise