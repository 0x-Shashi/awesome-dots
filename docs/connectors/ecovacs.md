# Ecovacs MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Ecovacs via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-ecovacs`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `open.ecovacs.com`
* Authentication: Access Key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the Access Key | Autonomous Execution |
| `devices` | list bound robots | Autonomous Execution |
| `status` | cleaning/paused/docked state | Autonomous Execution |
| `battery` | battery percent | Autonomous Execution |
| `stats` | area cleaned, duration | Autonomous Execution |
| `clean` | Execute clean command. | Autonomous Execution |
| `pause` | Execute pause command. | Autonomous Execution |
| `resume` | Execute resume command. | Autonomous Execution |
| `stop` | Execute stop command. | Autonomous Execution |
| `dock` | Execute dock command. | Autonomous Execution |
| `undock` | Execute undock command. | Autonomous Execution |
| `set-work-mode` | 0=sweep+mop, 1=sweep only, 2=mop only, 3=sweep then mop | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
