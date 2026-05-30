# claude-docs

A Claude Code plugin that adds a **`claude-docs`** expert subagent. It answers questions about
Claude Code and the Claude Agent SDK (hooks, MCP, subagents, slash commands, settings, plugins,
CLI flags, env vars, …) grounded in the **official online documentation** at
[code.claude.com/docs](https://code.claude.com/docs).

No docs are stored locally — the agent reads the live site on demand, so answers are always current.

## Install

In any Claude Code session (CLI, desktop app):

```
/plugin marketplace add SlaVinci/claude-docs
/plugin install claude-docs@slavinci
```

Restart the session, then use it:

```
@claude-docs how do PreToolUse hooks work?
```

Or just ask a Claude Code question and it will be delegated automatically.

### Web sessions

For Claude Code on the web, enable the plugin per-repository by committing a
`.claude/settings.json` to that repo that adds this marketplace and enables `claude-docs`.

## Update

```
/plugin marketplace update slavinci
```

## Uninstall

```
/plugin uninstall claude-docs@slavinci
```

## What's inside

```
.claude-plugin/marketplace.json          # marketplace catalog
plugins/claude-docs/
  ├── .claude-plugin/plugin.json          # plugin manifest
  └── agents/claude-docs.md               # the subagent (tools: WebFetch, WebSearch)
```
