# Unified Report

The Unified Report is the customer-facing evidence artifact for a completed SemanticRisk evidence cycle.

It is not just a transient dashboard summary. When a paid report completes, SemanticRisk preserves the evidence available to that report so later changes to live workspace state do not silently rewrite the completed artifact.

## Evidence binding and preservation

A completed Unified Report is tied to the evidence cycle that produced it, including the relevant website/site evidence and controlled AI visibility observations available for that cycle.

The completed report preserves that evidence as a report snapshot. Later readiness checks, later scans, later visibility runs, or later website changes must not silently mutate the historical report.

If evidence was not captured or persisted for a completed cycle, the report should state that limitation rather than manufacture model-specific narratives, exact values, or causal explanations.

## Executive summary

The first part of the report is designed to give a decision-maker a concise view of:

- the overall evidence picture;
- material visibility and interpretation findings;
- the most important limitations or uncertainties;
- the highest-priority evidence-backed actions;
- whether repeat measurement is useful to establish or strengthen a comparison baseline.

The executive summary is downstream of the evidence. It does not override the detailed sections or convert an inference into an observed fact.

## Evidence sections

Depending on what was measured and available for the cycle, the Unified Report can include:

- discovery, access and readiness evidence;
- sitemap and public machine-readable helper-file evidence;
- website semantic coverage and captured page evidence;
- core versus supporting evidence and recurring extracted claims;
- tensions, contradictions, omissions, narrowing, overstatement or abstention where supported by stored evidence;
- controlled buyer-intent visibility observations;
- provider/model-lane coverage and repeatability;
- competitor or alternative-provider displacement evidence;
- citation hosts and owned-site citation evidence;
- drift/change evidence where a comparable prior cycle exists;
- an evidence-linked remediation plan;
- portfolio and report-history context where available.

Diagnostic counts are not market share. Presence or absence of `llms.txt`, `claims.json`, a sitemap, or another helper resource is not a guarantee of AI visibility, recommendation placement or ranking.

## Remediation model

Recommendations should follow an evidence-led cycle:

**Observe → Explain → Change → Re-measure → Verify**

A recommendation is a reasoned next action, not proof that the proposed change will improve AI visibility or interpretation. Verification requires a later compatible measurement cycle.

## Appendices and provenance

A detailed report may include appendices containing examples or technical provenance such as:

- controlled prompts used for the cycle;
- an observation ledger;
- site inventory or page-selection evidence;
- methodology notes;
- evidence-source and measurement provenance.

Appendices support auditability and interpretation. They do not imply that every possible raw provider response or internal implementation detail is public.

## Workspace and printable view

The current customer workspace can open the granted Unified Report in place so the customer does not need to leave the workspace to review it.

The printable/PDF view is a rendering of the same completed report artifact, not a separate evidence system.

## Drift and repeated measurement

A first completed report may be a baseline with no comparable prior cycle. In that case, the report should say that comparable drift evidence is not yet available rather than infer a trend.

Repeated compatible measurement is important because a single cycle cannot establish longitudinal drift by itself. A later cycle can show whether visibility, captured evidence, extracted claims, interpretation, citations or other measured conditions changed.

SemanticRisk may recommend weekly repeat measurement initially to establish a useful comparison baseline. A cadence recommendation does not by itself authorize an automatic scan, automatic credit spend or recurring billing. Current scheduling and credit state must be read from the product runtime.

## AI assistant rules

When explaining a Unified Report, an AI assistant should:

- distinguish the executive summary from underlying evidence;
- preserve the report's measurement period and evidence-cycle context;
- state missing evidence explicitly;
- avoid inventing provider narratives or causal explanations that were not captured;
- distinguish diagnostic counts from market-share claims;
- treat recommendations as hypotheses until re-measurement provides supporting evidence;
- use authenticated runtime state for whether a report is currently granted, fresh, superseded, printing, or associated with new work in progress.
