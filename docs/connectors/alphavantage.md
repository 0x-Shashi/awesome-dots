# Alphavantage MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Alphavantage via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-alphavantage`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `www.alphavantage.co`
* Authentication: Alpha Vantage API key (per-user, alphavantage.co/support/#api-key; free tier 25 calls/day)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `quote` | latest quote | Autonomous Execution |
| `daily` | last 5 daily closes | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
