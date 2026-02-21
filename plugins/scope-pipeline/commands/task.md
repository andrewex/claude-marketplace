---
description: Convert planning documents into actionable, phased task lists
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-task agent to transform planning documents into detailed, phased task breakdowns.

This agent will:

1. Read all documentation in `.claude/scope/{feature-name}/`
2. Analyze the feature's scope, requirements, and dependencies
3. Decompose the plan into atomic, actionable tasks (1-4 hours each)
4. Organize tasks into logical phases (Foundation, Backend, Frontend, Integration, Polish, Testing)
5. Create clear acceptance criteria for each task
6. Save the task list to `.claude/scope/{feature-name}/tasks.md`

Use this command when:

- You have completed the `/scope-pipeline:plan` phase for a feature
- You want to convert high-level plans into developer-ready tasks
- You need a structured implementation roadmap with checkboxes
- You're ready to start implementation and want organized work items

The agent creates phased task lists that developers can follow step-by-step, with each phase ending in a completion marker task for tracking progress.

$ARGUMENTS
