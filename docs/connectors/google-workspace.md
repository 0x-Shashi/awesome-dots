# Google Workspace MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for inspecting calendar schedules, fetching shared documents, and organizing files via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-google-workspace`
* Runtime: Model Context Protocol (MCP) Server
* Target Host: `googleapis.com`
* Recommended Authentication: Google OAuth 2.0 User Grant with granular calendar and drive scopes.

## Action Permission Mapping

| MCP Tool Name | Action Description | Required Scope | Dots Permission Mode |
| :--- | :--- | :--- | :--- |
| `list_calendar_events` | Fetch upcoming meetings, attendees, and meeting descriptions. | `calendar.events.readonly` | Autonomous Execution |
| `search_drive_files` | Search documents, spreadsheets, and presentations in Google Drive. | `drive.metadata.readonly` | Autonomous Execution |
| `get_document_text` | Read text and outline content from a Google Doc. | `drive.readonly` | Autonomous Execution |
| `create_calendar_focus_block` | Insert a private focus or reminder block on the user's primary calendar. | `calendar.events` | Prompt-Initiated Execution |
| `send_meeting_invitation` | Dispatch a calendar invite to external attendees. | `calendar.events` | Supervised Execution |
| `delete_drive_file` | Permanently remove a file or move it to trash. | `drive` | User Handoff |

## Security Rules

1. External Attendee Gate: Sending invites to addresses outside the primary organization domain requires explicit user approval.
2. File Deletion Guard: Document purge or trash operations must trigger a mandatory User Handoff to avoid accidental loss of shared corporate assets.
