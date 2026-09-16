# ContextStream MCP Server

> Last updated: 2026 | Status: Stable | Maintained by: ContextStream

## What It Does

ContextStream is a hosted MCP that gives AI coding agents shared project context across sessions and tools. It pairs millisecond code search with saved decisions, lessons, and plans so agents can pick up work with the right files and rationale instead of starting from scratch.

## Quick Setup

### Cursor (hosted)

```json
// .cursor/mcp.json
{
  "mcpServers": {
    "contextstream": {
      "url": "https://mcp.contextstream.io/mcp"
    }
  }
}
```

### Cursor / Claude Code (local launcher)

```bash
npx -y @contextstream/mcp-server@latest setup
```

Or install via shell:

```bash
curl -fsSL https://contextstream.io/mcp/install.sh | sh
```

### Claude Code

```bash
claude mcp add --transport http contextstream https://mcp.contextstream.io/mcp
```

### Kimi Code

```markdown
<!-- AGENTS.md -->
## MCP Servers
- contextstream: hosted at https://mcp.contextstream.io/mcp (or run `npx -y @contextstream/mcp-server@latest setup`)
```

## What You Can Do

- Search your indexed codebase and cite sources for the next change
- Retrieve saved project decisions that should guide implementation
- Capture lessons and plans so later sessions stay aligned
- Share context across Cursor, Claude Code, Codex, and other MCP clients

## Requirements

- An MCP client (Cursor, Claude Code, Kimi Code, or compatible)
- Free ContextStream account (created during MCP onboarding; no credit card required)
- For local launcher: Node.js 20+ or the native install script
- For hosted-only: a client that supports Streamable HTTP / OAuth

## Links

- [GitHub](https://github.com/contextstream/mcp-server)
- [npm](https://www.npmjs.com/package/@contextstream/mcp-server)
- [Documentation](https://contextstream.io/docs/mcp)
- [Website](https://contextstream.io)
