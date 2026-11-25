# Lesson 5 — PHP Conditional Statements

## `if`

An `if` block runs only when its condition is true.

```php
if ($isLoggedIn === true) {
    echo "Access granted";
}
```

If the condition is false, PHP skips the block. Without an `else`, no automatic denial message is displayed.

## `if` and `else`

```php
if ($isLoggedIn === true) {
    echo "Access granted";
} else {
    echo "Access denied";
}
```

Exactly one of these two branches runs.

## `elseif`

PHP checks conditions in order and runs the first matching branch. Remaining branches are skipped.

```php
if ($paymentStatus === "successful") {
    echo "Booking confirmed";
} elseif ($paymentStatus === "pending") {
    echo "Payment is being processed";
} elseif ($paymentStatus === "refunded") {
    echo "Payment has been refunded";
} else {
    echo "Unknown payment status";
}
```

The final `else` handles values not matched above. Do not label an unknown status as failed unless the requirement says to.

## Nested conditions

An `if` inside another `if` is nested. The inner condition is checked only if execution reaches it.

```php
if ($age >= 18) {
    if ($isLoggedIn === true) {
        echo "Registration allowed";
    }
}
```

Equivalent combined condition:

```php
if ($age >= 18 && $isLoggedIn === true) {
    echo "Registration allowed";
}
```

Both require age and login to be true for the message to display.
