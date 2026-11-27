# Poptin MCP Server

> Last updated: 2026-11 | Status: Stable | Maintained by: Poptin

## What It Does

Poptin hosts an MCP server for lead-capture and email marketing workflows: draft email campaigns, analyze popup and form performance, and build audience segments. The endpoint is `https://mcp.popt.in/mcp` (streamable HTTP); there is no npm package to install. Authentication uses OAuth and requires a Poptin account with MCP access.

## Quick Setup

### Cursor

```json
// .cursor/mcp.json
{
  "mcpServers": {
    "poptin": {
      "url": "https://mcp.popt.in/mcp"
    }
  }
}
```

### Claude Code

```bash
claude mcp add --transport http poptin https://mcp.popt.in/mcp
```

### Kimi Code

```markdown
<!-- AGENTS.md -->
## MCP Servers
- poptin: https://mcp.popt.in/mcp
```

## What You Can Do

- Draft and prepare email campaigns from lead-capture data
- Analyze popup and form performance
- Build audience segments for follow-up campaigns

## Requirements

- Hosted remote server: no local install and no published package
- OAuth sign-in with a Poptin account that has MCP access
- Paid plans may apply: https://www.poptin.com/pricing/
- Hosted entry is not an endorsement; review the vendor's data and billing terms before connecting an account

## Links

- [GitHub](https://github.com/Poptin-LTD/Poptin-MCP)
- [Documentation](https://developers.poptin.com/docs/mcp)
- [Website](https://www.poptin.com/)
- [Hosted MCP](https://mcp.popt.in/mcp)
