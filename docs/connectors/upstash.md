# Upstash MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Upstash via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-upstash`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `*.upstash.io`
* Authentication: Per-database token (host declared at connect time)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `status` | Verify connection to upstash. | Autonomous Execution |
| `query` | Retrieve data from upstash. | Autonomous Execution |
| `execute` | Perform action in upstash. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
