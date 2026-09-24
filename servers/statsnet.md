# Statsnet MCP Server

> Last updated: 2026 | Status: Stable | Maintained by: usenetstate

## What It Does

Background check any company in the world: registration, executives, courts and finances.

Remote endpoint: `https://statsnet.co/mcp`  
Registry: `io.github.usenetstate/statsnet`  
Website: https://statsnet.co

## Quick Setup

### Cursor

```json
// .cursor/mcp.json
{
  "mcpServers": {
    "statsnet": {
      "url": "https://statsnet.co/mcp"
    }
  }
}
```

### Claude Code

```bash
claude mcp add --transport http statsnet https://statsnet.co/mcp
```

## Links

- Repo: https://github.com/usenetstate/statsnet-mcp
- Remote MCP: https://statsnet.co/mcp
