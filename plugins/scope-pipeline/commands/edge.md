---
description: Identify and document edge cases from planning documents
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-edge agent to analyze planning documents and identify all edge cases with proposed solutions.

This agent will:

1. Read all documentation in `.claude/scope/{feature-name}/` starting with `plan.md`
2. Systematically analyze 8 categories of edge cases:
   - Data edge cases (null values, boundaries, invalid formats)
   - User behavior (double-clicks, concurrent sessions, abandonment)
   - Timing (race conditions, timezone issues, expiration)
   - Network (connection loss, timeouts, retries)
   - Authorization (permission changes, token expiration)
   - Integration (third-party failures, webhook issues, API limits)
   - Business logic (calculations, state transitions, rounding)
   - Multi-tenancy (cross-tenant data, resource isolation)
3. Document each edge case with severity, likelihood, and impact
4. Propose specific solutions for handling each scenario
5. Create a priority matrix for implementation order
6. Generate a testing checklist for validation
7. Save to `.claude/scope/{feature-name}/edge-cases.md`

Use this command when:

- You have completed the `/scope-pipeline:plan` phase and want to ensure robustness
- You need to identify potential failure points before implementation
- You want to prioritize which edge cases to handle first
- You need a testing checklist for QA

The agent creates comprehensive edge case documentation that helps prevent bugs, improve error handling, and ensure a robust user experience.

**Recommended workflow**:
1. `/scope-pipeline:plan` - Create the implementation plan
2. `/scope-pipeline:ui` - Visualize the UI/UX layouts
3. `/scope-pipeline:edge` - Identify edge cases and solutions
4. `/scope-pipeline:task` - Break down into implementation tasks
5. `/scope-pipeline:exec` - Execute the implementation

$ARGUMENTS
