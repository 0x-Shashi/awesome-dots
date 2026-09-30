# Polar MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Polar via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-polar`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.polar.sh`
* Authentication: Organization Access Token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the access token | Autonomous Execution |
| `orders` | list orders | Autonomous Execution |
| `subscriptions` | list subscriptions | Autonomous Execution |
| `products` | list products | Autonomous Execution |
| `customers` | list customers | Autonomous Execution |
| `checkout-create` | create a checkout (confirm first) | Supervised Execution |
| `refund-create` | issue a refund (confirm first) | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
