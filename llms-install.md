# Installing the Tubroom MCP server

Tubroom is a remote MCP server. There is nothing to clone, build or install, and it needs no API key or account.

Add this to the MCP settings file (for Cline: `cline_mcp_settings.json`):

```json
{
  "mcpServers": {
    "tubroom": {
      "type": "streamableHttp",
      "url": "https://tubroom.com/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

To confirm it works, call `search_tub_rooms` with `{"place": "Gatlinburg", "limit": 3}`. It returns three hotels with the exact room to book, the tub type, the check date and a tubroom.com link for each.

All four tools are read-only: search_tub_rooms, romantic_tub_rooms, get_hotel, list_places.
