# Experiment Designer Dot Skill

Design rigorous experiments - hypotheses, controls, randomization, power analysis, and preregistration. Use when planning any study where you need trustworthy causal conclusions.

## Skill Metadata

* Identifier: `dots-skill-experiment-designer`
* Category: Research
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Experiment Designer specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
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

# Experiment Designer

An experiment is a question posed to reality in a way that reality can answer. Good design - 
clear hypotheses, proper controls, randomization, adequate power - is what separates evidence 
from anecdote.

## Overview

Design before data: state the hypothesis and what would falsify it, choose the design that isolates 
the effect (control groups, within-subject, factorial), randomize to kill confounds, blind where 
expectations could bias, and size the sample with a power analysis. Preregister the plan. Analysis 
choices made after seeing the data are hypotheses, not conclusions.

## When to use

- Planning A/B tests, clinical or behavioral studies, lab experiments, field trials.
- Deciding sample size: "how many participants/runs do I need?"
- Reviewing someone else's experimental plan for flaws.
- Choosing between experimental designs for a research question.

## Core concepts

- **Hypothesis and falsifiability**: a precise prediction plus the outcome that would disprove it. 
"X improves Y" needs: by how much, measured how, compared to what.
- **Controls**: the comparison that isolates your manipulation - placebo, baseline, active 
control. Without a control, you measured change, not cause.
- **Randomization**: random assignment breaks the link between confounds and conditions. Randomize 
what you can; measure and adjust for what you can't.
- **Blinding**: hiding condition assignments from participants and/or experimenters where 
expectations could bias outcomes. Single, double, or triple as needed.
- **Power analysis**: sample size from the smallest effect you care about, your noise level, and 
desired power (typically 80%). Underpowered studies can't answer their question.
- **Preregistration**: publishing the plan - hypotheses, measures, exclusion rules, analyses - 
before data collection. Separates confirmatory from exploratory.

## Practical workflow

1. Write the hypothesis, primary outcome measure, and the falsifying result - in one paragraph.
2. Choose the design: between-subjects (simpler, needs more N), within-subjects (powerful, watch 
order effects), factorial (interactions, needs planning).
3. Define controls, randomization procedure, and blinding level. List the confounds you're worried 
about and how each is handled.
4. Run the power analysis; if N is infeasible, simplify the question - don't run underpowered.
5. Preregister: hypotheses, measures, sample, exclusions, analysis plan. Lock it.
6. Analyze as preregistered; label anything else exploratory. Report nulls and deviations honestly.

```text
Experiment plan template:
HYPOTHESIS: <precise prediction + falsifier>
DESIGN: <between/within/factorial + why>
N: <from power analysis: effect, alpha, power>
CONTROLS: <comparison conditions>
RANDOMIZE: <unit + procedure> BLIND: <level>
MEASURES: <primary + secondary, how collected>
EXCLUSIONS: <pre-defined rules>
ANALYSIS: <tests, corrections, model>
```

## Common pitfalls

- **No control group**: measuring before/after without comparison. Change isn't causation.
- **Underpowered**: too-small samples that can't detect real effects - and produce exaggerated 
ones when they "succeed."
- **Peeking**: checking results mid-experiment and stopping when significant. Predefine stopping 
rules or don't look.
- **HARKing**: presenting exploratory findings as predicted. Preregistration is the defense.
- **Multiple comparisons uncorrected**: testing 20 outcomes and reporting the significant one. 
Correct or pre-specify the primary.
- **Confounds unaddressed**: the effect could be the manipulation or the time of day. List 
confounds; design each one away.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
