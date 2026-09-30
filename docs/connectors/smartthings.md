# Smartthings MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Smartthings via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-smartthings`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `api.smartthings.com`
* Authentication: provider OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | status check: verify token, list locations | Autonomous Execution |
| `locations` | list locations | Autonomous Execution |
| `devices` | list devices with capabilities | Autonomous Execution |
| `status` | read full device status | Autonomous Execution |
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
