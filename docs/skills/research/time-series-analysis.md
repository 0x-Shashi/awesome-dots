# Time Series Analysis Dot Skill

Analyze time-ordered data - decomposition, stationarity, forecasting models, changepoint detection, and proper temporal validation. Use when the order of observations matters.

## Skill Metadata

* Identifier: `dots-skill-time-series-analysis`
* Category: Research
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Time Series Analysis specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
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

# Time Series Analysis

Time series data has memory: today's value depends on yesterday's. Analysis must respect that - 
in modeling (autocorrelation, seasonality, trends), in validation (never shuffle time), and in 
forecasting (uncertainty grows with horizon).

## Overview

Start by understanding the series: plot it, decompose into trend/seasonality/residuals, check 
stationarity. Model the structure you find - classical methods (ARIMA family, exponential 
smoothing) for well-behaved series, machine learning for complex patterns with enough data. 
Validate with time-based splits only: train on the past, test on the future, rolling forward. 
Forecast with intervals, because point forecasts without uncertainty are wishes.

## When to use

- Forecasting: demand, traffic, prices, sensor readings, resource usage.
- Detecting changes: changepoints, anomalies, regime shifts in temporal data.
- Understanding temporal structure: seasonality, trends, cycles, autocorrelation.
- Evaluating any model on time-ordered data (validation must respect time).

## Core concepts

- **Decomposition**: trend + seasonal + residual. Seeing the components separately reveals what to 
model - and what's just noise.
- **Stationarity**: constant mean/variance over time. Many methods assume it; differencing or 
detrending achieves it. Test (ADF/KPSS), don't assume.
- **Autocorrelation**: correlation with past values (ACF/PACF plots guide model order). Ignoring it 
leaves predictable structure on the table - or worse, in the residuals.
- **Classical models**: ARIMA/SARIMA for autocorrelated series with seasonality; exponential 
smoothing for trend/seasonal patterns; each with well-understood diagnostics.
- **ML approaches**: gradient boosting on lag features, deep models for long complex series. 
Powerful with enough data; hungry and opaque without it.
- **Temporal validation**: rolling-origin backtesting - train on past, predict future, roll 
forward. Random splits leak the future and lie about performance.

## Practical workflow

1. Plot the series; decompose; check stationarity and seasonality. Understand before modeling.
2. Establish baselines: naive (last value), seasonal naive, moving average. Many "advanced" models 
lose to these.
3. Fit candidate models; diagnose residuals - they should look like white noise. Structure left 
in residuals means structure unmodeled.
4. Backtest with rolling origins across multiple windows; compare on horizon-appropriate metrics 
(MAE, sMAPE, quantile loss).
5. Forecast with prediction intervals; communicate how uncertainty widens with horizon.
6. Monitor in production: detect drift and changepoints; retrain on a schedule, not on hope.

```text
Time series checklist:
[ ] Plotted + decomposed; stationarity tested
[ ] Naive/seasonal-naive baselines beaten
[ ] Residuals diagnosed (white noise?)
[ ] Rolling-origin backtest, multiple windows
[ ] Intervals reported, not just point forecasts
[ ] Retraining + drift monitoring planned
```

## Common pitfalls

- **Shuffled validation**: random train/test splits on time data. The model "predicts" the past 
from the future. Always split by time.
- **Skipping baselines**: complex models that lose to seasonal naive. Baselines first, always.
- **Ignoring residuals**: fitting without checking what's left. Residual structure is the model 
telling you what it missed.
- **Point forecasts only**: "demand will be 1,200." With what uncertainty? Intervals are the honest 
product.
- **Stationarity assumed**: applying ARIMA to a trending series without differencing. Test and 
transform.
- **Lookahead leakage**: features computed with future information (centered moving averages, 
full-series normalization). Every feature must be computable at forecast time.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
