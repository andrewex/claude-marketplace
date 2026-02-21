---
description: Create a detailed implementation plan for a feature, bug fix, or refactor
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-planner agent to analyze requirements and create comprehensive implementation plans.

This agent will:

1. Analyze your feature/fix requirements thoroughly
2. Research the existing codebase to understand current architecture
3. Create a detailed implementation plan with phases and tasks
4. Document database changes, API changes, and UI components needed
5. Identify edge cases, risks, and testing strategies
6. Save the plan to `.claude/scope/{feature-name}/plan.md`

Use this command when:

- You want to plan a new feature before implementing it
- You need to think through a bug fix strategy
- You're planning a refactor or architectural change
- You want documented implementation steps with file paths
- You need to identify risks and dependencies before coding

The agent creates structured plans that serve as reliable roadmaps for implementation, stored in the `.claude/scope/` directory for future reference.

$ARGUMENTS
