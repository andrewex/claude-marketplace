# Changelog

All notable changes to the Scope Pipeline plugin will be documented in this file.

## [1.0.0] - 2026-02-20

### Added
- Initial release of the Scope Pipeline plugin
- 11 slash commands: `interview`, `brainstorm`, `plan`, `db`, `api`, `ui`, `edge`, `test`, `task`, `exec`, `full`
- 11 specialized Opus agents: `scope-interview`, `scope-brainstorm`, `scope-plan`, `scope-full`, `scope-db`, `scope-api`, `scope-ui`, `scope-edge`, `scope-test`, `scope-task`, `scope-executor`
- Requirements-gathering interview agent (`/scope-pipeline:interview`)
- Full pipeline orchestrator agent (`/scope-pipeline:full`) that runs all 7 planning phases
- Implementation planner agent (`/scope-pipeline:plan`) for architecture and strategy
- Executor agent (`/scope-pipeline:exec`) with resume capability
- Project-agnostic design that auto-discovers tech stack and conventions
- Comprehensive README with usage examples
