# Compare & Monitor

Compare & Monitor is the customer-facing comparative evidence workflow for a fixed primary domain and a governed set of comparison domains.

It is designed to answer a practical question: **what should the customer do, what should they watch, and where does the evidence currently show an advantage or disadvantage?**

Compare & Monitor does not replace each domain's own evidence or Unified Report. It combines compatible domain evidence under one primary-company measurement context and produces a comparison cycle, evidence-linked findings, and a comparison section in the primary domain's Unified Report.

## Fixed primary and comparison selection

A comparison set contains:

- one fixed primary domain representing **My company**;
- one or more active comparison domains selected from domains the customer can access in the workspace;
- a versioned comparison measurement plan;
- completed comparison measurement cycles;
- evidence-linked findings derived from those cycles.

Opening a competitor domain for inspection does not make that domain the comparison primary. The primary company's governed measurement context remains the anchor for the comparison.

Comparison domains remain independently measurable domains. A comparison relationship does not imply ownership, control, affiliation, or permission to act on another organisation's website.

The signed-in customer must have active runtime access to the primary domain and every active comparison member before the customer workspace can expose or execute the comparison.

Selecting or deselecting a comparison domain changes the customer's comparison set. Selection itself does not spend a credit or launch a scan.

## Evidence modes and credits

Compare & Monitor separates **domain evidence acquisition** from **comparison assembly**.

The customer can choose between two evidence modes before fresh domain work is requested:

- **Use current evidence where available** — reuse still-current paid reports already granted to this account and request fresh evidence only for selected domains that need it. The displayed credit cost is the number of selected domains that require fresh evidence.
- **Force fresh evidence for all selected domains** — request one new evidence cycle for every selected domain. The displayed credit cost is one credit per selected domain.

A current report belonging to another account is not treated as this customer's already-paid current evidence unless the runtime entitlement/grant rules make it current for this account.

If **every selected domain already has current paid evidence for the account**, SemanticRisk can build a new Compare & Monitor comparison cycle and findings from those current reports for **0 credits**. That path does not launch a new domain scan. Comparison processing can still take time because the governed comparison measurement and findings are being produced from the current evidence.

If the zero-credit comparison build fails, retrying that comparison build does not by itself require a domain scan or another credit. Runtime state remains authoritative for whether any selected domain later needs fresh evidence.

## Primary AI Measurement Plan preflight

Before paid comparison work is started, SemanticRisk resolves one primary-company AI Measurement Plan and applies that governed buyer/category context across the comparison set.

The primary context can be recovered from supported existing product evidence such as an active profile, compatible historical visibility context, governed taxonomy, or sufficiently strong stored public claim evidence.

When no defensible primary context can be resolved, paid comparison work is blocked before credits are used and the primary setup requires review.

A competitor should not be asked to define a separate comparison category merely because it is being measured. Fresh competitor evidence is measured under the fixed primary comparison context while the competitor's own independent domain evidence/profile remains a separate product object.

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

## Customer workspace and report destination

The workspace is the control/progress surface for comparison selection, evidence mode, credit requirement and comparison state. Detailed comparison interpretation belongs in the completed Unified Report rather than being duplicated as a second competing report surface in the workspace.

Customer-visible domain states can distinguish queued/scanning/AI measurement/processing/finalizing/ready/failed conditions. Aggregate Compare & Monitor progress should describe how many selected domains are ready rather than implying that the primary domain's progress represents the whole set.

When the selected domains are current and the completed comparison exactly matches the active selection, **View Compare & Monitor Report** opens the primary domain's Unified Report. Individual competitor reports remain supporting domain evidence and can still be opened separately.

The workspace can expose:

- comparison membership and evidence mode;
- credit requirement before fresh evidence is requested;
- current-domain readiness and aggregate comparison progress;
- comparison build state such as **Building comparison…** when current reports are being assembled;
- the final Compare & Monitor report action when compatible findings are ready.

Simply viewing the workspace or a completed comparison does not itself spend a credit, launch a scan, grant domain access, or force a fresh evidence cycle.

## No composite winner score

SemanticRisk should not manufacture one overall winner/rank score from heterogeneous comparison measurements unless a separately defined, governed methodology explicitly supports one.

Recognition, recommendation, citation, interpretation, governance and drift measurements can move differently. The customer should be able to see those differences rather than having them hidden inside an unexplained aggregate score.

## Runtime-state boundary

Documentation explains the Compare & Monitor contract but does not establish current comparison state.

An AI assistant must use authorized runtime state to determine:

- which primary domain and comparison set are active;
- which domains the customer may access;
- which selected domains already have current paid evidence for this account;
- the current reuse-mode and force-fresh credit cost;
- whether the primary measurement context is ready or needs review;
- which measurement-plan and probe versions are active;
- whether domain evidence is queued, running, ready or failed;
- whether a zero-credit current-evidence comparison is preparing, running, complete or failed;
- whether a completed comparison exactly matches the active selected domains;
- which findings are current;
- whether the displayed evidence is compatible for longitudinal comparison;
- whether any state-changing comparison action is currently available or authorized.

An AI assistant must not describe a zero-credit comparison build as a free new domain scan. It is a comparison computation using already-current paid domain evidence. Conversely, it must not tell the customer to buy fresh domain evidence when runtime state says all selected reports are current and eligible for the zero-credit comparison path.
