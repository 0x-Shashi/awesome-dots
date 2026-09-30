# Wise MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Wise via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-wise`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.wise.com`
* Authentication: Wise personal API token (per-user, wise.com \u2192 Settings \u2192 API tokens)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `profiles` | list profiles (also the status check) | Autonomous Execution |
| `balances` | multi-currency balances for profile P | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
