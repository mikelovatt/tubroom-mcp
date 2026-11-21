# Tubroom MCP server

[Tubroom](https://tubroom.com/?utm_source=github&utm_medium=readme) lists hotel rooms with their own jacuzzi, whirlpool or hot tub inside the room, city by city across the US, Canada and the UK. This is its remote MCP server: Claude, ChatGPT, Cursor, Gemini CLI, Cline or any MCP client can ask it which room to book.

**Server URL:** `https://tubroom.com/mcp` (Streamable HTTP, no account, no API key)

About 4,000 hotels in 295 city and area lists. Each listing names the exact room type with the tub, the source where it was confirmed (hotel website, chain site or booking site) and the date it was last checked. Pool and spa hot tubs, and soaking tubs without jets, do not count.

## Connect

- **Claude** (claude.ai, desktop): Settings, Connectors, Add custom connector. Paste `https://tubroom.com/mcp`.
- **ChatGPT**: developer mode on (Settings, Apps and connectors, Advanced), Create, paste `https://tubroom.com/mcp`, No authentication.
- **Claude Code**: `claude mcp add --transport http tubroom https://tubroom.com/mcp`
- **Cursor, Windsurf, VS Code**:
  ```json
  { "mcpServers": { "tubroom": { "url": "https://tubroom.com/mcp" } } }
  ```
- **Gemini CLI**: `gemini extensions install https://github.com/mikelovatt/tubroom-mcp`
- **Cline**: see [llms-install.md](llms-install.md).

## Tools

All four are read-only.

| Tool | What it returns |
|---|---|
| `search_tub_rooms` | Hotels with a jacuzzi, whirlpool or hot tub in the room in a city, town, state, province or UK nation, or near a lat/lng point. Filters: tub type, fireplace, tub for two, heart-shaped tub, suite, pets allowed, minimum rating. |
| `romantic_tub_rooms` | Romantic tub rooms (tub for two, fireplace in the room, heart-shaped tub, honeymoon room) with the reason each one counts. |
| `get_hotel` | One hotel by name or tubroom.com URL: the room with the tub, tub type, source and check date. Says plainly when a hotel is not listed. |
| `list_places` | Every city and area covered, with hotel counts by state, province or UK nation. |

Every answer links the hotel's Tubroom page, where you pick dates and check prices. The assistant cannot book.

Try: *"Hotels in Gatlinburg with a jacuzzi and a fireplace in the room"*, *"a romantic hot tub room in the Lake District"*, *"does the Hampton Inn Sevierville have a whirlpool room?"*

## Data

The same records as the site and the open dataset [hotels.json](https://tubroom.com/data/hotels.json) (CC BY 4.0). How tub rooms are checked: [tubroom.com/about](https://tubroom.com/about/?utm_source=github&utm_medium=readme). Setup page: [tubroom.com/mcp-server](https://tubroom.com/mcp-server/?utm_source=github&utm_medium=readme).

Official MCP Registry: `com.tubroom/tubroom`.

## About Tubroom

Tubroom is run by M&B Marketing SARL, France. Hotels cannot pay to be listed; booking buttons on tubroom.com are affiliate links. Contact: hello@tubroom.com.
