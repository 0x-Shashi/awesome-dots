# Printful MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Printful via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-printful`
* Runtime: Model Context Protocol (MCP) Server
* Category: Business Services
* Target Host: `api.printful.com`
* Authentication: personal access token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token | Autonomous Execution |
| `products` | list synced store products | Autonomous Execution |
| `orders` | list orders | Autonomous Execution |
| `order-create` | submit an order (confirm first; spends money) | Supervised Execution |
| `catalog-product` | show a catalog product and its variants | Autonomous Execution |
| `mockup-create` | start a mockup task | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
