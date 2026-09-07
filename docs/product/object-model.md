# SemanticRisk Object Model

This page defines the main public concepts that an AI assistant should use when reasoning about the SemanticRisk product.

It is a product knowledge model, not a database schema and not an API specification.

## Domain

A **domain** is the website property SemanticRisk evaluates.

A domain can have evidence, scans, observations, claims, reports, readiness state, measurement context, monitoring state, comparison state, and account permissions associated with it.

A domain must not be treated as owned or controllable merely because it is publicly reachable. Product actions may require account authority even when measurement itself does not require ownership proof.

## Readiness

**Readiness** is the pre-scan assessment of whether SemanticRisk can reach usable public evidence for a domain and what public discovery resources are available.

Readiness can include access/crawl observations and machine-readable file discovery. It is separate from the paid evidence cycle.

## Measurement profile

A **measurement profile** is the confirmed context used to frame controlled AI visibility observations for a domain.

It can describe the market/category, buyer need, decision/risk need, geography when relevant, and comparison context.

Measurement profiles are versioned so earlier evidence retains the context under which it was collected. A new profile version must not silently rewrite an older visibility cycle.

## Portfolio / comparison domain

A **portfolio** is the customer's ordered set of measurable domains in the workspace.

One domain can be treated as the primary domain and others as comparison or competitor domains. Comparison domains remain independent measurable domains with their own evidence and report state.

A comparison relationship does not establish ownership, control, affiliation, or permission to act on another organisation's website.

## Comparison set

A **comparison set** is a governed grouping of one primary domain and active comparison domains used for comparative measurement.

Customer access to a comparison view depends on runtime authorization for the primary domain and every active comparison member.

## Comparison measurement plan

A **comparison measurement plan** is the versioned set of comparative measurements applied to a comparison set.

The durable core focuses on AI-market outcomes such as recognition, category association, buyer-question outcomes, recommendations, citations, interpretation, governance/risk-sensitive outcomes and change over time.

Stable measurement keys preserve longitudinal meaning across plan versions and allow measurements to be classified as unchanged, refined, new or retired.

## Comparison cycle

A **comparison cycle** is a completed or failed execution of an active comparison measurement plan across the authorized comparison set.

For core AI-market measurements, the direct AI answer surface can be recorded first and a separate web-grounded verification pass can attach factual support and citations. Direct-answer outcome and supporting evidence remain separate observation layers.

Probe or measurement versions are part of the cycle context and should not be mixed silently when establishing longitudinal drift.

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

Observations can be compared over time, across models, or across domains when the measurement context is compatible.

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

**Monitoring** is recurring observation of a domain or comparison over time.

Monitoring creates the repeated evidence needed to identify changes rather than relying on a single snapshot.

Monitoring state can include whether recurring monitoring is enabled and the cadence at which it is configured to run.

A cadence preference or recommendation must not be treated as proof that recurring scans, automatic credit spend, or recurring billing are enabled.

## Report

A **report** is a user-facing synthesis of SemanticRisk evidence, observations, comparisons, findings, and recommendations.

Reports are outputs derived from the underlying observations. They should not be treated as the underlying source record when more direct evidence is available.

## Finding

A **finding** is an evidence-backed issue, change, comparison, advantage, or pattern surfaced for review.

A finding should distinguish observation from conclusion and should preserve enough context for a human or AI assistant to explain why it was surfaced.

Compare & Monitor currently presents evidence-linked findings as **Do this**, **Watch this**, and **Advantage**. Findings must not invent composite measurement outcomes or turn "not observed" evidence into proof that a competitor lacks a capability.

## Account and entitlement

An **account** represents the authenticated user or organisation context from which product access is evaluated.

An **entitlement** determines whether a product capability is available to that account or domain.

Documentation may explain a capability, but documentation alone does not grant permission to execute it. Runtime authentication, domain access, credit/entitlement state, and action-specific controls remain authoritative.

The current Compare & Monitor customer view is read-only and does not itself spend credits, launch comparison cycles, edit comparison membership, activate plans, or grant access.

## Relationship summary

A useful reasoning chain is:

**Domain → Readiness → Measurement profile → Evidence cycle → Observation → Claim / Interpretation → Comparison / Drift → Finding → Report / Monitoring**

Comparative reasoning can additionally follow:

**Authorized comparison domains → Comparison set → Versioned measurement plan → Comparison cycle → Evidence-linked findings → Compare & Monitor view**

Portfolio relationships connect independently measured domains for comparison. Account, role authority, credit/entitlement state, and action-specific controls govern which operations can be performed around those objects.
