# Mistral MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Mistral via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-mistral`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.mistral.ai`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `models` | list models for this key | Autonomous Execution |
| `chat` | chat completion (bills credits) | Autonomous Execution |
| `chat` | Execute chat command. | Autonomous Execution |
| `embeddings` | embeddings (bills credits) | Autonomous Execution |
| `embeddings` | print complete vectors | Autonomous Execution |
| `ocr` | OCR a PDF (billed per page) | Autonomous Execution |
| `ocr` | Execute ocr command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
