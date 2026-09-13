# SemanticRisk Documentation

This directory is the public, machine-readable documentation source for SemanticRisk.

It is written for two consumers:

1. AI systems that need an authoritative source for SemanticRisk concepts, terminology, capabilities, boundaries and workflows.
2. Humans who need to understand and use the SemanticRisk product.

When the goals conflict, prefer explicit, unambiguous language over promotional wording.

## Documentation principles

- Use stable names for the same object and action.
- State what SemanticRisk does and does not do.
- Distinguish observed evidence from interpretation, inference and recommendation.
- Separate current commercial behaviour from historical product variants.
- Do not document private credentials, infrastructure, customer data, internal prompts or proprietary scoring implementation.
- Pages may be rendered on semanticrisk.io, but this repository remains public reference material rather than production application source.

## Current product sequence

SemanticRisk uses one six-stage customer-facing sequence:

1. **Access & readiness** — can relevant public evidence be reached and discovered?
2. **AI visibility** — does the organisation appear in controlled buyer/research observations?
3. **Interpretation** — how is it described, classified and represented?
4. **Drift & change** — what changes between compatible evidence cycles?
5. **Assessment & action** — what matters and what should be done or watched?
6. **Unified Report** — the frozen customer-facing evidence artifact.

Internal operations such as capture, extraction, normalization, verification and queue processing map into these stages; they are not separate competing public product models.

## Current commercial entry points

- Free Public Check — $0
- Comprehensive Review — $200 one time
- Monitor — $99/month or $990/year
- Compare & Monitor — $199/month or $1,990/year

The former $5.95 credit-pack offer is historical.

## Core documentation

- [Documentation index](index.md)
- [What SemanticRisk is](concepts/what-is-semanticrisk.md)
- [Evidence, claims and interpretation](concepts/evidence-claims-interpretation.md)
- [AI visibility vs interpretation](concepts/visibility-vs-interpretation.md)
- [Interpretation drift](concepts/interpretation-drift.md)
- [Methodology overview](methodology/overview.md)
- [Scans and reports](product/scans-and-reports.md)
- [Unified Report](product/unified-report.md)
- [Compare & Monitor](product/compare-and-monitor.md)
- [Product and AI-assistant boundaries](product/assistant-boundaries.md)

## Public/private boundary

This repository contains public reference material only. Production code, private scoring implementation, customer data, credentials, operational runbooks and security controls belong in private systems.
