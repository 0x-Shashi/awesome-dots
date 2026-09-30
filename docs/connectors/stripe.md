# Stripe MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Stripe via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-stripe`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.stripe.com`
* Authentication: Stripe restricted API key (per-user, Dashboard \u2192 Developers \u2192 API keys; read-only permissions suffice)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `balance` | current available + pending balance | Autonomous Execution |
| `charges` | recent charges | Autonomous Execution |
| `customers` | recent customers | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
