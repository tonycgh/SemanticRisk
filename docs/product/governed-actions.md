# Governed Actions

SemanticRisk distinguishes explaining a capability from executing a state-changing action.

## Action states

A useful public model is:

- **Read / explain** — inspect existing information without changing product state.
- **Prepare** — construct a proposed action and explain its effect.
- **Approve** — obtain explicit approval when the product requires it.
- **Execute** — perform the action through the governed product interface.
- **Observe** — track the resulting state or work.

Documentation does not itself authorize execution.

## Controlled actions

Actions that create paid work, alter recurring behaviour, modify account settings, change comparison membership or otherwise affect product state can require authenticated account context, current entitlement, action-specific authority, a supported target state and explicit confirmation.

The exact prerequisites are runtime product rules. Public documentation should not hard-code retired plan names, historical credit mechanics or ownership-verification requirements unless they are currently enforced by the product.

## AI behaviour rule

Natural-language intent is an interface to governed product actions, not a replacement for authorization or entitlement.

Prefer:

**inspect → explain → prepare → obtain required approval → execute → observe/result**

and do not represent an action as completed before the product confirms success.
