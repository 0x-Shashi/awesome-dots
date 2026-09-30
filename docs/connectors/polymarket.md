# Polymarket MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Polymarket via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-polymarket`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `gamma-api.polymarket.com`
* Authentication: none, public API

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `markets` | list markets | Autonomous Execution |
| `markets` | search markets | Autonomous Execution |
| `markets` | active, sorted by 24h volume | Autonomous Execution |
| `market-get` | one market by condition id | Autonomous Execution |
| `market-get` | one market by slug | Autonomous Execution |
| `prices` | price history | Autonomous Execution |
| `orderbook` | public order-book snapshot | Autonomous Execution |
| `events` | list events | Autonomous Execution |
| `events` | one event by slug | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
