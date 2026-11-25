# Lesson 2 — Necessary and Sufficient Conditions

## Sufficient

A condition is sufficient when it guarantees the outcome.

In `P → Q`, P is sufficient for Q.

Example: If a user is an administrator, the user can access the administration area. Administrator status is sufficient under this rule. The statement does not prove that it is the only route to access.

## Necessary

A condition is necessary when the outcome cannot happen without it.

Example: “A patient can book only if logged in.”

`CanBook → IsLoggedIn`

Login is necessary for booking.

## If and only if

`P ↔ Q` expresses both directions. P is necessary and sufficient for Q, and Q is necessary and sufficient for P. Use it only when both directions are genuinely established.

## Unless

“Q unless P” is commonly read as “if not P, then Q”:

`NOT P → Q`

Example: “The appointment remains active unless it is cancelled.”

`NOT Cancelled → RemainsActive`

For “A patient cannot cancel unless logged in,” login is necessary:

`CanCancel → IsLoggedIn`

Equivalently, if the patient is not logged in, cancellation is not possible:

`NOT IsLoggedIn → NOT CanCancel`

Being logged in removes this particular restriction; it does not guarantee cancellation if other rules apply.

## Provided that / as long as

These phrases introduce a condition, but identify the outcome before choosing the arrow.

“A patient can access records provided that they are verified”:

`Verified → CanAccessRecords`

## Common mistake

Do not memorise a phrase mechanically. Identify what must be true and what follows from it.
