# Moonraker MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Moonraker via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-moonraker`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `the host you pass via --host`
* Authentication: no credential needed on most LAN installs (optional API key via the secure credential flow)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | server info; never needs a credential | Autonomous Execution |
| `status` | print state and temperatures | Autonomous Execution |
| `files` | list gcode files | Autonomous Execution |
| `upload` | Execute upload command. | Supervised Execution |
| `print-start` | Execute print-start command. | Autonomous Execution |
| `print-pause` | Execute print-pause command. | Autonomous Execution |
| `print-resume` | Execute print-resume command. | Autonomous Execution |
| `print-cancel` | Execute print-cancel command. | User Handoff |
| `emergency-stop` | Execute emergency-stop command. | Autonomous Execution |
| `device-power` | Execute device-power command. | Autonomous Execution |
| `gcode-script` | Execute gcode-script command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
