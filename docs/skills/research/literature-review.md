# Literature Review Dot Skill

Conduct systematic literature reviews - search strategy, screening, quality appraisal, synthesis, and gap identification. Use when mapping what a field knows on a question.

## Skill Metadata

* Identifier: `dots-skill-literature-review`
* Category: Research
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Literature Review specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
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

# Literature Review

A literature review answers: what does the field know, how well does it know it, and what's 
missing. Done systematically, it's research in its own right - not a reading list.

## Overview

The method: define a focused question, design a reproducible search, screen studies against 
explicit criteria, appraise their quality, extract findings into a structured form, and synthesize 
 - narratively or quantitatively. The review's value is in the synthesis: patterns across studies, 
contradictions explained, and gaps named. Every step is documented so another researcher could 
repeat it.

## When to use

- Starting a thesis, paper, or project: establishing what exists.
- Answering "what does the evidence say about X?" rigorously.
- Identifying research gaps worth pursuing.
- Writing the related-work or background section of a paper.

## Core concepts

- **Review question**: narrow and answerable - population, intervention/exposure, comparison, 
outcome. Vague questions produce unmanageable reviews.
- **Search strategy**: databases, keywords, synonyms, date ranges, documented exactly. Snowball 
from key papers' references and citations.
- **Screening**: title/abstract then full-text, against pre-defined inclusion/exclusion criteria. 
Two independent screeners when rigor matters; record exclusions.
- **Quality appraisal**: assess each study's methods - design, sample, measures, analysis, bias 
risks. Weight findings by quality, not by count.
- **Data extraction**: structured forms - study design, sample, methods, key findings, 
limitations. Consistency enables comparison.
- **Synthesis**: narrative (themes, patterns), tabular (comparison matrices), or quantitative 
(meta-analysis). End with: what's established, what's contested, what's missing.

## Practical workflow

1. Frame the question precisely; write inclusion/exclusion criteria before searching.
2. Run the documented search across databases; deduplicate; snowball key citations.
3. Screen in two passes (title/abstract, then full text); log every exclusion reason.
4. Appraise quality with a checklist appropriate to the study designs; extract findings into 
structured forms.
5. Synthesize: group by theme or method, compare findings, explain contradictions, assess the 
strength of evidence.
6. Write up: search flow, included studies table, synthesis, gaps, and implications - with the 
protocol documented for reproducibility.

```text
Review protocol (write before searching):
QUESTION: <focused, answerable>
CRITERIA: include <...> / exclude <...>
SOURCES: <databases + search strings + date range>
SCREENING: <two-pass process, who screens>
APPRAISAL: <quality checklist per study design>
EXTRACTION:<fields captured per study>
SYNTHESIS: <narrative / tabular / meta-analytic plan>
```

## Common pitfalls

- **Question too broad**: "AI in healthcare" is a library, not a review. Narrow until the corpus is 
manageable.
- **Undocumented search**: a review nobody can reproduce. Record every string, database, and date.
- **Cherry-picking**: citing supportive studies, ignoring the rest. The criteria - written first 
 - protect against this.
- **Vote counting**: "5 studies say yes, 3 say no" without weighing quality. Appraise before 
synthesizing.
- **No gap analysis**: summarizing without identifying what's missing. Gaps are the review's main 
contribution.
- **Stale by publication**: fields move fast. Note the search date; update before submitting.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
