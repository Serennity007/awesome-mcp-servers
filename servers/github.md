# GitHub MCP Server

> Last updated: 2026 | Status: Archived (unmaintained) | Maintained by: None — Anthropic's reference server is retired; GitHub maintains the official replacement

## What It Does

The GitHub MCP server connects your AI assistant directly to the GitHub API. It can read repositories, browse issues and pull requests, search code, create branches, and manage your entire GitHub workflow — all through natural language. No more context-switching between your editor and the browser.

> ⚠️ **Deprecated:** Anthropic's `@modelcontextprotocol/server-github` reference server is archived and unmaintained — the Quick Setup below installs GitHub's official [github/github-mcp-server](https://github.com/github/github-mcp-server) instead.

## Quick Setup

### Cursor

```json
// .cursor/mcp.json
{
  "mcpServers": {
    "github": {
      "command": "docker",
      "args": ["run", "-i", "--rm", "-e", "GITHUB_PERSONAL_ACCESS_TOKEN", "ghcr.io/github/github-mcp-server"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_your_token_here"
      }
    }
  }
}
```

### Claude Code

```bash
claude mcp add github -e GITHUB_PERSONAL_ACCESS_TOKEN=ghp_your_token_here -- docker run -i --rm -e GITHUB_PERSONAL_ACCESS_TOKEN ghcr.io/github/github-mcp-server
```

### Kimi Code

```markdown
<!-- AGENTS.md -->
## MCP Servers
- github: docker run -i --rm -e GITHUB_PERSONAL_ACCESS_TOKEN ghcr.io/github/github-mcp-server
```

Set `GITHUB_PERSONAL_ACCESS_TOKEN` as an environment variable or in `config.toml`.

Prefer a hosted setup? GitHub also serves the official remote endpoint at `https://api.githubcopilot.com/mcp/` (streamable HTTP, OAuth or PAT) for clients that support remote MCP servers.

## What You Can Do

- List and search repositories, issues, and pull requests
- Read file contents from any branch
- Create issues and pull requests with natural language
- Search code across repositories
- Manage branches and review PR diffs

## Requirements

- Docker installed and running — the official image is public at `ghcr.io/github/github-mcp-server`
- A [GitHub Personal Access Token](https://github.com/settings/tokens) with appropriate scopes (`repo`, `read:org`, etc.) — not needed when using the remote server with OAuth

## Links

- [GitHub (official)](https://github.com/github/github-mcp-server)
- [Documentation](https://github.com/github/github-mcp-server/blob/main/README.md)
- [Archived reference source](https://github.com/modelcontextprotocol/servers-archived/tree/main/src/github)
- [Legacy npm package](https://www.npmjs.com/package/@modelcontextprotocol/server-github)
