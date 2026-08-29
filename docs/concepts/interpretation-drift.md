# Interpretation Drift

Interpretation drift is a material change in AI interpretation between observations.

SemanticRisk uses repeated observations to distinguish different reasons why outputs may change.

## Possible change sources

A change between observations can be associated with one or more of the following:

- source content changed;
- captured content changed;
- crawl or capture conditions changed;
- extracted claims changed;
- model stance or classification changed;
- confidence changed;
- model behaviour changed while source evidence appeared stable;
- a pipeline error or access problem affected the observation.

## Public drift classes

SemanticRisk has used deterministic drift classes including:

- NO_CHANGE
- CONTENT_CHANGED
- EXTRACTION_DRIFT
- STANCE_DRIFT
- CONFIDENCE_DRIFT
- MIXED
- PIPELINE_AUTH
- PIPELINE_ERROR

These labels describe observed system states and comparisons. They should not be presented as automatic proof of cause.

## Interpretation rule

When discussing drift, distinguish clearly between:

1. what changed in the captured evidence;
2. what changed in model output;
3. what SemanticRisk can directly observe;
4. what is only a possible explanation.

## Example

If captured website content appears unchanged but an extracted claim changes, SemanticRisk may identify interpretation or extraction drift.

That observation does not by itself prove why the model changed its output.

## Monitoring purpose

Monitoring exists to make these changes visible over time so that a user can review material differences rather than relying on one isolated AI response.
