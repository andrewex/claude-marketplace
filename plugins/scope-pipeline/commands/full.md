---
description: Run the complete scope pipeline to create all planning documents for a feature
allowed-tools: [Read, Glob, Grep, Write, Task]
model: opus
---

Run the complete scope pipeline to create all planning documents for a feature.

Execute all 7 scope phases in sequence:

1. **Plan** (`plan.md`) - High-level implementation plan
2. **Database** (`schema.md`) - Database schema with tables, policies, migrations
3. **API** (`api-spec.md`) - API endpoints, schemas, server functions
4. **UI** (`wireframes.md`) - ASCII wireframes for all pages/views
5. **Edge Cases** (`edge-cases.md`) - Failure scenarios with solutions
6. **Tests** (`test-plan.md`) - E2E scenarios, unit tests, acceptance criteria
7. **Tasks** (`tasks.md`) - Phased implementation task breakdown

All documents are saved to `.claude/scope/{feature-name}/`.

Use this command when:

- You want to fully plan a feature before implementation
- You need comprehensive documentation for a complex feature
- You want all planning artifacts created in one session
- You're starting a major new feature or module

The pipeline creates a complete planning package:
```
.claude/scope/{feature-name}/
├── plan.md          # Implementation strategy
├── schema.md        # Database design
├── api-spec.md      # API contracts
├── wireframes.md    # UI layouts
├── edge-cases.md    # Error scenarios
├── test-plan.md     # Test strategy
└── tasks.md         # Implementation tasks
```

After completion, run `/scope-pipeline:exec {feature-name}` to begin implementation.

**Individual commands** (if you prefer to run phases separately):
- `/scope-pipeline:plan` - Just the implementation plan
- `/scope-pipeline:db` - Just the database schema
- `/scope-pipeline:api` - Just the API specification
- `/scope-pipeline:ui` - Just the wireframes
- `/scope-pipeline:edge` - Just the edge cases
- `/scope-pipeline:test` - Just the test plan
- `/scope-pipeline:task` - Just the task breakdown

$ARGUMENTS
