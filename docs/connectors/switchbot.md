# Switchbot MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Switchbot via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-switchbot`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `api.switch-bot.com`
* Authentication: token + secret pair via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | status check: verify token, count devices | Autonomous Execution |
| `devices` | list devices and IR remotes | Autonomous Execution |
| `status` | read device status | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `command` | Execute command command. | Autonomous Execution |
| `scenes` | Execute scenes command. | Autonomous Execution |
| `scene-execute` | Execute scene-execute command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
