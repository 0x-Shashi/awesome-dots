# Causal Inference Dot Skill

Estimate causal effects from observational and experimental data - DAGs, confounding control, quasi-experimental designs, and sensitivity analysis. Use when you need "what causes what," not just correlation.

## Skill Metadata

* Identifier: `dots-skill-causal-inference`
* Category: Research
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Causal Inference specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
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

# Causal Inference

Correlation is cheap; causation is the question that matters for decisions. Causal inference is the 
toolkit for answering "what would happen if we did X?" - from experiments when possible, and from 
observational data with explicit assumptions when not.

## Overview

Every causal claim rests on assumptions - the craft is making them explicit and testing them. 
Draw the causal graph (DAG) to see what confounds what. Choose the identification strategy that 
fits: randomization, or quasi-experiments (difference-in-differences, regression discontinuity, 
instrumental variables), or adjustment with careful confounder selection. Then probe robustness: 
sensitivity analysis asks how wrong the assumptions would need to be to overturn the conclusion.

## When to use

- Deciding whether an intervention works: policy, product change, treatment.
- Estimating effects from data you didn't experimentally control.
- Reviewing causal claims: checking whether the design supports the conclusion.
- Choosing between running an experiment and analyzing existing data.

## Core concepts

- **Potential outcomes**: the causal effect is the difference between what happened with treatment 
and what would have happened without it. The fundamental problem: you never observe both. All 
methods are ways around this.
- **DAGs**: directed acyclic graphs mapping assumed causal structure - confounders (common 
causes), mediators (mechanisms), colliders (conditioning on them biases). Draw it before choosing 
an analysis.
- **Confounding control**: adjust for confounders (backdoor paths), never for mediators or 
colliders. The DAG tells you which variables to include - "control for everything" is wrong.
- **Quasi-experiments**: difference-in-differences (parallel trends assumption), regression 
discontinuity (threshold assignment), instrumental variables (exclusion restriction). Each trades 
randomization for a different assumption - name it, defend it.
- **Propensity methods**: matching, weighting, or doubly-robust estimation to balance treated and 
control groups on observables. Only as good as the observed confounders.
- **Sensitivity analysis**: how strong would unmeasured confounding need to be to explain away the 
effect? Report it; it's the honest answer to "but what if you missed something?"

## Practical workflow

1. Define the treatment, outcome, and the decision the estimate informs.
2. Draw the DAG: hypothesized confounders, mediators, colliders. Get domain experts to critique it.
3. Choose identification: experiment if feasible; otherwise the quasi-experimental design whose 
assumptions you can best defend.
4. Estimate with appropriate methods; use doubly-robust approaches where available.
5. Run sensitivity analyses and placebo/falsification tests (effects where none should exist).
6. Report the estimate with uncertainty, the assumptions it rests on, and what would overturn it.

```text
Causal analysis checklist:
[ ] Treatment, outcome, estimand precisely defined
[ ] DAG drawn and critiqued; adjustment set derived from it
[ ] Identification strategy named with its key assumption
[ ] No adjustment for mediators/colliders
[ ] Falsification tests run (placebos, pre-trends)
[ ] Sensitivity to unmeasured confounding reported
```

## Common pitfalls

- **Controlling for everything**: adjusting for mediators (kills the effect) or colliders (creates 
bias). The DAG decides, not the kitchen sink.
- **Unstated assumptions**: every observational method assumes something untestable. Name it 
explicitly.
- **No falsification**: never testing where the method should find nothing. Placebos are cheap 
credibility.
- **Causal language from predictive models**: a regression coefficient is not a causal effect 
without a causal design.
- **Ignoring the estimand**: "the effect" of what, on whom, compared to what? Define it before 
estimating.
- **Fragile identification**: an IV with a weak first stage or a DiD with shaky parallel trends. 
Weak designs produce confident-looking noise.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
