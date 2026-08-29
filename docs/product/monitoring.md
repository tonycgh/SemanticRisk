# Monitoring

SemanticRisk monitoring is recurring observation of a domain so interpretation, evidence, claims, and access conditions can be compared over time.

## Purpose

A single scan is a snapshot. Monitoring creates a sequence of observations.

That sequence can support detection and explanation of:

- interpretation change;
- claim change;
- model disagreement;
- content change;
- capture or crawl regression;
- other material differences between observations.

Monitoring does not guarantee that every downstream AI system will behave consistently or that every change will be detected immediately.

## Monitoring state

For product reasoning, monitoring has at least two important properties:

- **enabled / disabled**;
- **cadence** when enabled.

The current product supports governed cadence choices including daily, weekly, monthly, and disabled states.

The account-facing product state is authoritative. Documentation should not be used to infer that monitoring is active for a particular domain.

## Eligibility

Recurring monitoring is a paid capability and can be subject to plan entitlement.

A domain may also need to be verified, and the requesting user may need owner or administrative authority before recurring monitoring settings can be changed.

If a user lacks eligibility, the assistant should explain the blocking condition rather than imply that the change was made.

## Changing monitoring

A monitoring cadence change is a controlled Amber action.

The expected flow is:

1. inspect current monitoring state;
2. prepare the proposed target cadence;
3. explain the effect;
4. validate domain verification, authority, and plan eligibility;
5. obtain explicit approval;
6. confirm the proposal is still current;
7. execute through the governed product action;
8. report the resulting state.

Nothing should be represented as changed merely because the proposal was prepared.

## Disabling monitoring

Disabling monitoring stops recurring monitoring for the selected domain.

Disabling future recurring work does not mean historical observations, reports, or previously captured evidence have been deleted.

Deletion and retention are separate concepts and should not be inferred from a monitoring-state change.

## AI assistant guidance

When asked questions such as "Are you monitoring my domain?" or "How often are you scanning me?", the assistant should inspect current account/domain state when that data is available.

When asked to change monitoring, the assistant should use the governed action path rather than relying on documentation alone.
