---
description: Design database schema from planning documents
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-db agent to create comprehensive database schema designs from planning documents.

This agent will:

1. Read all documentation in `.claude/scope/{feature-name}/` starting with `plan.md`
2. Identify all data entities, relationships, and business rules
3. Design normalized table structures with proper types
4. Create ASCII Entity Relationship Diagrams (ERD)
5. Design access control policies
6. Plan indexes for query performance
7. Write migration scripts
8. Document common query patterns
9. Save to `.claude/scope/{feature-name}/schema.md`

Use this command when:

- You have completed the `/scope-pipeline:plan` phase and need database design
- You need to understand data requirements before implementation
- You want to ensure proper access control policies
- You need migration scripts ready for implementation

The agent creates comprehensive schema documentation following database best practices:
- Proper primary keys and foreign key constraints
- Access control policies for data isolation
- Performance indexes
- Migration scripts using the project's migration tooling

**Recommended workflow**:
1. `/scope-pipeline:plan` - Create the implementation plan
2. `/scope-pipeline:db` - Design the database schema
3. `/scope-pipeline:ui` - Visualize the UI/UX layouts
4. `/scope-pipeline:api` - Design API endpoints
5. `/scope-pipeline:edge` - Identify edge cases
6. `/scope-pipeline:test` - Create test plan
7. `/scope-pipeline:task` - Break down into tasks
8. `/scope-pipeline:exec` - Execute implementation

$ARGUMENTS
