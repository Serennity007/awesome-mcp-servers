# Kleap MCP Server

> Last updated: 2026 | Status: Stable | Maintained by: Kleap

## What It Does

Kleap is an MCP server for creating, editing, and publishing websites. The same server is available as a local stdio process via npm (`kleap-cli`) and as a hosted endpoint at `https://kleap.co/api/mcp` (OAuth, 34 tools).

## Quick Setup

### Cursor

```json
// .cursor/mcp.json
{
  "mcpServers": {
    "kleap": {
      "command": "npx",
      "args": ["-y", "kleap-cli"]
    }
  }
}
```

Hosted alternative: add URL `https://kleap.co/api/mcp` and sign in with OAuth.

### Claude Code

```bash
claude mcp add kleap -- npx -y kleap-cli
```

### Kimi Code

```markdown
<!-- AGENTS.md -->
## MCP Servers
- kleap: npx -y kleap-cli
```

## What You Can Do

- Create a site from a short prompt
- Edit an existing Kleap app
- Publish a site
- Check publish status by id, slug, or domain

## Requirements

- Node.js 18+
- A Kleap account (`npx -y kleap-cli auth login`, or OAuth on the hosted URL)

## Links

- [GitHub](https://github.com/kleaphq/cli)
- [npm](https://www.npmjs.com/package/kleap-cli)
- [Documentation](https://kleap.co/mcp)
- [Hosted MCP](https://kleap.co/api/mcp)
