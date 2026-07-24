# Furnace MCP

Official [Model Context Protocol](https://modelcontextprotocol.io) server for [Furnace](https://getfurnace.io) — outbound email campaigns, inbox, leads, and mailboxes.

## Connect in Cursor

Add to `~/.cursor/mcp.json` (or project `.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "furnace": {
      "url": "https://mcp.getfurnace.io/mcp"
    }
  }
}
```

For the internal dogfood environment:

```json
{
  "mcpServers": {
    "furnace-dev": {
      "url": "https://mcp-dev.getfurnace.io/mcp"
    }
  }
}
```

Then open **Settings → Tools & MCP → Connect** on the Furnace server and approve workspace access in the browser.

## Auth

- **OAuth (recommended):** user-scoped, multi-account. Call `listAccounts` first when multiple workspaces are granted, then pass `account_id` on tools.
- **API keys (`f_…`):** account-pinned automation via `Authorization: Bearer f_…` header.

## What you can do

- List and manage campaigns, leads, and lead lists
- Read threads and messages; queue replies and forwards
- Manage mailboxes, tags, and block lists
- Launch, pause, resume, and stop campaigns

## Links

- Product: https://getfurnace.io
- API docs: https://api.getfurnace.io/docs
