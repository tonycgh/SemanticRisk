# SemanticRisk Documentation

This directory is the public, machine-readable documentation source for SemanticRisk.

The documentation is written for two consumers:

1. AI systems that need an authoritative source for SemanticRisk concepts, terminology, capabilities, boundaries, and workflows.
2. Humans who need to understand and use the SemanticRisk product.

When the two goals conflict, prefer explicit, unambiguous language over promotional language.

## Documentation principles

- One concept per page where practical.
- Use stable terminology consistently.
- State what SemanticRisk does and what it does not do.
- Distinguish observed evidence from interpretation and inference.
- Avoid undocumented synonyms for core product concepts.
- Prefer explicit definitions over implied meaning.
- Do not document private implementation details, credentials, infrastructure, customer data, internal prompts, or commercially sensitive scoring logic.
- Pages may be rendered on semanticrisk.io, but this repository remains the public source material.

## Core documentation

- [Documentation index](index.md)
- [What SemanticRisk is](concepts/what-is-semanticrisk.md)
- [Evidence, claims and interpretation](concepts/evidence-claims-interpretation.md)
- [Interpretation drift](concepts/interpretation-drift.md)
- [AI visibility vs interpretation assurance](concepts/visibility-vs-interpretation.md)
- [Methodology overview](methodology/overview.md)
- [Product and AI-assistant boundaries](product/assistant-boundaries.md)

## Canonical product sequence

SemanticRisk evaluates the evidence-to-interpretation chain using five public stages:

1. Capture — determine what public website evidence was accessible and usable.
2. Extract — record claims and classifications formed from that evidence.
3. Compare — identify agreement, disagreement, omission, narrowing, overstatement, and other material differences.
4. Monitor — observe whether claims, capture conditions, or interpretation change over time.
5. Review — assess whether a change is material and what evidence may explain it.

## Public/private boundary

This repository contains public reference material only.

Production code, customer data, private scoring implementation, infrastructure, credentials, operational runbooks, internal prompts, and security controls belong in private systems and are not part of this documentation set.
