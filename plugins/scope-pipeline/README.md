# Scope Pipeline

A structured feature development pipeline for Claude Code. Plan, design, and implement features through a systematic multi-phase workflow.

## What It Does

Scope Pipeline provides 11 slash commands and 11 specialized agents that guide you through a complete feature development lifecycle:

```
.claude/scope/{feature-name}/
├── requirements.md  # Gathered requirements from interview
├── brainstorm.md    # Ideas and approach exploration
├── plan.md          # Implementation strategy
├── schema.md        # Database design
├── api-spec.md      # API contracts
├── wireframes.md    # UI layouts (ASCII)
├── edge-cases.md    # Failure scenarios + solutions
├── test-plan.md     # Test strategy + scripts
└── tasks.md         # Phased implementation tasks
```

## Commands

| Command | Description |
|---------|-------------|
| `/scope:interview` | Gather requirements through structured interview questions |
| `/scope:brainstorm` | Explore ideas and approaches before committing to a plan |
| `/scope:plan` | Create a detailed implementation plan |
| `/scope:db` | Design database schema with tables, indexes, migrations |
| `/scope:api` | Design REST API endpoints with schemas and examples |
| `/scope:ui` | Create ASCII wireframes for all pages and components |
| `/scope:edge` | Identify edge cases across 8 categories with solutions |
| `/scope:test` | Create test plans with E2E, unit, and integration tests |
| `/scope:task` | Break plans into phased, atomic implementation tasks |
| `/scope:exec` | Execute the implementation phase by phase |
| `/scope:full` | Run the entire pipeline (all 7 planning phases) |

## Typical Workflow

### Full Pipeline (recommended for complex features)

```
/scope:interview my-feature-name   # Optional: gather requirements first
/scope:full my-feature-name        # Run all 7 planning phases
/scope:exec my-feature-name        # Execute the implementation
```

### Step-by-Step (for more control)

```
/scope:interview my-feature  # Optional: gather requirements
/scope:brainstorm my-feature # Optional: explore approaches
/scope:plan my-feature       # Create implementation plan
/scope:db my-feature         # Design database schema
/scope:api my-feature        # Design API endpoints
/scope:ui my-feature         # Create wireframes
/scope:edge my-feature       # Identify edge cases
/scope:test my-feature       # Create test plan
/scope:task my-feature       # Break into implementation tasks
/scope:exec my-feature       # Execute implementation
```

### Minimal Pipeline (for simpler features)

```
/scope:plan my-feature       # Plan it
/scope:task my-feature       # Break into tasks
/scope:exec my-feature       # Build it
```

## How It Works

Each command launches a specialized Opus-powered agent that:

1. **Reads project context** — CLAUDE.md, README, package.json, existing code
2. **Adapts to your stack** — discovers frameworks, patterns, conventions
3. **Produces structured documentation** — saved to `.claude/scope/{feature-name}/`
4. **Builds on prior phases** — each phase reads outputs from previous phases

The agents are project-agnostic. They work with any tech stack by discovering your project's patterns during their initial setup phase.

## Installation

### From Marketplace

```
/plugin marketplace add andrewex/claude-marketplace
/plugin install scope-pipeline@andrewex-marketplace
```

### Local Development

```
claude --plugin-dir ./plugins/scope-pipeline
```

## Project Compatibility

The pipeline works with any project. Each agent auto-discovers:

- **Language/Framework**: Node.js, Python, Go, Ruby, Rust, etc.
- **Database**: PostgreSQL, MySQL, SQLite, MongoDB, etc.
- **API Framework**: Express, Next.js, FastAPI, Rails, Django, etc.
- **UI Framework**: React, Vue, Svelte, Angular, etc.
- **CSS Framework**: Tailwind, Bootstrap, CSS Modules, etc.
- **Test Runner**: Jest, Vitest, Mocha, pytest, etc.
- **ORM/Client**: Prisma, Drizzle, SQLAlchemy, ActiveRecord, etc.

## Output Location

All planning documents are saved to:

```
{project-root}/.claude/scope/{feature-name}/
```

This directory is created automatically. Each phase adds its document to the same directory, building a comprehensive planning package.

## Resuming Work

The executor agent (`/scope:exec`) supports resume. If interrupted, run it again and it will:

1. Read the tasks.md file
2. Identify which phases are already marked complete
3. Continue from the next incomplete phase

## License

MIT
