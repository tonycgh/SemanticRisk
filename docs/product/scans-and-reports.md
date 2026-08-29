# Scans and Reports

This page defines the public reasoning relationship between SemanticRisk scans, observations, findings, and reports.

## Scan

A scan is a bounded evaluation run against a domain.

A scan can capture website evidence, access conditions, model observations, claims, and other structured outputs used by SemanticRisk.

A scan observes the target. It does not modify the target website.

## Scan state

Scans and report generation can be asynchronous work.

The product may show work as queued, running, completed, or failed. The exact runtime state should be read from the product rather than guessed from elapsed time or from the existence of a request.

An AI assistant should distinguish:

- **requested** — a user or system asked for work;
- **queued** — the work has been accepted but not completed;
- **running** — the work is actively being processed;
- **completed** — the governed product path reports completion;
- **failed** — the product reports that work did not complete successfully.

The assistant must not treat "requested" or "queued" as equivalent to "completed".

## Observation

A completed scan can produce one or more observations.

Observations are the underlying recorded results used for later comparison. They should be preferred over report prose when an AI needs to explain the precise source of a finding.

## Comparison

SemanticRisk can compare observations across time or across models.

A comparison can surface:

- no material change;
- content change;
- extraction or interpretation change;
- stance or confidence change;
- mixed change;
- capture or pipeline conditions that prevent a clean comparison.

A difference should not automatically be presented as harmful or as proof that the website changed.

## Finding

A finding is a reviewable result derived from evidence and comparison.

A good finding should preserve enough context to answer:

- what changed or differed;
- which observations are being compared;
- what evidence supports the finding;
- whether the likely driver is known or uncertain;
- why the difference may matter.

## Report

A report is a user-facing synthesis of the available evidence, observations, comparisons, findings, and recommendations.

A report can be useful for communication and decision-making, but it is downstream of the underlying evidence.

When an AI assistant has access to structured evidence and a report, it should not invent precision that exists in neither source. If a report summarizes a change but the underlying evidence does not establish the cause, the assistant should describe the cause as uncertain.

## Regeneration and freshness

A newly requested scan or report does not make older output invalid immediately. Until new work completes, the most recent completed observation or report remains the latest completed record.

The assistant should make freshness explicit when it matters, for example:

- latest completed scan;
- scan currently running;
- report generated from a specified observation period.

## AI assistant rule

When answering "What happened?", prefer this order:

**runtime state → observation → evidence → comparison → finding → report summary**

This reduces the chance of explaining a summarized report as though it were direct source evidence.
