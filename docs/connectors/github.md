# Github MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Github via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-github`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `api.github.com`
* Authentication: personal access token (classic, scopes `repo` + `read:user`, per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (GET /user) | Autonomous Execution |
| `repos` | list your repos (name, private, updated_at) | Autonomous Execution |
| `issues` | open issues in a repo | Autonomous Execution |
| `create-issue` | Execute create-issue command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
