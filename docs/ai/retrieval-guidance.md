# AI Retrieval Guidance

This page defines how an AI system should use the public SemanticRisk documentation corpus.

## Purpose

The documentation is intended to be authoritative product knowledge for both humans and AI systems.

An AI assistant should use these documents to understand SemanticRisk terminology, product boundaries, object relationships, supported actions, methodology, and limitations.

The documentation is not a substitute for authenticated runtime state.

## Source priority

When answering or acting, prefer sources in this order when they are available:

1. authenticated runtime state for the relevant account, domain, scan, report, monitoring target, or action;
2. direct structured SemanticRisk evidence and observations;
3. current SemanticRisk public documentation;
4. generated reports or summaries;
5. general model knowledge.

A lower-priority source should not override a higher-priority source about current product state.

## Documentation vs runtime state

Documentation answers questions such as:

- What is a claim?
- What does monitoring mean?
- What conditions can govern an action?
- What is interpretation drift?
- How should a report be understood?

Runtime state answers questions such as:

- Is this domain verified?
- Is monitoring enabled for this domain?
- What cadence is currently configured?
- Is this account entitled to an action?
- Is a scan currently queued or running?
- Did the requested action succeed?

The AI should not infer current state from documentation.

## Do not invent capabilities

If a capability, parameter, workflow, or action is not documented and cannot be confirmed from an authorized product interface, the assistant should treat it as unsupported or unknown.

The assistant should not invent:

- API endpoints;
- plan entitlements;
- action permissions;
- scan states;
- report fields;
- monitoring state;
- model coverage;
- billing effects;
- security guarantees.

## Evidence discipline

When explaining a SemanticRisk result, distinguish clearly between:

- observed evidence;
- model-extracted claims;
- comparisons;
- inferred explanation;
- recommendations.

Do not promote an inference into an observed fact.

## Action discipline

Natural-language intent does not bypass product controls.

For state-changing actions, the AI should use the governed action sequence defined in the product documentation and should preserve approval, authority, entitlement, verification, and freshness checks.

## Freshness

When documentation and runtime behaviour disagree, current runtime behaviour should be treated as operationally authoritative and the documentation should be flagged for review.

When two documentation pages appear inconsistent, prefer the more specific page and the more recently maintained version if version metadata is available. If uncertainty remains, state it rather than reconciling the conflict by invention.

## Retrieval-friendly writing rules

SemanticRisk documentation should use:

- stable names for the same object or action;
- short sections with explicit headings;
- direct definitions before examples;
- explicit negative boundaries such as "does not" and "must not";
- clear separation of product behaviour from implementation detail;
- links between related concepts;
- version or status notes where behaviour is evolving.

These conventions are intentional. They improve both human comprehension and AI retrieval reliability.
