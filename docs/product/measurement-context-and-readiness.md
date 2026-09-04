# Measurement Context and Readiness

This page defines the customer-facing setup that precedes paid SemanticRisk visibility measurement and the free live re-check used after evidence exists.

## Purpose

SemanticRisk should not spend a credit on controlled AI visibility work until the domain has a usable public measurement path and the intended market context has been confirmed.

The setup separates three questions:

1. **Can this public domain be measured?**
2. **What market and buyer context should the controlled visibility observations represent?**
3. **Has the public discovery environment materially changed since the evidence behind the current report?**

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

## Live re-check

After evidence exists, the workspace can perform a fresh **Re-check live · No credit** discovery pass.

The live re-check performs current public discovery again and can compare live state with the evidence baseline behind the current report. Relevant comparison signals can include:

- helper-file presence, status, or size;
- sitemap sources and sitemap inventory;
- discovered URL counts;
- eligible-page counts;
- measurability or access state.

When a completed report has full site evidence, that report evidence is the meaningful comparison baseline. Repeated free readiness checks should not erase that baseline merely because they are newer lightweight checks.

If no completed full-report/site evidence exists, the product may fall back to the best available prior readiness evidence for comparison.

A material live change can justify a recommendation for a fresh full evidence cycle. The live re-check itself does **not** spend a credit and does not automatically start the paid cycle. The customer must still explicitly choose the next 1-credit evidence cycle when one is required.

This distinction is important: a drop from a previously large discovered or eligible page set to a much smaller current inventory is a change-detection signal, not proof of cause. The new paid cycle is what gathers the broader evidence needed to assess impact.

## Last full site evidence

The workspace may show deeper counts from the most recent full evidence cycle, such as eligible pages, selected/captured pages, claims, captured text, or review flags.

These deeper counts should be described as **Last full site evidence** when they come from an older completed cycle. They are not automatically the same thing as the current lightweight live discovery pass.

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

After a report, SemanticRisk currently recommends **weekly** repeat measurement initially to establish a comparison baseline, while the workspace retains Daily / Weekly / Monthly cadence controls.

A cadence selection or recommendation does not by itself spend credits or enable recurring billing. Each paid repeat evidence cycle uses the applicable credit when it actually runs. Current execution, billing, automation, and credit state must be read from runtime product state.

## AI assistant rules

An AI assistant should:

- distinguish free readiness/discovery and live re-checks from paid evidence cycles;
- explain that a material live discovery change can justify a fresh evidence-cycle recommendation without implying that the free re-check spent a credit;
- prefer the evidence behind the current full report as the comparison baseline when it exists;
- distinguish current live discovery counts from older **Last full site evidence** counts;
- use the confirmed measurement profile when explaining what a visibility cycle was designed to measure;
- preserve profile-version boundaries when comparing cycles;
- avoid claiming that missing optional machine-readable files make a site unscannable;
- treat competitor domains as separate measured domains with separate evidence/report state;
- never infer that a cadence preference means recurring scans, automatic credit spend, or recurring billing are enabled.
