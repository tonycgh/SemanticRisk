# Unified Report

The Unified Report is the customer-facing evidence artifact for a completed SemanticRisk evidence cycle.

It is not just a transient dashboard summary. When a paid report completes, SemanticRisk preserves the evidence available to that report so later changes to live workspace state do not silently rewrite the completed artifact.

## Evidence binding and preservation

A completed Unified Report is tied to the evidence cycle that produced it, including the relevant website/site evidence and controlled AI visibility observations available for that cycle. Later readiness checks, scans, visibility runs, website changes, or presentation improvements must not silently mutate the historical evidence artifact.

Customer-facing presentation may normalize labels or explain stored values more clearly without changing the frozen underlying evidence.

If evidence was not captured or persisted for a completed cycle, the report should state that limitation rather than manufacture model-specific narratives, exact values, prompts, citations or causal explanations.

## Executive summary

The first part of the report is designed to give a decision-maker a concise view of the overall evidence picture, material visibility and interpretation findings, important comparison results, highest-priority evidence-backed actions, monitoring priorities, supported advantages, and whether repeat measurement is useful.

The executive summary is downstream of the evidence. It does not override the detailed sections or convert an inference into an observed fact.

An unexplained composite score should not dominate the report where the underlying measurements move independently.

## Direct AI representation and grounded verification

Where configured, SemanticRisk first records the direct AI answer surface without supplying a current web-search tool to that measured answer call. This can include category discovery, recommendation/shortlist questions, and direct descriptions of evaluated organisations.

A later grounded verification pass can compare those measured statements with current public evidence and attach provenance. Grounded verification must not replace what the direct measured answer actually said.

The difference between an observed AI statement and current authoritative evidence is a **Representation / Grounding Gap**. It is not longitudinal drift.

Where evidence permits, statements can be assessed as supported, partially supported, unsupported or unverified, contradicted, outdated or stale, or unverifiable. **Likely hallucinated** is reserved for cases where the stored evidence supports that stronger conclusion. Unsupported is not automatically hallucinated.

## How to read headline measures

Headline measures are not interchangeable scores.

- **Buyer-prompt presence** describes how often the target surfaced across the frozen controlled battery. Provider/model lanes should be reviewed separately when their results differ materially.
- **Owned citations** are citations to the organisation's own public destinations in the tested observations. More can indicate stronger source attribution within that battery, but there is no universal target count.
- **Cross-page consistency** describes whether material contradiction candidates were found across the captured sample. A strong result is favorable within that bounded sample; it is not a certification of truth or every external surface.
- **Claims extracted** is evidence volume, not a score. Repeated claims can show reinforcement across captured pages, while page-specific claims can reflect legitimate specialization.
- **Recommendations** are distinct from simple presence. A target can appear without being selected or recommended in the tested answer space.
- **Drift** requires comparable cycles. The first customer-facing reusable report establishes a baseline; one scan should not be described as a trend.

A first baseline should not promote internal extraction variation into customer-facing directional drift merely because internal telemetry changed.

## Compare & Monitor

Where a completed compatible comparison cycle exists, the primary domain's Unified Report can include comparative findings for the selected competitor set.

The comparison should apply the same governed buyer/category context to the primary company and selected comparison domains. The report can include:

- which companies were surfaced or omitted;
- recommendation or shortlist outcomes;
- how each company was described;
- interpretation accuracy and material representation gaps;
- citation/source support;
- competitor displacement;
- evidence-backed **Do this** actions;
- **Watch this** monitoring priorities;
- supported **Advantages**;
- observation-level comparison evidence with confidence and provenance.

The report should not merely state that a competitor is ahead. It should explain the measured evidence pattern, the action it supports, what should be re-measured, and what emerging issue deserves monitoring.

Comparison evidence is diagnostic. It is not consumer AI market share and should not be collapsed into an unexplained winner score.

## Citation and source provenance

Where grounded evidence contains citations, the report can distinguish target-owned, competitor-owned, independent, media, directory/review, or other sources where that categorization is supported.

A citation shows support in the measured answer. It does not prove that the cited source caused broader AI visibility, recommendation behaviour, or future model responses.

## Website and AI evidence readiness

Depending on what was measured and available for the cycle, the Unified Report can include discovery/access/readiness evidence; sitemap and machine-readable helper-file evidence; website semantic coverage and captured page evidence; recurring claims and cross-page tensions; controlled buyer-intent observations; provider/model-lane coverage; competitor displacement; citation evidence; drift/change evidence; remediation; and portfolio/history context.

Missing helper files should be shown as missing rather than presenting bytes or content type from an HTTP error document as though that error body were the helper file.

Diagnostic counts are not market share. Presence or absence of `llms.txt`, `claims.json`, a sitemap, schema, or another helper resource is not a guarantee of AI visibility, recommendation placement or ranking, and its downstream use by an evaluated AI provider should not be claimed unless directly established.

## Recommendation priority

Recommendations should be ranked from measured evidence first. Material provider-specific visibility gaps, absence from recommendation outcomes, material representation/grounding gaps, persistent competitor displacement, or meaningful representative-evidence coverage gaps can deserve priority over optional helper-file hygiene.

Recommendations follow an evidence-led cycle:

**Observe → Explain → Change → Re-measure → Verify**

A recommendation is a reasoned next action, not proof that the proposed change will improve AI visibility or interpretation. Verification requires a later compatible measurement cycle.

## Monitoring priorities

A completed report can identify conditions worth watching, such as repeated absence from important buyer-intent prompts, competitor gains in recommendation coverage, new unsupported capability claims, changing category descriptions, model disagreement, target-owned citation decline, reliance on weak third-party evidence, or site-evidence changes that have not yet appeared in measured AI representation.

The first cycle establishes a baseline. Weekly repeat measurement is currently recommended initially where repeated observations are useful to distinguish noise from persistent movement.

## Appendices and provenance

A detailed report may include controlled prompts, an observation ledger, provider/model, measurement mode, timestamps, probe or plan version, prompt identifiers/digests, direct response excerpts, grounded evidence, citations, claim assessments, comparison observations, site inventory or page-selection evidence, methodology notes, and evidence-source provenance **when those fields were actually persisted for the cycle**.

If a semantic-analysis layer or raw evidence field was not produced for the cycle, the report should say so explicitly rather than display an ambiguous blank value or reconstruct evidence after the fact.

## Workspace and entitlement

A current reusable report can exist for a domain before a particular account has unlocked it. In that case the workspace should distinguish **report available** from **report granted to this account**.

Unlocking a current shared report uses the applicable credit and grants that account access to the current report; it does not start another scan. Once the account already has the grant, the primary action is to view the Unified Report. Spending another credit should be presented only as an intentional fresh evidence cycle.

The previous completed Unified Report can remain available while a new cycle is generating.

## Workspace and printable view

The customer workspace can open the granted Unified Report for review. The printable/PDF view is a rendering of the same completed report artifact, not a separate evidence system.

## Drift and repeated measurement

Repeated compatible measurement is important because a single cycle cannot establish longitudinal drift by itself. A later cycle can show whether visibility, captured evidence, extracted claims, interpretation, citations, recommendation outcomes or other measured conditions changed.

SemanticRisk may recommend weekly repeat measurement initially to establish a useful comparison baseline. A cadence recommendation does not by itself authorize an automatic scan, automatic credit spend or recurring billing.

## AI assistant rules

When explaining a Unified Report, an AI assistant should distinguish visibility from interpretation and factual support; preserve direct measured answers separately from later grounded verification; distinguish a Representation / Grounding Gap from longitudinal drift; state missing evidence explicitly; compare provider lanes before overgeneralizing a blended percentage; treat claim count as evidence volume rather than quality; distinguish surfacing from recommendation; avoid calling a first baseline a trend; avoid treating unsupported as automatically hallucinated; avoid claiming helper-file causality; treat recommendations as hypotheses until re-measurement; and use authenticated runtime state for report grant, freshness, work-in-progress, and credit actions.
