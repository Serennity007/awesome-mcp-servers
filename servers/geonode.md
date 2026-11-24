# Geonode MCP Server

> Last updated: 2026-11 | Status: Beta | Maintained by: Geonode

## What It Does

Geonode is a hosted MCP server for web extraction, crawling, URL discovery and web search. The endpoint is `https://mcp.geonode.com/mcp` (streamable HTTP); there is no npm package to install. Limited keyless `extract` calls are available; an API key unlocks the full toolset, JavaScript rendering, country targeting and batch/crawl jobs.

## Quick Setup

### Cursor

```json
// .cursor/mcp.json
{
  "mcpServers": {
    "geonode": {
      "url": "https://mcp.geonode.com/mcp"
    }
  }
}
```

### Claude Code

```bash
claude mcp add --transport http geonode https://mcp.geonode.com/mcp
```

### Kimi Code

```markdown
<!-- AGENTS.md -->
## MCP Servers
- geonode: https://mcp.geonode.com/mcp
```

## What You Can Do

- Extract a page as Markdown or HTML, synchronously or as a polled job
- Discover a site's URLs (`map`), crawl a site and poll crawl status
- Run web searches and batch extractions
- Add JavaScript rendering, geo-targeting or custom headers with an API key

## Requirements

- Hosted remote server: no local install and no published package
- API key for the full toolset; keyless extraction is limited (5 requests/minute, 1 concurrent request, 100 MB/day, no JavaScript rendering or country targeting)
- An account and plan for API keys: https://app.geonode.com/signup

## Links

- [GitHub](https://github.com/geonodecom/mcp)
- [Documentation](https://docs.geonode.com)
- [Website](https://geonode.com/integrations/mcp)
- [Hosted MCP](https://mcp.geonode.com/mcp)
