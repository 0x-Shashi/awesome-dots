# Ynab MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Ynab via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-ynab`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.ynab.com`
* Authentication: OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `budgets` | list budgets | Autonomous Execution |
| `accounts` | account balances (balances are in milliunits) | Autonomous Execution |
| `transactions` | Execute transactions command. | Autonomous Execution |
| `categories` | category groups with budgeted/activity/balance | Autonomous Execution |
| `transaction-create` | Execute transaction-create command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
