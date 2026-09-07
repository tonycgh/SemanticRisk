# Representation, grounding and claim assessment

Updated: 7 September 2026

SemanticRisk separates the answer an evaluated AI system produces from the evidence later used to verify that answer. This prevents current web evidence from silently replacing the AI behaviour that was actually measured.

## Direct answer surface

For configured direct-answer measurements, SemanticRisk records the answer before supplying a current web-search tool to that measured answer call. The stored evidence can include the prompt, provider/model, measurement/probe version, provider response identifier and observable tool mode.

This is an **observable execution condition**, not a claim about a model's training data, hidden retrieval, memory or internal reasoning.

## Grounded verification

A separate verification pass can then use current public evidence to assess factual support and add provenance. The verification pass must not rewrite the recorded direct answer into what current web evidence suggests the AI should have said.

For first-party facts such as current features, pricing, policies and official statements, the organisation's own current public material may be the primary authority. Claims about reputation, market position, customer sentiment or third-party validation can require independent evidence.

A missing public claim is not proof that an organisation lacks a capability.

## Representation / Grounding Gap

A material difference between the recorded AI representation and current reference evidence is a **Representation / Grounding Gap**.

This is not automatically semantic drift. Drift requires a later compatible observation and describes change over time.

## Claim assessment vocabulary

Where evidence permits, SemanticRisk uses bounded verdicts such as:

- **Supported** — authoritative evidence supports the material statement.
- **Partially supported** — important parts are supported, but a qualifier or component is not established.
- **Unsupported / unverified** — supporting evidence was not found in the measured evidence set.
- **Contradicted** — current authoritative evidence materially conflicts with the statement.
- **Outdated / stale** — the statement appears to reflect superseded evidence.
- **Unverifiable** — available evidence is insufficient for a reliable verdict.

SemanticRisk does not treat every uncited or unsupported statement as a hallucination. Stronger wording such as **likely hallucinated** should be used only when the stored evidence supports that conclusion.

## Longitudinal comparability

Material changes to a measurement prompt or execution surface require a new compatible probe/version and a new baseline where necessary. Earlier evidence remains historical evidence, but SemanticRisk should not present a methodology change as customer or market drift.

## Report boundary

Where this evidence is available, the Unified Report should preserve the chain:

**Observed AI Claim → Reference Evidence → SemanticRisk Assessment**

The report may summarize findings for decision-making, but the underlying evidence and measurement boundary should remain inspectable.