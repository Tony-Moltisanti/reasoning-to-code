# Milestone 3 — Practice Exercises

Answer each question before checking the answer key in `../solutions/milestone-03-answer-key.md`.

## Conditional direction and reasoning

1. Translate: “A patient can book only if logged in.”
2. In `P → Q`, which condition is sufficient for Q?
3. If `P → Q` and P is true, what follows?
4. If `P → Q` and Q is false, what follows?
5. Explain why “P → Q; Q is true; therefore P is true” is invalid.
6. Explain why “P → Q; P is false; therefore Q is false” is invalid.
7. Translate: “A patient cannot cancel unless logged in.”
8. What does `P ↔ Q` express?

## Logical operators and PHP

9. A patient must be logged in and verified. Which logical operator connects the conditions?
10. A patient can access if verified or an administrator. Write the PHP expression.
11. Write a PHP condition for “not suspended.”
12. Explain the difference between `$isLoggedIn && ($isVerified || $isAdmin)` and `$isLoggedIn && $isVerified || $isAdmin`.
13. What happens if an `if` condition is false and there is no `else`?
14. In an `if`/`elseif` chain, what happens after the first matching branch runs?
15. Why should an unknown payment status not automatically be treated as failed?

## Comparisons and boundaries

16. A requirement says “at least 18.” Which operator should be used?
17. Why does `$age > 18` fail to implement “at least 18”?
18. Give three useful boundary values for a minimum age of 18.
19. Explain the difference between `===` and `==` in PHP.
20. What does `25 !== "25"` evaluate to, and why?

## Requirements and testing distinctions

21. Explain the difference between `must` and `should`.
22. What does `may` usually express in a requirement?
23. In common specification conventions, how can `shall` differ from `will`?
24. Distinguish expected result from actual result.
25. Give one positive and one negative test for an age-18 booking rule.
26. Explain verification versus validation.
27. Distinguish manual from automated testing.
28. Distinguish unit, integration and system testing.
29. Can a unit test be automated? Can a system test be manual?
30. A patient must be at least 18 and logged in, may book if verified or an administrator, and must not be suspended. Write the PHP condition.

## Applied scenario

A clinic requirement states:

“Patients must be at least 18 years old and logged in. They may book if verified or approved by an administrator. Suspended patients must never be allowed to book.”

31. Identify every mandatory condition.
32. Identify the alternative conditions.
33. Write the complete PHP condition.
34. Explain why an administrator approval must not override the age, login or suspension rules.
35. Evaluate these patients and state whether booking should be permitted:

| Patient | Age | Logged in | Verified | Admin | Suspended |
|---|---:|---|---|---|---|
| 1 | 20 | Yes | Yes | No | No |
| 2 | 17 | Yes | Yes | No | No |
| 3 | 25 | No | No | Yes | No |
| 4 | 30 | Yes | No | Yes | Yes |
