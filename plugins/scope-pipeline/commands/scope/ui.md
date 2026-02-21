---
description: Create ASCII wireframes from planning documents
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-ui agent to visualize UI/UX layouts from planning documents.

This agent will:

1. Read all documentation in `.claude/scope/{feature-name}/` starting with `plan.md`
2. Identify all pages, views, modals, and components described in the plan
3. Create detailed ASCII wireframes for each UI element
4. Document component states (loading, empty, error, populated)
5. Include responsive layouts for mobile-first features
6. Add specifications for colors, typography, and spacing
7. Save the wireframes to `.claude/scope/{feature-name}/wireframes.md`

Use this command when:

- You have completed the `/scope:plan` phase and want to visualize the UI
- You need to review layouts before creating implementation tasks
- You want a visual reference for developers during implementation
- You need to validate UI decisions before coding begins

The agent creates comprehensive wireframe documents using ASCII art that clearly show:
- Page layouts and component placement
- Interactive elements and user flows
- Empty, loading, and error states
- Mobile and tablet responsive variations
- Accessibility considerations

The agent adapts wireframes to match the project's UI framework and component library patterns.

**Recommended workflow**:
1. `/scope:plan` - Create the implementation plan
2. `/scope:ui` - Visualize the UI/UX layouts
3. `/scope:task` - Break down into implementation tasks
4. `/scope:exec` - Execute the implementation

$ARGUMENTS
