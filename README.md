# SemanticRisk

**AI visibility and interpretation intelligence for public websites.**

SemanticRisk examines whether AI systems can access and surface an organisation, what they understand from its public website, which claims and classifications they form, and whether that interpretation changes over time.

> **AI visibility tells you whether you appear. SemanticRisk tells you what was understood.**

[Website](https://semanticrisk.io) · [Public benchmark](https://semanticrisk.io/benchmark) · [Methodology](https://semanticrisk.io/methodology/) · [Sample Unified Report](https://semanticrisk.io/example-report) · [How it works](https://semanticrisk.io/how-it-works/)

---

## What this repository is

This repository is the **public documentation and reference layer for SemanticRisk**. It is not the production application source code, customer-data store, private scoring implementation, or infrastructure repository.

It exists so people, AI systems, agencies, researchers, and developers can reference the same product definitions, measurement boundaries, object model, methodology, and assistant rules used by SemanticRisk.

Where documentation and authenticated runtime state differ, **current runtime state is authoritative** for account balances, credits, report availability, evidence freshness, entitlements, promotional offers, and work in progress.

---

## The problem

An AI system can access a company website without surfacing the company in a buyer answer. It can surface a company while misunderstanding it. It can also change that interpretation even when the underlying website appears stable.

SemanticRisk therefore separates several questions that are often collapsed into a single visibility score:

- Can AI-oriented crawlers reach and discover the public evidence?
- Does the company appear in controlled buyer-prompt observations?
- How does AI classify and describe the organisation?
- Do models disagree, omit, narrow, or overstate claims?
- Has the measured interpretation changed over time?
- What evidence-backed action, if any, deserves attention next?

---

## Public measurement sequence

SemanticRisk uses one public six-stage sequence across the product and documentation:

1. **Access & readiness** — can the relevant public website evidence be reached and discovered?
2. **AI visibility** — does the organisation appear in controlled buyer-prompt observations?
3. **Interpretation** — what claims, categories, and descriptions are formed from the available evidence?
4. **Drift & change** — what changed between comparable evidence cycles?
5. **Assessment & action** — what is material, unusual, or worth addressing?
6. **Unified Report & monitoring** — preserve the evidence, findings, priorities, and printable/PDF view for the evidence cycle.

Internal documentation may describe lower-level operations such as capture, extraction, normalization, comparison, and review. Those are implementation activities that map into the six public stages above rather than separate customer-facing product models.

---

## AI visibility vs interpretation

| AI visibility | SemanticRisk interpretation intelligence |
|---|---|
| Measures whether a company appears in generated answers | Evaluates what AI systems understood about the company |
| Tracks prompt-level presence, recommendations, citations, and sources | Records claims, classifications, disagreement, omission, narrowing, and change |
| Answers “Did we appear?” | Answers “What did the system understand, and did that change?” |
| Can be influenced by access, relevance, competition, and source selection | Is traced back to public wording, structure, capture conditions, and model output |

SemanticRisk combines these views rather than treating them as competing product categories.

---

## Current applied product

The current commercial product is one operational workspace with one customer-facing **Unified Report** per evidence cycle.

- Any public domain can be checked without proving ownership.
- One SemanticRisk credit costs **US$5.95**.
- Standard credit packs are **1, 10, 20, and 100 credits**.
- A credit grants the current reusable Unified Report when that report is no more than 30 days old.
- If no fresh reusable report exists, one credit funds or joins the next shared public-domain evidence cycle.
- An explicit early refresh consumes another credit.
- Reusable public-domain evidence may be shared across entitled customers only when it is explicitly safe for reuse.
- Customer-private inputs are not exposed across customers.

Commercial and authenticated runtime details are authoritative at [semanticrisk.io](https://semanticrisk.io).

---

## What the Unified Report can contain

Depending on the available evidence for the domain and cycle, the Unified Report can include:

- access and crawl-readiness findings;
- robots.txt, sitemap, and discoverability observations;
- controlled buyer-prompt AI visibility evidence;
- citation and source-provenance evidence;
- AI interpretation and extracted-claim analysis;
- model disagreement or inconsistency evidence where measured;
- drift and change findings from comparable cycles;
- ranked evidence-backed next actions;
- a printable/PDF rendering of the same report.

The report is a diagnostic artifact, not a guarantee of future model behaviour, recommendation placement, search ranking, or downstream AI output.

---

## Public evidence

The public SemanticRisk site includes:

- a company and sector benchmark;
- the semanticrisk.io live specimen;
- public methodology and documentation;
- selected evidence and findings;
- a sample Unified Report;
- AI-readable discovery material such as `llms.txt` and `claims.json`.

The production platform and private implementation are maintained separately from this public reference repository.

---

## Framework boundaries

SemanticRisk does **not**:

- determine objective truth;
- certify safety, compliance, or correctness;
- replace human judgement;
- guarantee control over downstream AI output;
- function as a standalone decision-maker;
- infer a trend when comparable evidence does not exist.

Its purpose is evidence-led measurement and interpretation intelligence.

---

## Intended uses

SemanticRisk is relevant to:

- communications and reputation teams;
- SEO, GEO, AEO, and web-strategy agencies;
- marketing and brand teams;
- governance, assurance, and risk functions;
- evaluation of AI assistants and public-facing AI output;
- post-incident analysis;
- research, education, and policy discussion.

It is especially useful where AI-generated descriptions may influence customers, procurement teams, investors, regulators, partners, or the public.

---

## How to reference SemanticRisk

Suggested citation:

> **SemanticRisk — AI visibility and interpretation intelligence for public websites**  
> https://semanticrisk.io

This public reference evolves alongside the product. Material changes should be dated in the repository changelog.

---

## Repository status and licence

This repository contains public reference material only. It is not the distribution point for production code, customer data, private scoring logic, or infrastructure.

Unless a file states otherwise, the documentation and reference material in this repository are made available under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** licence. See `LICENSE` for the repository notice.
