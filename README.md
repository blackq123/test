# test

This repo is set up to use [treg](https://github.com/superdesigndev/treg), a pay-per-call catalog of agent tools.

## What's configured

- `.mcp.json` registers treg's MCP server (`https://treg.to/mcp/`) for Claude Code in this project.
  No token is stored in the repo: when you first use it, run `/mcp` in Claude Code and connect with
  **OAuth** (pick your team on the consent screen).
- `.claude/settings.json` adds the `superdesigndev/treg` plugin marketplace and turns on the `treg`
  plugin, which provides the `treg:treg` skill.

## Optional: the CLI

```bash
curl -fsSL https://treg.to/install.sh | sh   # install the treg CLI
treg login                                   # sign in (opens a browser)
treg catalog search "backlinks for a domain"
treg balance
```

Don't commit treg tokens. If you'd rather use a header token than OAuth, run `treg mcp install`, which
writes it to your user-scope Claude Code config, outside this repo.
