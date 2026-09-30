# Calcom MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Calcom via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-calcom`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.cal.com`
* Authentication: personal API key (per-user, keys start `cal_` / `cal_live_`)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `bookings` | list bookings | Autonomous Execution |
| `bookings` | filter by status | Autonomous Execution |
| `event-types` | list event types | Autonomous Execution |
| `create-booking` | Execute create-booking command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
