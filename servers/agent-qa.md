# Agent QA MCP Server

> Last updated: 2026 | Status: Beta | Maintained by: Vostride

## What It Does

Agent QA is a self-improving QA agent for web and mobile applications. Its MCP server gives coding assistants tools to author and validate tests, start runs, and inspect results.

## Quick Setup

### Cursor

```json
{
  "mcpServers": {
    "agent-qa": {
      "command": "npx",
      "args": ["-y", "agent-qa@0.1.21", "mcp"]
    }
  }
}
```

### Claude Code

```bash
claude mcp add agent-qa -- npx -y agent-qa@0.1.21 mcp
```

### Kimi Code

```toml
[mcp_servers.agent-qa]
command = "npx"
args = ["-y", "agent-qa@0.1.21", "mcp"]
```

## What You Can Do

- Create and validate Agent QA tests and suites
- Queue test or suite runs
- Inspect run steps, logs, artifacts, and failure classifications

## Requirements

- Node.js 24 or newer
- An Agent QA project and configured model credentials for test execution
- Dashboard-backed tools need the Agent QA dashboard running

## Links

- [GitHub](https://github.com/vostride/agent-qa)
- [npm](https://www.npmjs.com/package/agent-qa)
- [Documentation](https://vostride.com/docs/agent-qa)
