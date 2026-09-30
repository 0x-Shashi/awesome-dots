# Spotify MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Spotify via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-spotify`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.spotify.com`
* Authentication: OAuth 2.0 Authorization Code (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `me` | current user's profile | Autonomous Execution |
| `playlists` | list the user's playlists | Autonomous Execution |
| `playlist-tracks` | tracks in a playlist | Autonomous Execution |
| `top-tracks` | user's top tracks | Autonomous Execution |
| `top-artists` | user's top artists | Autonomous Execution |
| `search` | search the catalog | Autonomous Execution |
| `playlist-create` | Execute playlist-create command. | Supervised Execution |
| `playlist-add` | Execute playlist-add command. | Autonomous Execution |
| `save-track` | Execute save-track command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
