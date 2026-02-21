---
description: Execute feature implementation from completed scope plans
allowed-tools: [Read, Glob, Grep, Write, Edit, Bash, Task]
model: opus
---

Launch the scope-executor agent to systematically implement a feature based on its plan and task documents.

This agent will:

1. Read `.claude/scope/{feature-name}/plan.md` to understand the architecture
2. Read `.claude/scope/{feature-name}/tasks.md` for the task breakdown
3. Identify which phases are already complete (if resuming)
4. Execute each phase sequentially with thorough validation
5. Update tasks.md to mark phases complete as work progresses
6. Provide a final summary with any deviations or follow-up recommendations

Use this command when:

- You have completed `/scope:plan` and `/scope:task` for a feature
- You want to start implementing a planned feature
- You need to resume work on a partially completed feature
- You want systematic, phase-by-phase implementation with progress tracking

The agent executes phases in order, validates each phase before marking complete, and maintains accurate progress tracking in the task document for seamless resume capability.

$ARGUMENTS
