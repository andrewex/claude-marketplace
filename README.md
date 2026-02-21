# Claude Marketplace

A collection of Claude Code plugins for structured development workflows.

## Plugins

| Plugin | Description |
|--------|-------------|
| [scope-pipeline](./plugins/scope-pipeline/) | A structured feature development pipeline — brainstorm, plan, design, test, and execute |

## Installation

### Add the Marketplace

```
/plugin marketplace add andrewex/claude-marketplace
```

### Install a Plugin

```
/plugin install scope-pipeline@andrewex
```

### Update Plugins

```
/plugin update scope-pipeline@andrewex
```

## Local Development

To test plugins locally without installing:

```
claude --plugin-dir ./plugins/scope-pipeline
```

## Creating New Plugins

Each plugin lives in its own directory under `plugins/` and follows the [Claude Code plugin format](https://code.claude.com/docs/en/discover-plugins):

```
plugins/my-plugin/
├── .claude-plugin/
│   └── plugin.json       # Plugin manifest
├── commands/              # Slash commands (.md files)
├── agents/                # Agent definitions (.md files)
├── README.md
├── LICENSE
└── CHANGELOG.md
```

After creating a plugin, add it to `.claude-plugin/marketplace.json` in the repo root.

## License

MIT
