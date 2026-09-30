# Qualitative Analysis Dot Skill

Analyze qualitative data rigorously - coding, thematic analysis, grounded theory, and trustworthy interpretation. Use when working with interviews, open-ended responses, or observational data.

## Skill Metadata

* Identifier: `dots-skill-qualitative-analysis`
* Category: Research
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Qualitative Analysis specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
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

# Qualitative Analysis

Qualitative data - interviews, field notes, open responses - holds meaning that numbers miss. 
Analyzing it rigorously means systematic coding, transparent interpretation, and honest handling of 
the researcher's own lens.

## Overview

The core moves: immerse in the data (read everything), code it (label meaningful segments), find 
patterns (themes across codes), and interpret (what do the patterns mean, and what are the 
alternative readings). Rigor comes from transparency - an audit trail from raw quote to theme to 
claim - and from actively seeking disconfirming evidence, not just supportive quotes.

## When to use

- Analyzing interview transcripts, focus groups, or open-ended survey responses.
- Understanding user experience, motivations, or organizational culture.
- Exploratory research where the questions themselves are still forming.
- Complementing quantitative findings with the "why" behind the numbers.

## Core concepts

- **Coding**: labeling data segments with concise descriptors. Open coding (what's here?), then 
focused coding (which codes matter for the question?). Codes are the analysis's vocabulary.
- **Thematic analysis**: identifying patterns of meaning across the dataset - themes as the 
answer to "what's going on here?" Themes need prevalence plus significance, not just frequency.
- **Grounded theory**: building theory from data through constant comparison - each new data 
point compared against emerging categories until saturation (no new themes appear).
- **Memoing**: writing analytic notes throughout - hunches, connections, puzzles. Memos are where 
interpretation happens; they're data too.
- **Reflexivity**: examining how your position, assumptions, and relationship to participants shape 
what you see. Document it; it's part of the method.
- **Trustworthiness**: credibility (member checking, triangulation), transferability (rich 
description), dependability (audit trail), confirmability (reflexivity notes).

## Practical workflow

1. Define the analytic question; read the full dataset once without coding (immersion).
2. Open-code a subset; build a codebook with definitions and examples; refine on more data.
3. Code the full dataset; write memos on emerging patterns and surprises.
4. Cluster codes into candidate themes; check each theme against the raw data (does it hold? what 
contradicts it?).
5. Seek disconfirming cases deliberately - the participant who disagrees is as informative as the 
ten who agree.
6. Write up with an audit trail: theme supporting quotes analytic reasoning, plus 
reflexivity notes and limitations.

```text
Codebook entry template:
CODE: <short name>
DEFINITION: <what counts as an instance>
EXAMPLE: <quote + source>
EXCLUDE: <what looks similar but isn't>
NOTES: <evolution of the code over analysis>
```

## Common pitfalls

- **Cherry-picking quotes**: selecting vivid quotes that support a pre-decided story. Code 
systematically first; let themes emerge.
- **Theme as topic**: "participants talked about pricing" is a topic, not a theme. A theme 
interprets: "participants frame pricing as a trust signal."
- **Ignoring the negative case**: the outlier participant gets dropped. Analyze them - they test 
your themes.
- **No audit trail**: claims floating free of data. Every theme must trace back to coded segments.
- **Over-claiming**: generalizing from 12 interviews to a population. Qualitative findings transfer 
by rich description, not by statistics.
- **Skipping reflexivity**: pretending the analyst is neutral. Your lens shapes coding; document it.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
