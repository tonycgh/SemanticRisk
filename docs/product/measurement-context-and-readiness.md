# Measurement Context and Readiness

This page defines the customer-facing setup that precedes paid SemanticRisk visibility measurement.

## Purpose

SemanticRisk should not spend a credit on controlled AI visibility work until the domain has a usable public measurement path and the intended market context has been confirmed.

The setup separates two questions:

1. **Can this public domain be measured?**
2. **What market and buyer context should the controlled visibility observations represent?**

## Free readiness check

Before paid AI work starts, SemanticRisk can perform a readiness and discovery check for the selected domain.

The readiness check can inspect whether usable public content is reachable and whether common machine-readable discovery resources appear to be present, including:

- `robots.txt`;
- sitemap discovery;
- `llms.txt`;
- `llms-full.txt`;
- `claims.json`;
- `claims.txt`.

A missing `llms.txt`, `claims.json`, or similar optional machine-readable file does **not** by itself make a domain unscannable.

The readiness check does not consume a paid scan credit merely because it is checking access or discovery files.

## Machine-file validation

SemanticRisk does not treat every HTTP 2xx response as proof that a machine-readable file exists.

A response can be rejected as a false positive when, for example:

- a supposed text or JSON file is actually an HTML fallback page;
- a JSON resource is empty or invalid JSON;
- a text resource is empty;
- a redirected response does not directly provide the requested resource.

The purpose is to report actual machine-readable availability rather than a website's generic catch-all response.

## Confirmed measurement context

Before paid Buyer Visibility Core work starts for a workspace domain, the customer confirms the measurement context used to frame the controlled buyer-intent observations.

The context can include:

- market/category;
- buyer need;
- risk or decision need;
- geography when relevant;
- comparison domains.

The confirmed context is versioned. A completed or running visibility cycle is bound to the measurement-profile version used when that cycle was created.

Changing the context later must not silently rewrite the meaning of earlier evidence. A later cycle can use a newer confirmed version while prior observations retain their original context.

## Comparison portfolio

A workspace can include the customer's primary domain and additional comparison or competitor domains.

Comparison domains are normal measurable domains, not annotations attached to the primary domain. Each domain has its own evidence state and Unified Report.

Adding a competitor to the portfolio does not itself spend a credit. When the customer chooses to run a paid evidence cycle for that competitor, the normal per-domain credit rules apply.

The product may recommend adding multiple competitors to improve comparative usefulness. Such guidance is a recommendation, not a requirement to purchase additional scans.

## Repeat-measurement preference

After a report, SemanticRisk may suggest a daily, weekly, or monthly repeat-measurement cadence based on the evidence or customer goal.

Selecting a cadence preference does not by itself spend credits or enable recurring billing. Current execution, billing, automation, and credit state must be read from runtime product state.

## AI assistant rules

An AI assistant should:

- distinguish free readiness/discovery checks from paid evidence cycles;
- use the confirmed measurement profile when explaining what a visibility cycle was designed to measure;
- preserve profile-version boundaries when comparing cycles;
- avoid claiming that missing optional machine-readable files make a site unscannable;
- treat competitor domains as separate measured domains with separate evidence/report state;
- never infer that a cadence preference means recurring scans, automatic credit spend, or recurring billing are enabled.
