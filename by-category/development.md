# 🔧 Development

MCP servers for software development workflows — code, repos, and DevOps.

## Servers

| Server | Description | Package | Status |
|--------|-------------|---------|--------|
| [GitHub](../servers/github.md) | Repos, issues, PRs, and code search | `@modelcontextprotocol/server-github` | Stable |
| [ContextStream](../servers/contextstream.md) | Shared project context — code search plus decisions, lessons, and plans | `@contextstream/mcp-server` | Stable |

## Typical Workflows

### Code Review

1. **GitHub** — Fetch the PR diff and review comments
2. **Filesystem** — Read the changed files for full context
3. Write a review with specific, actionable feedback

### Issue Triage

1. **GitHub** — List open issues
2. **Memory** — Check if similar issues were resolved before
3. **GitHub** — Assign labels and priority

### Continuing Work Across Sessions

1. **ContextStream** — Search the indexed codebase for files relevant to the next change
2. **ContextStream** — Retrieve saved decisions and lessons that should guide the work
3. **GitHub** — Open or update the PR with that shared context

### Setting Up a New Project

1. **GitHub** — Create the repository
2. **Filesystem** — Scaffold the project structure
3. **GitHub** — Set up branch protection rules

## See Also

- [Databases](databases.md) — For data layer servers
- [Communication](communication.md) — For team collaboration
