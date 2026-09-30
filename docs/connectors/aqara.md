# Aqara MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Aqara via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-aqara`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `open-<region>.aqara.com`
* Authentication: OAuth-style account authorization via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | UNTESTED: status check, list homes | Autonomous Execution |
| `homes` | UNTESTED: list homes | Autonomous Execution |
| `rooms` | UNTESTED: list rooms | Autonomous Execution |
| `devices` | UNTESTED: list devices | Autonomous Execution |
| `status` | UNTESTED: read device attributes | Autonomous Execution |
| `control` | Execute control command. | Autonomous Execution |
| `control` | Execute control command. | Autonomous Execution |
| `control` | Execute control command. | Autonomous Execution |
| `control` | Execute control command. | Autonomous Execution |
| `control` | Execute control command. | Autonomous Execution |
| `scenes` | Execute scenes command. | Autonomous Execution |
| `run-scene` | Execute run-scene command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
