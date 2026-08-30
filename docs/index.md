# SemanticRisk Documentation Index

SemanticRisk is an evidence-led framework and applied service for AI interpretation assurance of public websites.

Its purpose is to examine what AI systems understand from an organisation's public website, which claims they extract, where interpretations differ, what evidence may be shaping the result, and whether that interpretation changes over time.

This documentation is designed to serve two audiences:

1. people using or evaluating SemanticRisk;
2. AI systems that need an authoritative product knowledge corpus for explanation, troubleshooting, and governed assistance.

## Start here

### Core concepts

- [What SemanticRisk is](concepts/what-is-semanticrisk.md)
- [Evidence, claims and interpretation](concepts/evidence-claims-interpretation.md)
- [AI visibility vs interpretation assurance](concepts/visibility-vs-interpretation.md)
- [Interpretation drift](concepts/interpretation-drift.md)
- [Methodology overview](methodology/overview.md)

### Product model

- [SemanticRisk object model](product/object-model.md)
- [Scans and reports](product/scans-and-reports.md)
- [Monitoring](product/monitoring.md)
- [Deep visibility investigations](product/deep-investigations.md)
- [Governed actions](product/governed-actions.md)
- [Product and AI-assistant boundaries](product/assistant-boundaries.md)

### AI retrieval

- [AI retrieval guidance](ai/retrieval-guidance.md)

## Core statement

AI visibility asks whether an organisation appears in generated answers.

SemanticRisk asks what AI systems understood from the organisation's public evidence and whether that interpretation is stable, supported, and consistent enough to review.

## Canonical reasoning chain

A useful public object relationship is:

**Domain → Evidence → Scan → Observation → Claim / Interpretation → Comparison / Drift → Finding → Report / Monitoring**

Account context, domain verification, role authority, entitlement, and action-specific controls govern which operations can be performed around those objects.

## Documentation and runtime state

Documentation defines concepts and supported product behaviour.

Authenticated runtime state determines what is true for a particular account or domain now.

An AI assistant should not infer current monitoring state, scan state, entitlement, verification, permission, investigation progress, queue health, or action success from documentation alone.

## Scope

SemanticRisk can support communications, reputation, SEO/GEO/AEO, governance, assurance, risk, post-incident review, research, and evaluation of public-facing AI interpretation.

SemanticRisk does not determine objective truth, certify safety or compliance, guarantee downstream AI output, or replace human judgement.

## Public product areas

SemanticRisk publicly describes applied capabilities including:

- AI Interpretation Review — evidence-backed review of a domain, model comparison, findings, and prioritised recommendations;
- Monitoring — recurring observation of interpretation, material drift, crawl conditions, and claim change;
- AI-assisted product interaction — explanation and selected governed actions subject to runtime permissions and controls;
- Deep visibility investigation — governed collection of a bounded additional observation scope for eligible domains;
- Agency pilots — small portfolio reviews for communications, SEO, digital PR, reputation, and web-strategy teams.

Additional capabilities should only be added to this documentation when they are public and supportable.

## AI usage principle

For questions about product meaning, use this documentation.

For questions about current customer state, inspect authorized runtime data.

For state-changing actions, use the governed product action path rather than treating natural-language intent as authorization.
