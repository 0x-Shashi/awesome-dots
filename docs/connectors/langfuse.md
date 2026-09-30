# Langfuse MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Langfuse via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-langfuse`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `cloud.langfuse.com`
* Authentication: Public+secret key pair (per-project; host declared at connect time)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the credential | Autonomous Execution |
| `traces` | list traces | Autonomous Execution |
| `traces` | traces for one session | Autonomous Execution |
| `observations` | list observations | Autonomous Execution |
| `prompts` | list prompts | Autonomous Execution |
| `prompts` | one prompt's details | Autonomous Execution |
| `score` | score a trace (confirm first) | Autonomous Execution |
| `datasets` | list datasets | Autonomous Execution |
| `dataset-item` | add a dataset item (confirm first) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
