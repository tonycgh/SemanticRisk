# Evidence, Claims and Interpretation

SemanticRisk distinguishes between source evidence, extracted claims, and interpretation.

These terms should not be used interchangeably.

## Evidence

Evidence is public website material that was accessible and usable during capture.

Evidence may include text, structure, page context, metadata, and other publicly available source material used by the analysis process.

A capture result describes what was available to the analysis process. It does not establish that the captured material is objectively true.

## Claim

A claim is a statement, proposition, capability, classification, or other assertion extracted or formed by an AI system from the available evidence.

A claim is an observed model output, not an automatic statement of fact.

## Interpretation

Interpretation is the broader understanding formed from one or more claims, classifications, omissions, relationships, and contextual signals.

Interpretation can differ between models even when the underlying evidence is the same.

## Important distinction

SemanticRisk should preserve the chain:

public evidence -> model output -> extracted claim -> interpretation -> comparison/review

Do not collapse this chain into a statement that SemanticRisk has established objective truth.

## Typical review questions

- Which source evidence appears to support a claim?
- Did a model omit a material capability?
- Did a model narrow or overstate a capability?
- Did different models form materially different claims from similar evidence?
- Did the evidence change between observations?
- Did the interpretation change while the evidence appeared stable?

These questions are evidence-led review questions. They are not automatic compliance or truth determinations.
