# SemanticRisk Documentation Maintenance Contract

The SemanticRisk documentation is part of the product surface and the public knowledge corpus used by AI-assisted workflows.

## Operating rule

A customer-facing product change is not documentation-complete until the public knowledge model has been reviewed for consistency.

Review documentation when a change affects:

- product promise or positioning;
- pricing, plans or entitlement;
- funnel or primary calls to action;
- measurement method, question population or report contents;
- readiness, scans, monitoring, comparison or failure semantics;
- public terminology or methodology;
- public/API route ownership visible to customers or AI systems;
- AI-assistant actions, explanations or boundaries.

## Maintenance cadence

Use **event-driven documentation updates** as the primary rule: when the public contract changes, update the affected documentation in the same development cycle.

Periodic drift review is a backstop, not a substitute for event-driven maintenance. A separate repetitive documentation reminder is unnecessary when routine production/revenue review already checks for documentation drift.

## Suggested review flow

1. Review the merged customer-facing change and the canonical private product contract.
2. Identify which public concepts, prices, question counts, routes, states or boundaries changed.
3. Update the relevant public documentation pages.
4. Update `llms.txt`, `CURRENT_PRODUCT.md`, the documentation index or discovery claims when the canonical public knowledge model changed.
5. Mark retired behaviour historical instead of leaving two active definitions.
6. Record material public knowledge changes in `CHANGELOG.md`.

## Source priority

When sources disagree, prefer:

1. current production/runtime behaviour for account- or cycle-specific state;
2. current private canonical product and measurement contracts;
3. current public SemanticRisk documentation;
4. historical roadmaps, reports and summaries;
5. general model knowledge.

Public documentation must not expose private implementation details merely because those details were used to verify the public contract.

## Definition of done

For customer-facing changes, documentation is complete when the affected public pages are updated or the change was explicitly reviewed and determined not to affect the public knowledge model.

The goal is not documentation volume. The goal is one current, authoritative, retrieval-friendly model of how SemanticRisk works.
