# Rachio MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Rachio via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-rachio`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `api.rach.io`
* Authentication: personal API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `person` | person info + controller ids | Autonomous Execution |
| `schedule` | current schedule on a controller | Autonomous Execution |
| `zone-start` | Execute zone-start command. | Autonomous Execution |
| `stop` | EMERGENCY OFF: closes all valves | Autonomous Execution |
| `device-on` | Execute device-on command. | Autonomous Execution |
| `device-off` | Execute device-off command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
