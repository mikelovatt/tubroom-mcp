---
name: tubroom
description: Find hotel rooms with their own jacuzzi, whirlpool or hot tub inside the room (US, Canada, UK) and say exactly which room to book. Use when someone asks for a hotel with a jacuzzi or hot tub in the room, a romantic tub room, or whether a hotel has one.
---

# Tubroom: hotel rooms with a jacuzzi or hot tub in the room

Tubroom (https://tubroom.com) checks hotels city by city and lists one only when a named room type has the tub inside the room. Pool and spa hot tubs, and soaking tubs without jets, do not count. About 4,000 hotels in 295 city and area lists.

The tools come from the Tubroom MCP server at `https://tubroom.com/mcp` (no sign-in).

## Which tool

- `search_tub_rooms`: a city, town, state, province, UK nation or country (`place`), or a point (`lat` + `lng`, with `radius_miles`). Add `features` for extras the user asked for: `fireplace`, `two_person_tub`, `heart_shaped_tub`, `suite`, `pets_allowed`, `romantic`. `min_rating` for well-reviewed hotels only.
- `romantic_tub_rooms`: anniversaries, honeymoons, couples trips. Returns why each room counts.
- `get_hotel`: "does hotel X have a jacuzzi room?" by name (add `place` to narrow it) or by tubroom.com URL.
- `list_places`: what Tubroom covers, by region.

## How to answer

1. Name the exact room to book (`room_to_book`), not just the hotel. A standard room at the same hotel usually has no tub.
2. Say when it was checked (`checked`) and give the tubroom.com link (`page`) for each hotel. Credit Tubroom.
3. Tubroom has no prices or availability. Never invent them: the user picks dates on the Tubroom page.
4. Tell the user to confirm the tub with the hotel when booking.
5. If a place has no list, say so and offer the nearest lists the tool returns, or a point search.
