# Scans and Reports

This page defines the public relationship between SemanticRisk readiness checks, evidence cycles, observations, findings and Unified Reports.

## Readiness

Before commercial AI measurement begins, SemanticRisk can perform a free public readiness/discovery check to determine whether useful evidence is reachable and what public discovery resources are available.

A missing optional helper file such as `llms.txt` or `claims.json` does not by itself make a domain unmeasurable. The presence of a helper file also does not prove that an evaluated AI provider used it.

## Measurement context

Controlled AI measurement uses a versioned evidence-grounded context such as organisation/entity, sector, buyer-facing category, buyer need, decision/risk need and geography where relevant.

A completed/running cycle remains bound to the profile version under which it was created. Later context changes must not silently rewrite older evidence.

## Commercial evidence cycles

A fresh commercial evidence cycle is one coherent chain rather than an arbitrary mix of recent artifacts:

1. fresh discovery and representative site evidence;
2. semantic synthesis and measurement-context preparation;
3. controlled buyer/research AI observations;
4. interpretation and provenance evidence;
5. comparison/drift analysis where compatible evidence exists;
6. a frozen Unified Report.

Fresh discovery must produce usable representative site evidence before downstream AI measurement starts. A zero-representative-page result is a blocked state, not a successful empty report.

## Current question plans

The current Buyer Visibility Matrix v1 uses neutral, evidence-grounded buyer/research questions:

- Comprehensive Review: 60 questions;
- Monitor: 30 questions;
- Compare & Monitor: 40 questions under the fixed primary-company context.

The matrix is organized across ten decision dimensions and six stable research perspectives. Exact provider/model lanes, repetitions and required observation totals are calculated from the active plan at runtime.

Historical six-question/twenty-four-observation batteries remain historical evidence only; they are not the current commercial requirement.

## Progress and asynchronous work

A generating cycle can move through site evidence, context preparation, AI measurement, interpretation, comparison/finalization and report materialization.

Customer-facing progress should reflect actual evidence state rather than elapsed time. Useful states include queued, running, blocked, partial/recovering, completed and failed.

Already-entitled work can continue through server-side reconciliation without the customer keeping a browser tab open. The product should not invent an ETA when runtime evidence does not support one.

## Failure and repair

A recoverable provider or worker delay is processing state, not evidence that the customer needs to purchase another product.

If SemanticRisk produces a structurally invalid commercial report because required evidence was missing or the system failed to complete the funded/entitled outcome correctly, a repair cycle can use the existing Review or subscription entitlement when the runtime product marks that repair as eligible.

Runtime entitlement remains authoritative for a particular account.

## Observation, comparison and finding

An **observation** is a recorded result from site or AI measurement.

A **comparison** evaluates compatible observations across time, model lanes or domains. A difference is not automatically harmful and should not be presented as proof of a website change when capture/model conditions could explain it.

A **finding** is an evidence-backed interpretation or action derived from observations and comparison. It should preserve enough provenance to explain what was observed, what evidence supports the finding and what remains uncertain.

## Unified Report

The Unified Report is the frozen customer-facing synthesis of one completed evidence cycle.

It may summarize observations and recommendations, but the underlying persisted evidence remains the more direct source when precise explanation is required. Later presentation improvements must not silently change the historical evidence artifact.

A first valid cycle establishes a baseline. Longitudinal drift requires compatible repeat evidence. Structurally invalid reports are not normal trend baselines; when no exact valid comparison exists the correct state is **Comparable drift unavailable**.

## AI assistant rule

For "what happened?", prefer:

**runtime state → observation → evidence → comparison → finding → report summary**

For "do I need to pay again?", use current Review/subscription entitlement and repair state rather than historical credit rules or documentation inference.
