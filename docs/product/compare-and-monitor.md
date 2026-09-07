# Compare & Monitor

Compare & Monitor is the customer-facing comparative evidence view for a primary domain and a governed set of comparison domains.

It is designed to answer a practical question: **what should the customer do, what should they watch, and where does the evidence currently show an advantage or disadvantage?**

Compare & Monitor does not replace each domain's own evidence or Unified Report. It combines compatible persisted comparison measurements into a read-only comparative view.

## Comparison set

A comparison set contains:

- one primary domain;
- one or more active comparison domains;
- a versioned comparison measurement plan;
- completed comparison measurement cycles;
- evidence-linked findings derived from those cycles.

Comparison domains remain independently measurable domains. A comparison relationship does not imply ownership, control, affiliation, or permission to act on another organisation's website.

The signed-in customer must have active runtime access to the primary domain and every active comparison member before the customer workspace can expose the comparison.

## Measurement plan

Compare & Monitor uses a governed, versioned measurement plan rather than an arbitrary feature checklist.

The durable core is focused on AI-market outcomes such as:

- recognition and category association;
- buyer-question outcomes;
- recommendation and shortlist outcomes;
- citations and evidence provenance;
- interpretation accuracy or material omission;
- governance, compliance or risk-sensitive outcomes;
- change over time.

Product features can inform those measurements, but feature presence alone is not the main comparative outcome.

A plan may also contain comparison-specific and watch/context measurements. Plan versions use stable measurement keys so the product can distinguish unchanged, refined, new and retired measurements without rewriting earlier evidence.

## Direct AI answer surface and verification

For the core AI-market measurements, SemanticRisk measures the direct AI answer surface first.

Discovery and recommendation prompts should not disclose the evaluated vendor names merely to force them into the answer. Interpretation and drift measurements capture direct descriptions of the evaluated domains.

A separate web-grounded pass can then be used to verify factual support and attach citations. Direct answer outcome and supporting web evidence are separate observations and should not be collapsed into one claim.

Context/watch measurements may use web-grounded evidence where that is the measurement being performed.

Measurement/probe versions remain part of the evidence context. A materially changed probe version should not silently contaminate longitudinal drift baselines from an older version.

## Findings

Comparison findings are persisted as evidence-linked snapshots. Current customer-facing finding types are:

- **Do this** — a recommended, testable action or investigation supported by the comparison evidence;
- **Watch this** — a developing or persistent condition that should be re-measured or reviewed;
- **Advantage** — evidence showing a favourable relative outcome for the primary domain.

Every finding should remain traceable to the completed comparison cycle, measurement key, relevant domain and persisted observation evidence.

A finding may summarize or interpret evidence, but it must not recalculate authoritative measurement outcomes or invent a new composite score.

Recommendations are non-causal hypotheses unless later compatible measurement supports the claimed effect.

Repeated discovery/recommendation failures and persistent interpretation errors can be elevated because persistence across comparable observations is materially different from a one-off response.

## Evidence-bounded language

Not observing a capability, claim, recommendation or citation is not proof that the organisation lacks it.

Compare & Monitor should use evidence-bounded language such as "not observed in this measurement" rather than turning absence from the evaluated evidence into an unsupported factual claim about a competitor.

## Customer workspace view

The current customer workspace presentation is read-only. It can expose:

- an executive comparison summary;
- Do this findings;
- Watch this findings;
- Advantages;
- a collapsed measurement-evidence matrix showing the underlying comparative observations.

The current view does not by itself:

- spend a credit;
- launch a scan or comparison cycle;
- edit the comparison set;
- activate or change a measurement plan;
- grant access to a domain;
- take action against a compared organisation.

Those states and actions remain governed by their own runtime authorization and entitlement rules.

## No composite winner score

SemanticRisk should not manufacture one overall winner/rank score from heterogeneous comparison measurements unless a separately defined, governed methodology explicitly supports one.

Recognition, recommendation, citation, interpretation, governance and drift measurements can move differently. The customer should be able to see those differences rather than having them hidden inside an unexplained aggregate score.

## Runtime-state boundary

Documentation explains the Compare & Monitor contract but does not establish current comparison state.

An AI assistant must use authorized runtime state to determine:

- which comparison set is active;
- which domains the customer may access;
- which measurement-plan version is active;
- whether a comparison cycle completed or failed;
- which findings are current;
- whether the displayed evidence is compatible for longitudinal comparison;
- whether any state-changing comparison action is currently available or authorized.
