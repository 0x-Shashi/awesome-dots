# Homey MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Homey via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-homey`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `the host you pass via --host`
* Authentication: personal API token or OAuth via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `status` | Verify connection to homey. | Autonomous Execution |
| `query` | Retrieve data from homey. | Autonomous Execution |
| `execute` | Perform action in homey. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
