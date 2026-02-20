# mcp-transitous

MCP server for global public transport routing via [Transitous](https://transitous.org) —
a community-run, open-source transit routing service based on GTFS data.

> **Status: Work in Progress** — Server scaffolding is in place. Tools are not yet implemented.

---

## Prerequisites

- [Bun](https://bun.sh) runtime (`curl -fsSL https://bun.sh/install | bash`)
- No API keys needed — Transitous is free and open

---

## Planned Tools

- `transitous_search_stops` — Search for transit stops worldwide by name
- `transitous_get_routes` — Plan a transit journey between two stops
- `transitous_get_departures` — Get upcoming departures from a stop

---

## Data Source

[Transitous](https://transitous.org) is an open-source project that aggregates GTFS (General
Transit Feed Specification) data from public transit agencies worldwide. It runs an instance
of MOTIS, an open-source transit routing engine. No registration required.

---

## Install

```bash
git clone git@github.com:McCullonas/mcp-transitous.git
cd mcp-transitous
bun install
```

---

## MCP Client Configuration (once implemented)

```json
{
  "mcpServers": {
    "transitous": {
      "command": "bun",
      "args": ["run", "/path/to/mcp-transitous/src/index.ts"]
    }
  }
}
```

---

## Licence

MIT
