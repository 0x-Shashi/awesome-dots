# Prusa Connect MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Prusa Connect via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-prusa-connect`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `connect.prusa3d.com`
* Authentication: personal API token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API token | Autonomous Execution |
| `printers` | printers and their state | Autonomous Execution |
| `jobs` | jobs and their status | Autonomous Execution |
| `files` | files in printer storage | Autonomous Execution |
| `files` | Execute files command. | Autonomous Execution |
| `cameras` | printer cameras | Autonomous Execution |
| `stats` | print statistics | Autonomous Execution |
| `upload` | Execute upload command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
