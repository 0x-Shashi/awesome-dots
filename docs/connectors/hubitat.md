# Hubitat MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Hubitat via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-hubitat`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `the host you pass via --host`
* Authentication: Maker API token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `status` | Verify connection to hubitat. | Autonomous Execution |
| `query` | Retrieve data from hubitat. | Autonomous Execution |
| `execute` | Perform action in hubitat. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
