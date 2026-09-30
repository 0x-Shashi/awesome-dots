# Shippo MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Shippo via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-shippo`
* Runtime: Model Context Protocol (MCP) Server
* Category: Business Services
* Target Host: `api.goshippo.com`
* Authentication: API token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API token | Autonomous Execution |
| `rates` | rates for a shipment (no label bought) | Autonomous Execution |
| `get-shipment` | retrieve a shipment | Autonomous Execution |
| `track` | tracking status | Autonomous Execution |
| `buy` | buy a label from a rate | User Handoff |
| `buy` | Execute buy command. | User Handoff |
| `refund` | refund/void an unused label | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
