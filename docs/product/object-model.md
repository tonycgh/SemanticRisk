# SemanticRisk Object Model

This page defines the main public concepts an AI assistant should use when reasoning about SemanticRisk. It is a product knowledge model, not a database schema or API specification.

## Domain

A **domain** is the public website property SemanticRisk evaluates. Public measurement does not require proof of ownership, although authenticated account actions remain governed by entitlement and permissions.

## Readiness

**Readiness** is the pre-measurement assessment of whether useful public evidence is reachable and what public discovery resources are available.

## Measurement profile

A **measurement profile** is the versioned context used to frame controlled AI observations. It can include organisation/entity, sector, buyer-facing category, buyer need, decision/risk need and geography where relevant.

Earlier evidence remains bound to the profile version under which it was collected.

## Evidence cycle

An **evidence cycle** is one coherent bounded measurement generation linking representative site evidence, measurement context, AI observations, interpretation/provenance evidence and a Unified Report.

## Observation

An **observation** is a recorded site or AI measurement result used by later comparison, reporting and drift analysis.

## Claim

A **claim** is a structured statement extracted or formed from available evidence. It records what a model appeared to understand or assert; it is not automatically objective truth, certification or legal finding.

## Interpretation

An **interpretation** is the broader meaning or classification formed from claims and evidence.

## Drift

**Interpretation drift** is a material change between compatible observations over time. A detected difference is not automatically harmful and can reflect content, capture, extraction, model or methodology changes.

## Portfolio and comparison set

A **portfolio** is the customer's measurable domain set. For Compare & Monitor, one domain is fixed as the primary domain and up to three selected competitors can form the active comparison set.

A **comparison set** is the governed grouping of the fixed primary domain plus selected comparison domains.

## Comparison measurement plan

A **comparison measurement plan** is the versioned set of comparative questions/measurements applied under the fixed primary-company context.

## Comparison cycle

A **comparison cycle** is an execution of the active comparison plan across the authorized selected set.

## Finding

A **finding** is an evidence-backed issue, change, comparison, advantage or action surfaced for review. Customer-facing comparison findings include **Do this**, **Watch this**, and **Advantage**.

## Unified Report

A **Unified Report** is the frozen customer-facing synthesis of a completed evidence cycle. It is downstream of the underlying evidence and should not be treated as the only source record when direct observations are available.

## Monitoring

**Monitoring** is recurring entitled observation that creates compatible evidence over time. Current public subscription products are Monitor and Compare & Monitor.

A cadence recommendation is not proof that a particular account currently has scheduled work enabled; runtime state remains authoritative.

## Account and entitlement

An **account** is the authenticated user/organisation context.

An **entitlement** determines which commercial capability is available, for example a Comprehensive Review grant or an active Monitor/Compare & Monitor subscription. Historical credit/grant records can exist for compatibility but are not the current public commercial model.

## Relationship summary

**Domain → Readiness → Measurement profile → Evidence cycle → Observation → Claim / Interpretation → Comparison / Drift → Finding → Unified Report → Monitoring**

Comparative reasoning additionally follows:

**Fixed primary + selected competitors → Comparison set → Versioned comparison plan → Comparison cycle → Evidence-linked findings → Primary Unified Report**
