# SemanticRisk Documentation Maintenance Contract

The SemanticRisk documentation is part of the product surface and part of the authoritative knowledge corpus used by AI-assisted workflows.

## Operating rule

Customer-facing product changes should trigger a documentation review before the work is considered complete.

A documentation review is required when a change affects any of the following:

- customer-visible capabilities;
- domain, scan, claim, evidence, finding, report, monitoring, or account behaviour;
- entitlement or plan requirements;
- AI-assistant actions or explanations;
- approval requirements or governed-action behaviour;
- supported cadences, states, limits, or failure semantics;
- public methodology or terminology;
- public API behaviour;
- billing-visible effects;
- privacy, authority, verification, or access boundaries.

## Daily review cadence

During active product development, review the documentation against current production changes at least once per development day.

The daily review does not require a documentation change when product behaviour has not changed. Its purpose is to detect documentation drift early.

Suggested review flow:

1. Review recent production commits and merged changes.
2. Identify changes that alter a public concept, workflow, state, entitlement, or AI action.
3. Update the relevant canonical documentation page.
4. Update `llms.txt` or the documentation index when a new canonical page is introduced.
5. Avoid documenting experimental or private implementation details as supported public behaviour.
6. Record material public-documentation changes in `CHANGELOG.md`.

## Source priority

Documentation must be grounded in current supported product behaviour.

When sources disagree, use this priority:

1. current production/runtime behaviour;
2. current private implementation and entitlement rules;
3. current public SemanticRisk documentation;
4. historical roadmaps, reports, and summaries;
5. general model knowledge.

Public documentation must not expose private implementation details merely because they were used to verify the public contract.

## Definition of done

For customer-facing changes, the product change is documentation-complete when one of these is true:

- relevant documentation has been updated; or
- the change was reviewed and explicitly determined not to affect the public knowledge model.

## AI-specific requirement

Documentation should answer the questions an AI assistant needs in order to reason safely:

- What is this object or capability?
- What current state must be checked at runtime?
- What may the user ask to do?
- What prerequisites apply?
- Does the action require approval?
- What can change as a result?
- What explicitly does not change?
- What failure or stale-state conditions can occur?
- What must not be inferred from documentation alone?

The goal is not documentation volume. The goal is a current, authoritative, retrieval-friendly model of how SemanticRisk works.
