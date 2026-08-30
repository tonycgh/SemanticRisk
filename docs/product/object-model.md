# SemanticRisk Object Model

This page defines the main public concepts that an AI assistant should use when reasoning about the SemanticRisk product.

It is a product knowledge model, not a database schema and not an API specification.

## Domain

A **domain** is the website property SemanticRisk evaluates.

A domain can have evidence, scans, observations, claims, reports, monitoring state, and account permissions associated with it.

A domain must not be treated as owned or controllable merely because it is publicly reachable. Product actions may require verification and account authority.

## Evidence

**Evidence** is captured public website material or observable access/crawl information used during SemanticRisk evaluation.

Evidence can include page content and capture/accessibility conditions.

Evidence is not equivalent to objective truth. It is the material available to the evaluation process.

## Scan

A **scan** is a bounded evaluation run against a domain.

A scan can capture evidence and produce structured observations used by later comparison, reporting, monitoring, or interpretation analysis.

A scan is an observation event. It does not modify the target website.

## Observation

An **observation** is a recorded result from a scan or model evaluation.

Observations can be compared over time or across models.

## Claim

A **claim** is a structured statement extracted or formed by an AI model from available evidence.

A claim records what the model appeared to understand or assert. A SemanticRisk claim is not automatically an established fact, endorsement, certification, or legal finding.

## Interpretation

An **interpretation** is the broader meaning or classification formed from one or more claims and the evidence available to the model.

SemanticRisk evaluates interpretation because two systems can access similar evidence while forming materially different descriptions, classifications, omissions, or emphases.

## Drift

**Interpretation drift** is a material change between observations over time.

A detected difference is not automatically harmful. SemanticRisk separates possible content change, capture change, extraction change, model disagreement, and other causes where evidence allows.

## Monitoring

**Monitoring** is recurring observation of a domain over time.

Monitoring creates the repeated evidence needed to identify changes rather than relying on a single snapshot.

Monitoring state can include whether recurring monitoring is enabled and the cadence at which it is configured to run.

## Report

A **report** is a user-facing synthesis of SemanticRisk evidence, observations, comparisons, findings, and recommendations.

Reports are outputs derived from the underlying observations. They should not be treated as the underlying source record when more direct evidence is available.

## Finding

A **finding** is an evidence-backed issue, change, comparison, or pattern surfaced for review.

A finding should distinguish observation from conclusion and should preserve enough context for a human or AI assistant to explain why it was surfaced.

## Account and entitlement

An **account** represents the authenticated user or organisation context from which product access is evaluated.

An **entitlement** determines whether a product capability is available to that account or domain.

Documentation may explain a capability, but documentation alone does not grant permission to execute it. Runtime authentication, domain authority, plan entitlement, verification state, and action-specific controls remain authoritative.

## Relationship summary

A useful reasoning chain is:

**Domain → Evidence → Scan → Observation → Claim / Interpretation → Comparison / Drift → Finding → Report / Monitoring**

Account, verification, role authority, and entitlement govern which actions can be performed around those objects.
