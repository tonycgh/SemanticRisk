# Measurement Context and Readiness

This page defines the customer-facing setup that precedes paid SemanticRisk visibility measurement and the free live re-check used after evidence exists.

## Purpose

SemanticRisk should not spend a credit on controlled AI visibility work until the domain has a usable public measurement path and a defensible market context is available.

The setup separates three questions:

1. **Can this public domain be measured?**
2. **What market and buyer context should the controlled visibility observations represent?**
3. **Has newer public evidence materially changed the setup that should drive the next comparable cycle?**

## Free readiness check

Before paid AI work starts, SemanticRisk can perform a readiness and discovery check for the selected domain.

The readiness check can inspect whether usable public content is reachable and whether common machine-readable discovery resources appear to be present, including `robots.txt`, sitemap discovery, `llms.txt`, `llms-full.txt`, `claims.json`, and `claims.txt`.

A missing `llms.txt`, `claims.json`, or similar optional machine-readable file does **not** by itself make a domain unscannable. The readiness check does not consume a paid scan credit merely because it is checking access or discovery files.

## Live re-check

After evidence exists, the workspace can perform a fresh **Re-check live · No credit** discovery pass.

The live re-check performs current public discovery again and can compare live state with the evidence baseline behind the current report. Relevant comparison signals can include helper-file presence/status/size, sitemap sources and inventory, discovered URL counts, eligible-page counts, and measurability or access state.

When a completed report has full site evidence, that report evidence is the meaningful comparison baseline. Repeated free readiness checks should not erase that baseline merely because they are newer lightweight checks.

A material live change can justify a recommendation for a fresh full evidence cycle. The live re-check itself does **not** spend a credit and does not automatically start the paid cycle. The customer must still explicitly choose the next 1-credit evidence cycle when one is required.

## Last full site evidence

The workspace may show deeper counts from the most recent full evidence cycle, such as eligible pages, selected/captured pages, claims, captured text, or review flags. These deeper counts should be described as **Last full site evidence** when they come from an older completed cycle.

## Machine-file validation

SemanticRisk does not treat every HTTP 2xx response as proof that a machine-readable file exists. HTML fallback pages, invalid or empty JSON, empty text resources, or unsuitable redirects can be rejected as false positives.

## AI measurement setup

SemanticRisk uses a measurement profile to frame the controlled buyer-intent observations for a domain. The profile can include organisation/entity, broad sector, market/category, buyer decision task, decision/trust factors, and geography when relevant.

When governed taxonomy provides a defensible market category, SemanticRisk can build the standard buyer-prompt setup automatically. The customer does not have to author the six prompts manually.

When an active profile is unavailable, supported product evidence can also be used to recover or propose the measurement context. For Compare & Monitor, the primary-company context may be resolved from compatible historical visibility metadata, governed taxonomy, or stored public claim evidence.

When stored claim evidence produces a complete **high-confidence** AI classification, the current product can persist that classification as the active primary measurement profile automatically so the comparison can proceed. Medium- or low-confidence classification remains a proposal for human review and must not start paid work when no defensible current context is available.

When no defensible context can be resolved, the workspace blocks paid AI measurement before a credit is used and asks for meaningful market-category confirmation. The buyer task and decision/trust wording can then be derived and shown for review.

The measurement profile is versioned. A completed or running visibility cycle remains bound to the profile version used when that cycle was created. Changing the setup later must not silently rewrite earlier evidence.

## Fresh evidence-derived context

A fresh coherent paid cycle captures and synthesizes site evidence before controlled visibility observations begin. When that same-cycle evidence supports it, SemanticRisk can classify the organisation/entity, broad sector, buyer-facing market/category, buyer decision need, decision/risk need, and geography before launching the visibility battery.

High-confidence context that is owned by SemanticRisk's evidence classification can be persisted automatically as a new profile version. A prompt-affecting automatic change creates a new immutable version rather than rewriting the meaning of earlier observations.

Automatic refinement is deliberately bounded. A customer-confirmed market/category should not be silently replaced merely because a classifier proposes another label, and genuinely custom buyer-task or decision/risk wording should be preserved. Legacy or clearly generic wording can be improved when the fresh evidence supports a more specific formulation.

Broad geography terms such as `global`, `worldwide`, or `international` are treated as **unbounded geography**, not as literal locations to insert into buyer prompts. This prevents constructions such as “in global.”

Lower-confidence evidence should not silently replace a defensible current profile. If no usable context exists, the product should require review before paid AI measurement proceeds.

## Compare & Monitor primary context

Compare & Monitor uses the primary company's governed measurement context across the selected comparison set. Opening or measuring a competitor does not transfer comparison-primary status to that competitor and does not require the competitor to define its own comparison category.

Before fresh paid comparison evidence is queued, SemanticRisk preflights the primary AI Measurement Plan. If the primary context is unresolved, the comparison is stopped before credits are spent.

Competitor evidence remains separate from the primary company's profile. A comparison run can apply the primary context to a competitor measurement for comparability without redefining the competitor's independent long-term measurement profile.

## Review latest scan evidence

After a completed site audit produces newer captured public claims than the currently saved measurement profile, the workspace can flag **New scan evidence available · review setup before next cycle**.

The measurement-setup assistant can compare the current category, buyer task, decision/trust factors, and geography with the newest stored public claims. Its proposal can include evidence signals, confidence, and a reason to keep or change the current setup.

This review is evidence-led rather than generic category boilerplate: the assistant should use only the supplied public-site evidence and should not invent services, customers, certifications, capabilities, locations, market scope, risks, or outcomes.

Reviewing the latest scan evidence does **not** use a credit. Saving a revised profile does not itself start a paid evidence cycle. If the setup changes materially, the revised version applies to a later explicitly requested cycle; the current completed report remains bound to its original profile and evidence.

If the latest evidence supports the current setup, the assistant may say that no setup change is required before the next comparable cycle.

## Comparison portfolio

A workspace can include the customer's primary domain and additional comparison or competitor domains. Comparison domains are normal measurable domains, not annotations attached to the primary domain. Each domain has its own evidence state and Unified Report.

Adding or selecting a competitor does not itself spend a credit. Whether a selected domain needs a new credit-funded evidence cycle depends on the account's current report/evidence state and the Compare & Monitor evidence mode. See [Compare & Monitor](compare-and-monitor.md).

## Repeat-measurement preference

After a report, SemanticRisk currently recommends **weekly** repeat measurement initially to establish a comparison baseline, while the workspace retains Daily / Weekly / Monthly cadence controls.

A cadence selection or recommendation does not by itself spend credits or enable recurring billing. Current execution, billing, automation, and credit state must be read from runtime product state.

## AI assistant rules

An AI assistant should distinguish free readiness, live re-check, measurement-setup review, same-cycle evidence classification, comparison-context preflight and paid evidence cycles; use current runtime evidence/profile state rather than infer freshness; preserve profile-version boundaries; preserve customer-confirmed or genuinely custom context unless runtime state says it was changed; interpret broad global-scope terms as unbounded geography rather than literal prompt locations; avoid treating optional machine files as visibility guarantees; and never imply that reviewing setup, automatically resolving a high-confidence context, or selecting a comparison domain has itself spent an additional credit or started another domain scan.
