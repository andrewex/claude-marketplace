---
description: Create comprehensive test plans from planning documents
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-test agent to create comprehensive test plans from planning documents.

This agent will:

1. Read all documentation in `.claude/scope/{feature-name}/`
2. Analyze feature requirements, UI flows, and edge cases
3. Design test strategy with coverage goals
4. Create E2E test scenarios with step-by-step scripts
5. Outline unit and integration tests
6. Document accessibility test requirements
7. Define test data fixtures
8. Create acceptance criteria checklist
9. Save to `.claude/scope/{feature-name}/test-plan.md`

Use this command when:

- You have completed planning and want to define test coverage
- You need E2E test scripts for browser testing
- You want to define acceptance criteria before implementation
- You need to ensure edge cases are tested

The agent creates comprehensive test documentation including:
- Test strategy with coverage goals
- E2E scenarios with browser automation steps
- Unit test outlines for utilities and components
- Integration tests for API endpoints
- Accessibility testing checklist
- Test data fixtures and generation
- Acceptance criteria (P0, P1, P2)

**Recommended workflow**:
1. `/scope-pipeline:plan` - Create the implementation plan
2. `/scope-pipeline:db` - Design the database schema
3. `/scope-pipeline:api` - Design API endpoints
4. `/scope-pipeline:ui` - Visualize the UI/UX layouts
5. `/scope-pipeline:edge` - Identify edge cases
6. `/scope-pipeline:test` - Create test plan
7. `/scope-pipeline:task` - Break down into tasks
8. `/scope-pipeline:exec` - Execute implementation

$ARGUMENTS
