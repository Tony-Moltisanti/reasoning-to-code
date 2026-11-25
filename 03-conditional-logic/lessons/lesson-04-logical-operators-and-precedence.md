# Lesson 4 — AND, OR, NOT, Grouping and Precedence

## AND

Both conditions must be true.

| P | Q | P AND Q |
|---|---|---|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | F |

PHP: `&&`

Example: `$isLoggedIn && $isVerified`

## OR

At least one condition must be true. PHP `||` is inclusive OR: it is also true when both conditions are true.

| P | Q | P OR Q |
|---|---|---|
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | F |

PHP: `||`

Example: `$isVerified || $isAdmin`

## NOT

NOT reverses a truth value. PHP uses `!`.

- `!true` is false.
- `!false` is true.

Example: `!$isSuspended` means the patient is not suspended. Negation changes the truth value; it does not itself perform an opposite action.

## Parentheses

Requirement: a patient must be logged in and must be verified or an administrator.

Correct grouping:

```php
$isLoggedIn && ($isVerified || $isAdmin)
```

Login is mandatory. Verification and administrator status are alternatives.

Without parentheses:

```php
$isLoggedIn && $isVerified || $isAdmin
```

PHP evaluates `&&` before `||`, so this means:

```php
($isLoggedIn && $isVerified) || $isAdmin
```

An administrator could pass without being logged in. This violates the requirement.

## Short-circuit evaluation

- With `&&`, a false left operand makes the whole expression false; PHP need not evaluate the right operand.
- With `||`, a true left operand makes the whole expression true; PHP need not evaluate the right operand.

This can avoid unnecessary work and matters when an operand calls a function or has another effect.

## A reliable translation habit

Separate mandatory conditions from alternatives. Join mandatory conditions with AND, group alternatives with OR, and use NOT for disqualifying conditions that must be false.
