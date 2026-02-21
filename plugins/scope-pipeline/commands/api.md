---
description: Design API endpoints from planning documents
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Launch the scope-api agent to create comprehensive API specifications from planning documents.

This agent will:

1. Read all documentation in `.claude/scope/{feature-name}/` starting with `plan.md`
2. Identify all required API endpoints and operations
3. Design RESTful endpoints with proper HTTP methods
4. Create request/response schemas with type definitions
5. Document authentication and authorization requirements
6. Design server-side functions and route handlers
7. Include error handling and status codes
8. Add frontend usage examples
9. Save to `.claude/scope/{feature-name}/api-spec.md`

Use this command when:

- You have completed the `/scope-pipeline:plan` phase and need API design
- You need to understand endpoint requirements before implementation
- You want to design server-side functions for complex operations
- You need API documentation for frontend development

The agent creates comprehensive API documentation following REST best practices:
- Consistent URL patterns (kebab-case, plural nouns)
- Proper HTTP methods (GET, POST, PUT, PATCH, DELETE)
- Meaningful status codes (200, 201, 400, 401, 403, 404)
- Type-safe request/response schemas
- Frontend usage examples

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
