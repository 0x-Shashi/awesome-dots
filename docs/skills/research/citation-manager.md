# Citation Manager Dot Skill

Manage citations and references - collecting sources, organizing libraries, formatting bibliographies, and keeping reference integrity. Use when writing anything that cites sources.

## Skill Metadata

* Identifier: `dots-skill-citation-manager`
* Category: Research
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Citation Manager specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
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

# Citation Manager

Citations are the paper's supply chain: every claim traceable to its source. Managing them means 
collecting sources systematically, organizing them so you can find anything, formatting 
consistently, and - critically - verifying that every citation is real and says what you claim.

## Overview

The workflow: capture sources as you read (never "I'll find it later"), store them with notes on 
why they matter, cite-while-you-write with keys instead of hand-typed references, and generate the 
bibliography from the library. The integrity rule: every in-text citation matches a real source 
you've read, and every bibliography entry is cited. Reference managers automate formatting; they 
don't automate honesty.

## When to use

- Writing papers, theses, reports, or any document with references.
- Building a personal research library over time.
- Collaborating: shared libraries keep everyone's citations consistent.
- Cleaning up a manuscript's references before submission.

## Core concepts

- **Capture at reading time**: save the full citation + PDF + your notes the moment you read 
something useful. "I'll relocate it later" fails reliably.
- **Cite keys**: stable keys (`smith2024attention`) used in drafts; the formatted reference is 
generated, never hand-typed. Renumbering-proof.
- **Annotated library**: each entry with a one-line note - what it claims, why you cited it. 
Future you will thank present you.
- **Style consistency**: one citation style per document (APA, IEEE, Chicago…), applied by the 
tool, not by hand. Switching styles should be one setting.
- **Reference integrity**: every citation verified - the source exists, you read the relevant 
part, it supports your claim. AI-generated citations must be checked individually.
- **Deduplication**: the same source saved three ways creates triple entries. Merge duplicates; 
keep one canonical record.

## Practical workflow

1. Set up the library before writing: folder structure or tags by project/topic.
2. For each source read: save citation metadata, the file, and a 2-line note (claim + relevance).
3. Write with cite keys; never type a formatted reference by hand.
4. Before submission: run the integrity check - every key resolves, every entry is cited, no 
duplicates, style consistent.
5. Verify AI-suggested citations individually: confirm the source exists and supports the claim.
6. Archive the library with the manuscript version so the reference set is reproducible.

```text
Source note template:
KEY: smith2024attention
CLAIM: <what the paper shows, in your words>
USE: <why you're citing it - which argument it supports>
READ: <which sections you actually read>
LIMIT: <caveats relevant to your use>
```

## Common pitfalls

- **Phantom citations**: references that don't exist - the classic AI failure mode. Verify every 
single one.
- **Citation without reading**: citing the abstract or a citation-of-a-citation. Read the part you 
rely on.
- **Hand-formatted references**: typed bibliographies that break on every edit. Generate from keys.
- **No notes**: a library of 500 PDFs with no memory of why each mattered. Annotate at capture time.
- **Style drift**: mixed formats in one document. Set the style once; let the tool enforce it.
- **Uncited bibliography entries**: sources in the list that nothing cites (or claims nothing 
supports). Audit both directions.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
