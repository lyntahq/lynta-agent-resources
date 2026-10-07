# Lynta public agent resources

This repository publishes Lynta's public information skill, agent guidance, and read-only MCP connection details for coding agents and assistants.

- `skills/lynta-public-info/SKILL.md` answers product, pricing, and integration questions using cited public pages.
- `mcp.json` connects to Lynta's public documentation MCP server at `https://lyntahq.com/mcp`.
- `AGENTS.md` describes the public product boundaries and links to current source material.
- `plugin.json` is the portable Agent Plugin manifest.

The MCP server can search and return published website pages. It cannot access customer projects or perform product actions. This repository does not contain the Lynta product source code.

## Install the skill

Browse the [Lynta public-information skill on skills.sh](https://skills.sh/lyntahq/lynta-agent-resources/lynta-public-info).

```sh
npx skills add lyntahq/lynta-agent-resources
```

## Sources

- [Developer resources](https://lyntahq.com/developers)
- [Public agent view](https://lyntahq.com/?mode=agent)
- [Full agent guide](https://lyntahq.com/llms.txt)
- [MCP server card](https://lyntahq.com/.well-known/mcp/server-card.json)
