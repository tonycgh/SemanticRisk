# Deep Visibility Investigations

A deep visibility investigation is a governed SemanticRisk action that creates a bounded set of additional AI observations for a domain using previously established investigation context.

It is intended to gather more evidence when a customer needs a deeper view than the currently stored visibility evidence provides.

## Capability and entitlement

Deep investigation is a Professional capability.

An AI assistant must not infer eligibility from documentation alone. Current account and domain entitlement state must be checked at runtime before the action is offered or executed.

## Governed action model

Deep investigation is an Amber action.

The expected flow is:

**inspect current state → prepare exact investigation scope → show proposal → obtain explicit approval → execute governed queue work → observe progress → explain completed evidence**

Preparing an investigation does not itself create observation work.

## Proposal scope

Before approval, SemanticRisk should expose the bounded scope of the proposed investigation, including the applicable prompt set, configured models, repetitions, and resulting observation count.

The approved scope is treated as fixed. If the underlying scope changes before execution, the action must be prepared again rather than applying stale approval to different work.

## Reuse of governed context

A new deep investigation should reuse the latest supported completed visibility setup for the domain rather than inventing new category, buyer-need, risk-need, geography, alias, or other investigation context from free-form assistant inference.

If there is not enough governed prior setup to reproduce the investigation safely, the action should not execute.

## Active investigation rule

SemanticRisk should not create a second customer-agent deep investigation for a domain while an approved investigation is already active.

When an active investigation exists, the assistant should inspect and report that run instead of proposing an overlapping duplicate run.

## Partial authorization and recovery

An investigation can exist while some observations are already complete, some are authorized in the queue, and some of the approved observation scope still needs authorization.

SemanticRisk may offer a governed recovery/resume action for the missing portion of the already approved scope.

Recovery must remain bound to the exact active investigation. If the active investigation changes, the assistant should prepare the recovery again before asking for approval.

The recovery action must not silently expand the investigation beyond its approved observation scope.

## Progress and queue state

While an investigation is active, SemanticRisk can expose live progress such as:

- total observations in scope;
- observations authorized or already complete;
- observations still needing authorization;
- queued work;
- currently running work;
- completed queue jobs;
- failed queue jobs;
- whether the queue appears stalled.

These are runtime states, not documentation facts. The assistant must read current state before describing investigation progress.

## Queue-health interpretation

A stalled queue indicator means authorized observation work appears not to be progressing normally. It does not by itself mean the investigation evidence is invalid or that the target domain changed.

Failed observation jobs mean some requested observations did not complete successfully. The assistant should distinguish observation failure from a negative finding about the monitored domain.

## Completion

When the approved observation scope reaches terminal state, SemanticRisk should treat the investigation as evidence collection completed and then explain or review the newly stored evidence.

Completion of queue work does not mean every model necessarily returned a usable answer; terminal outcomes can include supported non-answer states such as blocked or unsupported observations.

## AI behaviour rules

The assistant must not:

- represent a prepared investigation as already running;
- represent an approved investigation as complete before runtime state confirms completion;
- create a duplicate overlapping investigation when an active governed run already exists;
- reuse stale approval after scope or active-run state changes;
- treat queue failure as proof of a semantic or reputational problem with the domain;
- invent current prompt counts, model counts, repetitions, queue counts, or completion percentages from documentation.

For customer-specific questions, current runtime state is authoritative.