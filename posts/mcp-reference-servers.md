# 7 free MCP reference servers to start with

*20 Nov 2026 · By Abu Daud, CMA · WhatsApp +966 57 561 5384*

The Model Context Protocol (MCP) lets Claude and other AI apps connect to tools and data. The official repo **[modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)** keeps 7 free reference servers. All are free and open source (Apache 2.0 for new contributions, MIT for existing code). Checked 20 Nov 2026: public, ~92k stars, not archived.

> **Read this first.** The repo says these are *reference implementations* for learning, **not production-ready**. Try them on test folders and test repos. Keep company or client finance data on servers you have vetted.

| # | Server | What it does | Price | Start command | Source |
|---|---|---|---|---|---|
| 1 | Filesystem | Read and write files, only inside folders you allow | Free | `npx -y @modelcontextprotocol/server-filesystem /path/to/allowed/files` | [src/filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) |
| 2 | Fetch | Fetches a web page and turns it into clean text for the AI | Free | `uvx mcp-server-fetch` | [src/fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) |
| 3 | Git | Read, search and work with a local Git repository | Free | `uvx mcp-server-git --repository path/to/repo` | [src/git](https://github.com/modelcontextprotocol/servers/tree/main/src/git) |
| 4 | Memory | Knowledge-graph memory that persists between chats | Free | `npx -y @modelcontextprotocol/server-memory` | [src/memory](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) |
| 5 | Time | Current time and time-zone conversion | Free | `uvx mcp-server-time` | [src/time](https://github.com/modelcontextprotocol/servers/tree/main/src/time) |
| 6 | Sequential Thinking | Step-by-step, reflective problem solving | Free | see README | [src/sequentialthinking](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking) |
| 7 | Everything | Test server with prompts, resources and tools (for builders) | Free | see README | [src/everything](https://github.com/modelcontextprotocol/servers/tree/main/src/everything) |

`npx` needs Node.js. `uvx` needs [uv](https://docs.astral.sh/uv/) (Python).

## Claude Desktop config example

Paste into `claude_desktop_config.json`, then fully quit and reopen Claude Desktop.

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/allowed/files"]
    },
    "time": {
      "command": "uvx",
      "args": ["mcp-server-time"]
    }
  }
}
```

On Windows the repo wraps `npx` with `cmd /c`, e.g. `"command": "cmd", "args": ["/c", "npx", "-y", "@modelcontextprotocol/server-memory"]`.

## 4 quick-start steps

1. **Pick one.** Start with Filesystem on a test folder.
2. **Add the config** above to Claude Desktop.
3. **Restart** Claude Desktop fully.
4. **Not prod.** Treat these as teaching code; vet anything that touches real data.

## What moved to the archive

Older servers such as GitHub, GitLab, Google Drive, PostgreSQL, SQLite, Slack, Puppeteer, Brave Search, Google Maps, Redis and Sentry now live in [servers-archived](https://github.com/modelcontextprotocol/servers-archived) and are no longer maintained there. Look for current servers in the official [MCP Registry](https://registry.modelcontextprotocol.io/).

## Sources

- [github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) README (checked 20 Nov 2026)
- [src/time README](https://github.com/modelcontextprotocol/servers/tree/main/src/time) (checked 20 Nov 2026)

Servers by the MCP project and its contributors. This page only links to them.

---
Free guide (PDF): [MCP Starter Guide](../freebies/MCP-Starter-Guide.pdf) · More free resources: [imdaud-freebies](https://github.com/daudcma3-debug/imdaud-freebies#readme)

*By Abu Daud, CMA · Finance & Accounting AI Agents and Automations · WhatsApp [+966 57 561 5384](https://wa.me/966575615384)*
