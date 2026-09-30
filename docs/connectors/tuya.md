# Tuya MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Tuya via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-tuya`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `openapi.tuyaus.com`
* Authentication: Access ID + Access Secret pair via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | status check: fetch a cloud token | Autonomous Execution |
| `device` | read device information | Autonomous Execution |
| `status` | read data-point status | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `scene` | Execute scene command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
