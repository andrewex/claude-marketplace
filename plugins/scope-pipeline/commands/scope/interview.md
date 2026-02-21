---
description: Interview the user to gather requirements before planning a feature
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-interview agent to conduct a structured requirements-gathering interview before planning.

This agent will:

1. Understand the high-level feature concept from the user
2. Explore the existing codebase to inform follow-up questions
3. Ask targeted questions across key dimensions (users, data, UI, integrations, constraints)
4. Synthesize answers into a structured requirements document
5. Identify ambiguities and get clarification
6. Save the requirements to `.claude/scope/{feature-name}/requirements.md`

Use this command when:

- You have a feature idea but haven't fully fleshed out the requirements
- You want to ensure nothing is missed before planning begins
- You're working with a stakeholder who needs guided questions
- You want a documented requirements baseline to plan against
- The feature is complex and touches multiple parts of the system

The agent produces a structured requirements document that feeds directly into `/scope:plan`.

**Recommended workflow**:
1. `/scope:interview` - Gather and document requirements
2. `/scope:brainstorm` - Explore approaches (optional)
3. `/scope:plan` - Create the implementation plan
4. `/scope:full` or individual phases - Complete the pipeline

$ARGUMENTS
