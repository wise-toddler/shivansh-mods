# shivansh-mods

A Claude Code plugin marketplace. Each plugin lives in its own repo, linked here as a git submodule: plugins in `plugins/`, other tools in `tools/`.

| Plugin | What it does |
|---|---|
| [anti-hung](https://github.com/wise-toddler/anti-hung) | Sends `continue` when the network comes back after a turn died, and compacts then continues when the context is full |
| [pin-note](https://github.com/wise-toddler/pin-note) | Pins notes above the input that stay put while the chat scrolls; the agent keeps them, with numbered points you answer a few at a time |
| [zsh-guard](https://github.com/wise-toddler/zsh-guard) | Blocks Bash tool commands that rely on bash word splitting, which zsh does not do |

## Other tools

Also linked as submodules. Each one installs the way its own README says; mcp-cli also ships its skill as a plugin (`mcp-cli@shivansh-mods`), while the `mcp-call` CLI itself comes from `pipx install mcp-cli-skill`.

| Tool | What it does |
|---|---|
| [mcp-cli-skill](https://github.com/wise-toddler/mcp-cli-skill) | `mcp-call`: call any MCP server's tools from the shell, plus a skill that teaches Claude to use it |
| [slack-pat-mcp](https://github.com/wise-toddler/slack-pat-mcp) | MCP server for your own Slack account with a user token (xoxp): channels, DMs, search, drafts, canvases |
| [browser-manage](https://github.com/wise-toddler/browser-manage) | Chrome/Edge extension and MCP server to manage tabs and drive pages from Claude |

## Install

```
/plugin marketplace add wise-toddler/shivansh-mods
/plugin install anti-hung@shivansh-mods
/plugin install pin-note@shivansh-mods
/plugin install zsh-guard@shivansh-mods
/plugin install mcp-cli@shivansh-mods   # skill only; pipx install mcp-cli-skill for the CLI
```

## Working on it

```
git clone --recurse-submodules https://github.com/wise-toddler/shivansh-mods
```

Change a plugin inside `plugins/<name>`, commit and push there, then commit the new submodule commit here.
