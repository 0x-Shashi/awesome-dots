# Calendly MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Calendly via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-calendly`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.calendly.com`
* Authentication: OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token, shows your user URI | Autonomous Execution |
| `scheduled-events` | Execute scheduled-events command. | Autonomous Execution |
| `event-types` | Execute event-types command. | Autonomous Execution |
| `invitees` | invitees for one event | Supervised Execution |
| `availability` | Execute availability command. | Autonomous Execution |
| `cancel` | Execute cancel command. | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
