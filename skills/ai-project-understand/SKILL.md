---
name: ai-project-understand
description: Quickly understand what the current project does, how it is structured, how it works, and which files should be read first.
---

Analyze the current project.

The goal is to help me quickly understand what this project does without reading the entire codebase.

Focus on:

**Purpose → Architecture → Flow → Reading Path**

## 1. Project Overview

Explain:

- What this project does
- What problem it solves
- Who or what uses it
- Its main inputs and outputs
- Its primary use cases

Keep this section concise.

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

Explain the important folders and modules.

For each important area, show:

- Folder or module name
- Responsibility
- Important files
- Relationship with other modules

Skip generated files, dependencies, build outputs, and boilerplate.

## 4. Architecture

Explain the overall architecture, including:

- Entry points
- Main layers or modules
- Core business logic
- Data access
- External integrations
- Configuration
- User interface or API layer

Create a concise Mermaid diagram showing the main architecture.

Use actual module, class, and component names when useful.

## 5. Main Execution Flow

Trace the most important end-to-end flow:

`Entry → Validation → Core Logic → Data / External System → Result`

Explain:

- Where execution starts
- Which components participate
- How data moves
- Where important decisions occur
- What result is produced

Focus on the most representative flow, not every possible path.

## 6. Core Features

List the project's main features.

For each feature, explain:

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

Recommend the minimum code-reading path for understanding the project.

For each item, show:

1. File, class, or module
2. Why I should read it
3. What I should understand
4. Suggested reading order

Prioritize:

- README and documentation
- Entry points
- Core business logic
- Main execution flow
- Important integrations
- Configuration

Skip files that provide little understanding value.

## 10. Unknowns and Assumptions

List anything that cannot be confirmed, such as:

- Missing business context
- Unclear module responsibilities
- Unknown external system behavior
- Missing configuration
- Undocumented runtime requirements

Do not present assumptions as facts.

## 11. Final Summary

End with:

### Project Purpose
One short explanation.

### Architecture
One short explanation.

### Main Flow
One short explanation.

### Core Module
The most important module or component.

### Read First
The first file or module I should inspect.

### Confidence
High / Medium / Low, with a brief reason.

## General Rules

- Do not explain code line by line
- Do not analyze every file equally
- Skip generated code and boilerplate
- Prioritize project purpose and behavior
- Use actual file, class, and module names
- Separate confirmed information from assumptions
- Do not invent business requirements
- Keep the response concise and developer-oriented

The result should let me answer these questions within a few minutes:

1. What does this project do?
2. Why does it exist?
3. How is it structured?
4. How does it work?
5. Where is the core logic?
6. Which external systems does it use?
7. Which files should I read first?