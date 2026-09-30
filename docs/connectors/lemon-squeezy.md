# Lemon Squeezy MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Lemon Squeezy via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-lemon-squeezy`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.lemonsqueezy.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `orders` | list orders | Autonomous Execution |
| `subscriptions` | list subscriptions | Autonomous Execution |
| `customers` | list customers | Autonomous Execution |
| `products` | list products | Autonomous Execution |
| `checkout-create` | create checkout (confirm first) | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
