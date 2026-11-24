# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.1] - 2026-11-24

### Added

- **Geonode** — Hosted MCP server for web extraction, crawling, URL discovery and search (`https://mcp.geonode.com/mcp`; hosted-only, MIT server repo, API key for the full toolset)
- Web category index now covers web extraction; badges and the repo count move to 13 servers

### Verified

- Endpoint smoke test on 2026-11-24: `initialize` and `tools/list` returned HTTP 200 and 16 tools (`extract`, `job`, `jobs`, `statistics`, `batch`, `batch_status`, `cancel_batch`, `crawl`, `crawl_status`, `cancel_crawl`, `map`, `map_jobs`, `map_job`, `search`, `search_jobs`, `search_job`).
- Keyless access is rate-limited by the vendor; no account-backed tool was exercised. "Verified" means reachable and structurally checked, not an endorsement of a paid plan.

## [1.1.0] - 2026-11-24

### Added

- **Kleap** — Create, edit, and publish websites (`kleap-cli`, MIT)
- **ContextStream** — Shared project context for AI coding agents: code search, decisions, lessons, and plans (`@contextstream/mcp-server`, MIT)
- **Agent QA** — Author and run QA tests, then triage results (`agent-qa`, FSL-1.1-ALv2 source-available; linked only)
- `by-category/web.md` category index; the Web row in the README index now links to it
- The new-server issue template now lists the actual categories, and the `new-server` label exists

### Verified

- Kleap: hosted `https://kleap.co/api/mcp` answered `initialize` and `tools/list`; npm `kleap-cli@2.2.0` inspected.
- ContextStream: hosted `https://mcp.contextstream.io/mcp` returned an authentication challenge (reachable remote MCP endpoint); npm `@contextstream/mcp-server@1.0.96` inspected.
- Agent QA: npm `agent-qa@0.3.11` inspected, MCP stdio entry present; setup examples pinned to 0.3.11.
- Verification is HTTP / npm metadata level. No server was exercised against a live account, and "verified" means reachable and structurally checked, not an endorsement.

## [1.0.0] - 2026-08-17

### Added

- Initial release of Awesome MCP Servers
- 9 curated MCP server entries (all verified on npm):
  - **Filesystem** — Local file system access (`@modelcontextprotocol/server-filesystem`)
  - **GitHub** — Repository, issue, and PR management (`@modelcontextprotocol/server-github`)
  - **PostgreSQL** — Database querying and exploration (`@modelcontextprotocol/server-postgres`)
  - **Redis** — Cache and key-value operations (`@modelcontextprotocol/server-redis`)
  - **Web Search** — Brave Search integration (`@modelcontextprotocol/server-brave-search`)
  - **Memory** — Persistent knowledge graph (`@modelcontextprotocol/server-memory`)
  - **Puppeteer** — Browser automation (`@modelcontextprotocol/server-puppeteer`)
  - **Slack** — Workspace messaging (`@modelcontextprotocol/server-slack`)
  - **Context7** — Live library documentation (`@upstash/context7-mcp`)
- Quick Start guides for Cursor, Claude Code, and Kimi Code
- Category index pages:
  - [Development](by-category/development.md) — GitHub
  - [Databases](by-category/databases.md) — PostgreSQL, Redis
  - [Communication](by-category/communication.md) — Slack
- GitHub templates:
  - Issue template for suggesting new servers
  - PR template for adding servers
- CI workflow for markdown linting and structure validation
- MIT License
- Contributing guidelines
