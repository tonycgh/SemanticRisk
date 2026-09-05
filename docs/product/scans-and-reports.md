# Scans and Reports

This page defines the public reasoning relationship between SemanticRisk scans, evidence cycles, observations, findings, and reports.

## Scan

A scan is a bounded evaluation run against a domain.

A scan can capture website evidence, access conditions, model observations, claims, and other structured outputs used by SemanticRisk.

A scan observes the target. It does not modify the target website.

## Pre-scan readiness and measurement context

Before paid Buyer Visibility Core work starts in the workspace, SemanticRisk separates free readiness/discovery from the paid evidence cycle.

The readiness step checks whether usable public content can be measured and inspects common machine-readable discovery resources. It does not consume a paid scan credit merely because it performs that preflight.

The customer also confirms a versioned measurement context describing the market/category, buyer need, decision/risk need, geography when relevant, and comparison set. The controlled visibility cycle is bound to the confirmed profile version used when the cycle begins.

A later context edit must not silently change the meaning of an earlier cycle. Earlier evidence remains associated with its original profile version.

See [Measurement context and readiness](measurement-context-and-readiness.md).

## Credit-funded full evidence cycle

A fresh credit-funded Unified Report is produced from one coherent evidence cycle rather than from independently selected recent artifacts.

For a new paid cycle, SemanticRisk performs fresh public discovery before the credit-funded work is committed, creates a cycle-bound site-evidence audit, selects a representative page set, and gathers that site evidence first. The cycle then proceeds to the controlled AI measurement and interpretation work needed for the report.

The current full cycle includes:

1. fresh site discovery and a cycle-bound representative website-evidence set;
2. Buyer Visibility Core v1: six controlled buyer-intent prompts, two model lanes, and two repetitions, for 24 controlled AI visibility observations; and
3. interpretation/scan evidence bound to that same report cycle.

The Unified Report is materialized only after the required evidence for the bound cycle has completed successfully. A new cycle must not silently reuse an older site-audit snapshot merely because newer visibility or interpretation evidence exists.

Existing completed reports remain frozen historical evidence. Starting a new cycle does not rewrite an earlier report.

A compatible recent cycle may be joined or recovered rather than duplicated. Compatibility includes the measurement-profile version used for the controlled visibility work. If an account has already funded the same generating report cycle, continuing or repairing that cycle does not consume another credit merely because processing was interrupted or temporarily throttled.

Older paid cycles that already contain compatible partial evidence may be completed in place using the credit already spent when the product can safely preserve the evidence boundary.

A completed full-cycle report snapshot is treated as immutable evidence. Polling or reconciliation must not silently replace its completed visibility run, site evidence, or extend its freshness window.

## Evidence-cycle phases and progress

A generating cycle can move through distinct evidence phases. Customer-facing progress should reflect the evidence actually completed rather than elapsed time.

During **site evidence** collection, the workspace can report representative pages completed, discovered URL count, and eligible-page count. Visibility and interpretation stages should remain visibly waiting rather than appearing complete from an older report.

After current site evidence is ready, controlled AI measurement and interpretation can proceed from the same cycle. If all 24 visibility observations are complete but interpretation is queued for a worker, the workspace should say so explicitly. A queued worker is processing state, not a reason to purchase another credit.

The previous completed Unified Report can remain available while a new cycle is generating. Its evidence must not be presented as though it were the new cycle's current evidence.

Overall progress percentages, when shown, should be derived from completed evidence stages or actual observation counts. SemanticRisk should not invent time-based percentages or ETAs for asynchronous work.

## Multiple domains and competitors

The primary site and comparison/competitor sites are separate measurable domains.

Adding a competitor to a workspace portfolio does not itself spend a credit. If the customer chooses to run a paid evidence cycle for that competitor, the normal per-domain credit rule applies and the competitor receives its own evidence and Unified Report.

Comparative report views may use evidence from multiple measured domains, but one domain's paid cycle should not be described as automatically funding another domain's scan.

## Provider delays and failure

Upstream model-provider throttling can delay individual observations. Recoverable provider throttling is retried automatically and should be presented as processing state rather than as evidence that the customer needs to purchase another cycle.

Where a paid evidence cycle reaches a terminal failure and cannot produce the funded report, the consumed credit is returned automatically. A SemanticRisk-side provider failure must not be converted into a second customer charge.

Exact provider limits, retry timing, queue position, and completion time are runtime/operational state and must not be inferred from this documentation.

## Scan and cycle state

Scans and report generation can be asynchronous work.

The product may show work as queued, running, partial/recovering, completed, or failed. The exact runtime state should be read from the product rather than guessed from elapsed time or from the existence of a request.

An AI assistant should distinguish:

- **requested** — a user or system asked for work;
- **queued** — the work has been accepted but not completed;
- **running** — work is actively being processed;
- **partial/recovering** — some required evidence exists and eligible remaining work is being recovered or retried;
- **completed** — the governed product path reports completion;
- **failed** — the product reports that work did not complete successfully.

The assistant must not treat requested, queued, or partial work as equivalent to completed evidence.

When available, progress such as representative site pages completed, completed visibility observations, or current interpretation job state should be read from runtime state. It is safe to tell a user that an asynchronous cycle continues after they leave the workspace, but an AI should not invent an ETA.

## Observation

A completed scan or evidence cycle can produce one or more observations.

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

Comparisons across evidence cycles should preserve the measurement context/profile version used by each cycle. If the market or buyer context changed between cycles, that context change is relevant to interpretation and should not be hidden.

## Finding

A finding is a reviewable result derived from evidence and comparison.

A good finding should preserve enough context to answer:

- what changed or differed;
- which observations are being compared;
- what evidence supports the finding;
- whether the likely driver is known or uncertain;
- why the difference may matter.

## Unified Report

The Unified Report is the customer-facing synthesis of the evidence cycle: available website evidence, visibility observations, comparisons, findings, and recommendations.

A report can be useful for communication and decision-making, but it is downstream of the underlying evidence.

When an AI assistant has access to structured evidence and a report, it should not invent precision that exists in neither source. If a report summarizes a change but the underlying evidence does not establish the cause, the assistant should describe the cause as uncertain.

A report may also provide comparison and next-step guidance. Recommendations for repeat measurement are guidance, not proof that automated recurrence, credit spend, or recurring billing is enabled.

## Regeneration and freshness

A newly requested evidence cycle does not make older completed output invalid immediately. Until new work completes, the most recent completed observation or report remains the latest completed record.

The assistant should make freshness explicit when it matters, for example:

- latest completed evidence;
- fresh site evidence currently being collected;
- fresh evidence cycle currently running;
- 18 of 24 controlled visibility observations complete, when runtime state actually reports that value;
- interpretation queued or running, when runtime state reports that state;
- report generated from a specified observation period.

## AI assistant rule

When answering “What happened?”, prefer this order:

**runtime state → observation → evidence → comparison → finding → report summary**

When answering “Do I need to pay again?”, prefer authenticated credit/grant/report runtime state over documentation. A recoverable, queued, or already-funded cycle must not be described as requiring another credit unless the current product state explicitly says so.

When explaining a visibility result, include the confirmed measurement context when it materially affects what was measured, and do not silently compare cycles bound to different context versions as though their setup were identical.

When a new cycle is running, do not substitute older completed site evidence, visibility evidence, or interpretation state for the current cycle merely because the older report remains available.

This reduces the chance of explaining a summarized report as though it were direct source evidence, mixing evidence generations, or turning an operational retry into an unnecessary customer purchase.
