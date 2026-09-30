# Clerk MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Clerk via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-clerk`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `api.clerk.com`
* Authentication: Secret API key (per-project)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the secret key | Autonomous Execution |
| `users` | list users | Autonomous Execution |
| `user` | look up one user | Autonomous Execution |
| `create` | create a user | Supervised Execution |
| `update` | update a user | Supervised Execution |
| `delete` | delete a user | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
