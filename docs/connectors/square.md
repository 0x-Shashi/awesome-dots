# Square MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Square via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-square`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `connect.squareup.com`
* Authentication: provider OAuth 2.0 or personal access token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token (sandbox) | Autonomous Execution |
| `locations` | list seller locations | Autonomous Execution |
| `payments` | list payments | User Handoff |
| `payment-get` | one payment | User Handoff |
| `order-create` | create an order (moves no money) | Supervised Execution |
| `checkout-create` | Execute checkout-create command. | Supervised Execution |
| `checkout-get` | Terminal checkout status | Autonomous Execution |
| `checkout-cancel` | Execute checkout-cancel command. | User Handoff |
| `charge` | Execute charge command. | Autonomous Execution |
| `refund` | Execute refund command. | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
