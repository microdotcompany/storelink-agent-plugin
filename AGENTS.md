# AGENTS.md

This repo is the Store.link plugin for Claude Code and for Codex/ChatGPT: one skill plus an MCP config pointing at `https://dashboard.store.link/mcp`. The MCP server itself lives in `microdotcompany/storelink-dashboard` (`server/src/modules/mcp/`).

## Layout

| Path                               | Read by                                                                                      |
| ---------------------------------- | -------------------------------------------------------------------------------------------- |
| `.claude-plugin/plugin.json`       | Claude Code and Anthropic's directory                                                        |
| `.claude-plugin/marketplace.json`  | Claude Code (also the ChatGPT desktop app)                                                   |
| `plugin.json`                      | Codex/ChatGPT (portable Agent Plugins manifest, OpenAI fields under `extensions.com.openai`) |
| `.agents/plugins/marketplace.json` | Codex                                                                                        |
| `.mcp.json`                        | Claude Code (`type: http`)                                                                   |
| `mcp.json`                         | Codex/ChatGPT (`type: streamable-http`, CIMD OAuth)                                          |
| `skills/storelink/`                | both                                                                                         |

## Rules

- No secrets, hooks, commands, agents or `userConfig`. OpenAI's directory rejects them and Claude's chat surfaces ignore them.
- No `.DS_Store` files, symlinks or submodules.
- The skill is provider-neutral: write "the assistant", never "Claude" or "ChatGPT". Keep `SKILL.md` under 300 lines.
- The tools describe themselves. The skill teaches workflow and domain (stores, the Product Sheet, live changes, customer emails, plan limits), not tool parameters. When a tool changes in the dashboard repo, check the recipes still match.
- Bump `version` in `.claude-plugin/plugin.json` and `plugin.json`, and `metadata.version` in `SKILL.md`, together. CI checks they match.

## Validate

```
claude plugin validate --strict .
```

To try the Codex install without touching your own config:

```
CODEX_HOME=$(mktemp -d) sh -c 'codex plugin marketplace add . && codex plugin add storelink@storelink && codex mcp list'
```
