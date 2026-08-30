# Methodology Overview

SemanticRisk uses an evidence-to-interpretation workflow designed to preserve the distinction between source material, AI output, comparison, and review.

## 1. Capture

Identify public website evidence that is accessible and usable for analysis.

Capture conditions matter. A later difference may result from source content change, crawl behaviour, accessibility conditions, or another capture-related factor.

## 2. Extract

Use AI systems to form structured claims, classifications, and related observations from the captured evidence.

An extracted claim is a model output. It is not automatically treated as objective truth.

## 3. Compare

Compare observations across models and/or across time.

Comparison can identify:

- agreement;
- disagreement;
- omission;
- narrowing;
- overstatement;
- classification difference;
- extraction change;
- stance change;
- confidence change.

## 4. Monitor

Repeat observations to identify material changes in capture conditions, claims, classifications, and interpretation.

Monitoring turns a single observation into a time series that can be reviewed for drift.

## 5. Review

Assess the evidence and comparison results to determine whether a change appears material and what may explain it.

Review should distinguish direct observation from inference.

## Methodological boundaries

SemanticRisk does not claim that model agreement proves truth or that model disagreement proves error.

SemanticRisk does not infer causation solely from correlation between website change and model-output change.

SemanticRisk does not guarantee that downstream AI systems will reproduce the observations recorded by the platform.

The purpose of the methodology is to make interpretation observable, comparable, and reviewable.
