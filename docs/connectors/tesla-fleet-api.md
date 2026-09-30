# Tesla Fleet Api MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Tesla Fleet Api via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-tesla-fleet-api`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `fleet-api.prd.na.vn.cloud.tesla.com`
* Authentication: provider OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `vehicles` | list vehicles | Autonomous Execution |
| `vehicle-data` | live state (charge, location, climate, doors) | Autonomous Execution |
| `vehicle-data` | Execute vehicle-data command. | Autonomous Execution |
| `wake` | wake a sleeping car (metered) | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
