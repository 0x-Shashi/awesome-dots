# Etsy MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Etsy via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-etsy`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `openapi.etsy.com`
* Authentication: OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify OAuth token and keystring | Autonomous Execution |
| `receipts` | list receipts (orders) | Autonomous Execution |
| `listings` | list active listings | Autonomous Execution |
| `listing-create` | create a listing (confirm first) | Supervised Execution |
| `transactions` | list transactions | Autonomous Execution |
| `ledger` | list payment-account ledger entries | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
