# Claude Code Plugin Marketplace

A test project for building a basic plugin marketplace for Claude Code.

## Goals

- Browse and discover Claude Code plugins
- Install/uninstall plugins
- View plugin details, descriptions, and usage info

## Structure

```
plugin-test/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace registry
└── plugins/
    └── matt-test/
        ├── .claude-plugin/
        │   └── plugin.json       # Plugin manifest
        ├── skills/
        │   └── greet/
        │       └── SKILL.md      # Greeting skill
        ├── commands/
        │   └── hello.md          # Hello command
        └── agents/
            └── helper.md         # Helper agent
```

## Usage

**Add the marketplace locally:**
```
/plugin marketplace add ./plugin-test
```

**Install a plugin:**
```
/plugin install matt-test@plugin-test
```

**Use the hello command:**
```
/matt-test:hello World
```

**Test locally with --plugin-dir:**
```bash
claude --plugin-dir ./plugins/matt-test
```

## Status

Early prototype / testing phase.
