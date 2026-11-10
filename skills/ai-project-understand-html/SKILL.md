---
name: ai-project-understand-html
description: Generate a concise HTML dashboard that explains what the current project does, how it is structured, how it works, and which files should be read first.
---

Analyze the current project and generate a single self-contained HTML project overview.

The goal is to help me quickly understand what this project does without reading the entire codebase.

Focus on:

**Purpose → Architecture → Flow → Reading Path**

## 1. Project Overview

Summarize:

- What this project does
- What problem it solves
- Who or what uses it
- Main inputs and outputs
- Primary use cases

Keep this concise.

Clearly distinguish confirmed information from assumptions.

## 2. Technology Stack

Identify:

- Programming languages
- Frameworks
- Runtime and platform
- Main libraries
- Database or storage
- External APIs or services
- Build and dependency tools

Only include technologies confirmed by the repository.

## 3. Project Structure

Show the important folders and modules.

For each important area, include:

- Folder or module name
- Responsibility
- Important files
- Relationship with other modules

Skip generated files, dependencies, build outputs, and boilerplate.

## 4. Architecture

Explain:

- Entry points
- Main layers or modules
- Core business logic
- Data access
- External integrations
- Configuration
- User interface or API layer

Create a simple visual architecture diagram in the HTML.

Also include the equivalent Mermaid source using actual module and component names when useful.

## 5. Main Execution Flow

Trace the most important end-to-end flow:

`Entry → Validation → Core Logic → Data / External System → Result`

Explain:

- Where execution starts
- Which components participate
- How data moves
- Where important decisions occur
- What result is produced

Focus on the most representative flow.

## 6. Core Features

For each main feature, show:

- What it does
- Where it is implemented
- Main entry point
- Important dependencies

## 7. External Dependencies

Identify important integrations such as:

- Databases
- APIs
- Authentication providers
- Message queues
- File systems
- Cloud services
- Other internal systems

Explain what each dependency is used for.

## 8. Configuration and Startup

Explain:

- How the application starts
- Important configuration files
- Required environment variables
- Runtime dependencies
- Build or run commands, if confirmed

Do not invent missing setup steps.

## 9. Recommended Reading Path

Recommend the minimum code-reading path.

For each item, show:

1. File, class, or module
2. Why I should read it
3. What I should understand
4. Suggested reading order

Prioritize entry points, core business logic, main flows, integrations, and configuration.

## 10. Unknowns and Assumptions

List information that cannot be confirmed.

For each item, explain:

- What is unknown
- Why it matters
- Where additional context may be required

Do not present assumptions as facts.

## 11. Final Summary

End with:

- Project Purpose
- Architecture
- Main Flow
- Core Module
- Read First
- Confidence: High / Medium / Low

## HTML Requirements

Generate one self-contained HTML file.

Requirements:

- Clean developer dashboard
- Responsive layout
- Light and dark theme support
- Clear project structure and architecture
- Collapsible sections where useful
- Visual architecture and execution flow
- Include equivalent Mermaid source
- No external dependencies
- No external images, scripts, fonts, or network requests
- Keep important information visible and easy to scan
- Prioritize content over decoration

## General Rules

- Do not explain code line by line
- Do not analyze every file equally
- Skip generated code and boilerplate
- Prioritize project purpose and behavior
- Use actual file, class, and module names
- Separate confirmed information from assumptions
- Do not invent business requirements
- Keep the dashboard concise and developer-oriented

The dashboard should let me answer these questions within a few minutes:

1. What does this project do?
2. Why does it exist?
3. How is it structured?
4. How does it work?
5. Where is the core logic?
6. Which external systems does it use?
7. Which files should I read first?