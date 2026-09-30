# Octoprint MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Octoprint via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-octoprint`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `the host you pass via --host`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `version` | server version | Autonomous Execution |
| `status` | printer state, hotend and bed temps | Autonomous Execution |
| `job` | current print progress | Autonomous Execution |
| `files` | list gcode files on the printer | Autonomous Execution |
| `printhead` | home axes (LOW) | Autonomous Execution |
| `job-cmd` | Execute job-cmd command. | Autonomous Execution |
| `job-cmd` | Execute job-cmd command. | Autonomous Execution |
| `job-cmd` | Execute job-cmd command. | Autonomous Execution |
| `upload` | Execute upload command. | Supervised Execution |
| `file-select` | Execute file-select command. | Autonomous Execution |
| `tool-temp` | Execute tool-temp command. | Autonomous Execution |
| `bed-temp` | Execute bed-temp command. | Autonomous Execution |
| `gcode` | Execute gcode command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
