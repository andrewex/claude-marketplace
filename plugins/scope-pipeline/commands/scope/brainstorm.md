---
description: Generate ideas and explore approaches before creating a plan
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-brainstorm agent to generate ideas and explore different approaches for a feature before committing to a plan.

This agent will:

1. Understand the feature concept or problem space
2. Research the existing codebase for relevant patterns and context
3. Generate multiple approaches with pros/cons analysis
4. Explore creative solutions and alternatives
5. Identify key decisions that need to be made
6. Suggest which approach(es) merit further planning
7. Save ideas to `.claude/scope/{feature-name}/brainstorm.md`

Use this command when:

- You have a vague feature idea and want to explore possibilities
- You want to compare different implementation approaches before committing
- You're not sure which direction to take with a feature
- You want creative input on solving a problem
- You want to document alternatives before making architectural decisions
- You need to present options to stakeholders

The agent creates a brainstorm document that serves as the foundation for informed planning decisions.

**Recommended workflow**:
1. `/scope:brainstorm` - Generate ideas and explore approaches (optional)
2. `/scope:plan` - Create the implementation plan
3. `/scope:ui` - Visualize the UI/UX layouts
4. `/scope:edge` - Identify edge cases and solutions
5. `/scope:task` - Break down into implementation tasks
6. `/scope:exec` - Execute the implementation

$ARGUMENTS
