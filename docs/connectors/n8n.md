# N8N MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for N8N via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-n8n`
* Runtime: Model Context Protocol (MCP) Server
* Category: Automation
* Target Host: `your n8n instance host`
* Authentication: API key (instance; host declared at connect time)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `workflows` | list workflows | Autonomous Execution |
| `workflow` | inspect one workflow | Autonomous Execution |
| `create` | create a workflow | Supervised Execution |
| `update` | update a workflow (confirm first) | Supervised Execution |
| `executions` | list executions | Autonomous Execution |
| `executions` | executions for one workflow | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
