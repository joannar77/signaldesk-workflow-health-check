# SignalDesk Workflow Health Check

**Track A: Fictional Domain Packet**

## What I built

A short Jupyter notebook that helps the fictional SignalDesk product team assess three AI-assisted workflows and identify the most important issue to investigate before broader rollout.

The notebook cleans the export, calculates session-weighted workflow health metrics, and compares model-reported confidence with human-facing outcomes. It focuses on one core decision: which workflow appears healthiest, and which signal requires immediate investigation?

## Data

The analysis uses the provided fictional `product_usage_events.csv`, containing seven days of aggregated usage for Lead Summary, Reply Draft, and Feedback Clustering.

## Key finding

Lead Summary appears healthiest overall, with the highest acceptance among completed outputs and the lowest review flag rate. Reply Draft requires investigation: on August 7, model confidence reached 91% while acceptance fell to 47.1% and review flags rose to 40%. Because the review policy changed mid-day, this is an operational warning—not evidence that the model itself caused the decline.

## Assumptions and issues

Rates are calculated from summed counts rather than averages of row-level percentages. I removed one explicitly labeled duplicate export row, standardized inconsistent team casing, retained missing values, and treated demo-account traffic as non-routine. Confidence and estimated time saved are treated as directional rather than definitive quality measures.

## Run locally

```bash
pip install -r requirements.txt
jupyter notebook signaldesk-health-check.ipynb
```

## With more time

I would separate August 7 into pre-policy and post-policy cohorts, audit flagged outputs, exclude demo traffic from routine reporting, and monitor the same health metrics weekly.
