# Second Brain Dot Skill

Build a second brain: a trusted external system for capturing, organizing, and retrieving everything you learn and need. Use when knowledge is scattered or you want ideas to compound over time.

## Skill Metadata

* Identifier: `dots-skill-second-brain`
* Category: Productivity
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Second Brain specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
```

## Governance and Permission Mapping

| Action Phase | Operation | Assigned Permission Mode |
| :--- | :--- | :--- |
| Ingestion | Scanning feeds, reading logs, and inspecting state | Autonomous Execution |
| Processing | Running local transforms, filtering, and drafting | Autonomous Execution |
| Verification | Compiling candidate recommendations and reports | Prompt-Initiated Execution |
| Modification | Committing changes, dispatching messages, or updating records | Supervised Execution |
| Destruction | Deleting records, purging branches, or revoking access | User Handoff |

## Operational Instructions

# Second Brain

## Overview

A second brain is an external, organized, searchable system holding what your biological brain shouldn't have to: notes, ideas, resources, tasks, references.

Purpose: free your mind for thinking by trusting capture; make knowledge compound by connecting and revisiting it.

Built on four capabilities: capture everything, organize for action, distill to essence, express by creating.

Tool-agnostic - Notion, Obsidian, or any notes app works. The system matters, not the software.

## When to use

- Knowledge scattered across apps, notebooks, and memory
- Reading/learning a lot but retaining and reusing little
- Creative or knowledge work needing a personal idea library
- Setting up a long-term personal knowledge management system
- Wanting past work and learning to compound instead of evaporate

## Core concepts

- **Capture everything.**
 Fleeting ideas, quotes, highlights, meeting notes, voice memos - into one inbox within seconds. The brain is for having ideas, not storing them.
- **Organize for actionability.**
 File by where it's useful (projects, areas, resources), not by source or topic taxonomy. Organization serves retrieval, not aesthetics.
- **Distill progressively.**
 Bold key passages, highlight the best, summarize, extract the essence. Each layer compresses; the top layer is what you'll actually reuse.
- **Express regularly.**
 Knowledge compounds when used: write, build, teach, decide. A second brain that only collects is a museum; expression is the point.
- **Projects over topics.**
 Organize primarily around active projects (things with goals and deadlines). Topic-based filing creates beautiful libraries nobody opens.
- **Search-first retrieval.**
 Design for search: good titles, consistent naming, full-text search you trust. Retrieval beats perfect folders.
- **Interoperability.**
 Plain text / standard formats where possible. Your second brain should survive app changes - export regularly, avoid lock-in.
- **Review rhythms.**
 Weekly inbox processing, monthly project reviews, quarterly archive sweeps. A brain without maintenance becomes a attic.

## Practical workflow

1. **Choose one home.**
 One primary app for the second brain. Notion, Obsidian, Apple Notes - pick by your needs (database vs. markdown vs. simplicity).
2. **Set up capture everywhere.**
 Mobile quick-add, desktop hotkey, email-to-inbox, read-later integration. Capture in under 10 seconds from anywhere.
3. **Create the structure.**
 Top-level: Inbox, Projects (active), Areas (ongoing responsibilities), Resources (topics/interests), Archive. Keep it shallow.
4. **Migrate gradually.**
 Don't big-bang migrate years of notes. Move things as you touch them; leave the rest in a legacy archive, searchable.
5. **Build the distilling habit.**
 When saving anything: bold the key sentence, add one line in your own words. Thirty seconds now saves hours later.
6. **Create retrieval paths.**
 Project dashboards, an index note, consistent titles (`YYYY-MM-DD topic`). Test: can you find it in 30 seconds?
7. **Schedule expression.**
 Weekly writing/building time that draws on the brain. Retrieval practice is what converts storage into knowledge.
8. **Maintain quarterly.**
 Archive dead projects, merge duplicates, delete the useless. A second brain is a garden, not a warehouse.

## Common pitfalls

- **Collecting without expressing.**
 10,000 saved articles, zero created. Capture without expression is hoarding with extra steps.
- **Organizing as procrastination.**
 Perfecting folders and tags instead of thinking. Organization serves retrieval; beyond that it's avoidance.
- **Tool obsession.**
 Migrating apps yearly, rebuilding the system each time. The system is the habits, not the software. Commit.
- **No capture habit.**
 Elaborate structure, empty inbox. If capture takes >10 seconds, ideas stay in your head and die there.
- **Over-distilling.**
 Five layers of highlighting on every article. Distill the keepers; most inputs deserve capture-only or deletion.
- **Topic-based everything.**
 Beautiful topic hierarchies nobody browses. Organize by active projects first; topics are secondary.
- **No backups/exports.**
 Years of thinking in a proprietary format with no export. Regular exports; prefer portable formats.
- **Review-less accumulation.**
 Inbox growing forever, archive never touched. Without review rhythms, the brain becomes an attic of good intentions.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
