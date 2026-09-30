# Shopify MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Shopify via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-shopify`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `<your-shop>.myshopify.com`
* Authentication: Shopify Admin API access token (per-user, Shopify admin \u2192 Apps \u2192 Develop apps \u2192 custom app; scopes read_orders/read_products/read_customers plus write_products/write_discounts for writes)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection | Autonomous Execution |
| `orders` | open orders | Autonomous Execution |
| `products` | products | Autonomous Execution |
| `customers` | customers | Autonomous Execution |
| `product-create` | Execute product-create command. | Supervised Execution |
| `discount-create` | Execute discount-create command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
