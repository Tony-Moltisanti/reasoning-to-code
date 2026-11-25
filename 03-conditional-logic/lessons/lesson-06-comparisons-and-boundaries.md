# Lesson 6 — Comparison Operators and Boundary Conditions

## Comparison operators

| Operator | Meaning | Example |
|---|---|---|
| `===` | Identical value and type | `25 === 25` is true |
| `!==` | Not identical in value or type | `25 !== "25"` is true |
| `==` | Equal after applicable type conversion | `18 == "18"` is true |
| `!=` | Not equal after applicable type conversion | `18 != 20` is true |
| `>` | Greater than | `19 > 18` is true |
| `<` | Less than | `17 < 18` is true |
| `>=` | Greater than or equal to | `18 >= 18` is true |
| `<=` | Less than or equal to | `18 <= 18` is true |

## Strict and loose comparison

`===` checks value and type:

```php
18 === 18     // true
18 === "18"   // false
```

`==` permits PHP type conversion where applicable:

```php
18 == "18"    // true
```

Strict comparison is usually clearer when the exact type matters.

## Boundary values

Requirement: a patient must be at least 18.

Correct:

```php
$age >= 18
```

Faulty:

```php
$age > 18
```

The faulty expression rejects someone who is exactly 18. It is a logical error, not necessarily a syntax error.

Check values just below, at, and just above the boundary:

- 17 — below.
- 18 — exactly at.
- 19 — above.

Another example: a fee must be at least ₦3,000. `$amount >= 3000` accepts ₦3,000. `$amount > 3000` incorrectly rejects the exact threshold.

Boundary-value thinking exposes errors that testing only typical values may miss.
