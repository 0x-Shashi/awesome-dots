# Sentry MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Sentry via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-sentry`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `sentry.io`
* Authentication: auth token (per-user, sentry.io \u2192 Settings \u2192 Auth Tokens)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `orgs` | your organizations | Autonomous Execution |
| `projects` | projects in an org | Autonomous Execution |
| `issues` | unresolved issues, last 24h, by frequency | Autonomous Execution |
| `resolve` | Execute resolve command. | Autonomous Execution |
| `archive` | Execute archive command. | Autonomous Execution |
| `assign` | Execute assign command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
