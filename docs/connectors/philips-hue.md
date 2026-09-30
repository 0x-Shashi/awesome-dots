# Philips Hue MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Philips Hue via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-philips-hue`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `derived from --host at runtime; the CLI refuses to send the key anywhere else`
* Authentication: Bridge pairing (local) or OAuth2 (remote)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `status` | Verify connection to philips-hue. | Autonomous Execution |
| `query` | Retrieve data from philips-hue. | Autonomous Execution |
| `execute` | Perform action in philips-hue. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
