# Governed Actions

SemanticRisk distinguishes between explaining a capability and executing a capability.

An AI assistant may be able to describe an action without being authorized to perform that action.

## Action states

A useful public model is:

- **Read / explain** — inspect or explain existing information without changing product state.
- **Prepare** — construct a proposed action and explain its effect before execution.
- **Approve** — obtain explicit user approval when the action requires it.
- **Execute** — perform the action through the governed product interface.
- **Observe** — track the resulting work or state change.

The assistant should not collapse these states into one step when the product requires separation.

## Controlled actions

Some SemanticRisk actions are controlled because they change recurring behaviour, create new work, consume account resources, or affect product state.

A controlled action can require one or more of:

- authenticated account context;
- domain verification;
- domain or team authority;
- sufficient plan entitlement;
- an explicit approval step;
- confirmation that the proposed action is still current;
- a supported target state or parameter.

The runtime product is authoritative for these checks.

## Amber actions

SemanticRisk uses **Amber** for actions that are permitted only after a clear proposal and explicit approval.

An Amber action should tell the user:

1. what will change;
2. which domain or object is affected;
3. what will not change;
4. whether approval is required;
5. why the action is unavailable if eligibility checks fail.

The assistant must not represent an Amber action as completed before the governed execution path confirms success.

## Example: monitoring cadence

Changing recurring monitoring cadence is a governed action.

Supported product states may include recurring monitoring being enabled at a supported cadence or disabled.

Before a monitoring cadence change can execute, the product can require:

- a verified domain;
- sufficient domain/team authority;
- an eligible monitoring plan;
- explicit approval;
- confirmation that the monitoring state has not changed since the proposal was prepared.

If the state has changed, the assistant should prepare the action again rather than applying an outdated proposal.

## Example: accessibility evidence refresh

Refreshing direct accessibility evidence is also presented as a controlled action.

The proposed action should be explained before work is queued. Its purpose is to refresh reachability and response evidence for the selected domain.

It should not be described as modifying the target website, changing billing, changing monitoring cadence, or automatically starting a separate visibility investigation unless the product explicitly does so.

## AI behaviour rule

The assistant should prefer:

**inspect → explain → prepare → obtain required approval → execute → report result**

over pretending that a natural-language request itself bypasses product controls.

Natural language is an interface to governed product actions, not a replacement for authorization, entitlement, or safety checks.
