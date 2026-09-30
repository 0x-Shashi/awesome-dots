# Fal Ai MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Fal Ai via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-fal-ai`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `fal.run`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key (free) | Autonomous Execution |
| `models` | list the model catalog | Autonomous Execution |
| `run` | submit a job | Autonomous Execution |
| `status` | poll the job | Autonomous Execution |
| `result` | fetch the finished result | Autonomous Execution |
| `upload` | upload a local file to fal's CDN | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
