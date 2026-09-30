# Google Nest MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Google Nest via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-google-nest`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `smartdevicemanagement.googleapis.com`
* Authentication: provider OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `status` | Verify connection to google-nest. | Autonomous Execution |
| `query` | Retrieve data from google-nest. | Autonomous Execution |
| `execute` | Perform action in google-nest. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
