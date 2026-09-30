# Tally MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Tally via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-tally`
* Runtime: Model Context Protocol (MCP) Server
* Category: Forms and Surveys
* Target Host: `api.tally.so`
* Authentication: API key (per-user; free on all plans)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `forms` | list forms | Autonomous Execution |
| `form` | fetch a form with its blocks | Autonomous Execution |
| `create` | create a form | Supervised Execution |
| `update` | replace blocks | Supervised Execution |
| `submissions` | read submissions | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
