# Milestone 3 — Answer Key and Explanations

## 30-question assessment

1. **B** — `CanBook → IsLoggedIn`; login is necessary.
2. **B** — Payment success plus the conditional gives confirmation (modus ponens).
3. **A** — If Q is false under `P → Q`, P must be false (modus tollens).
4. **B** — Both conditions are required (AND).
5. **B** — `!` means NOT.
6. **A** — A false operand makes an AND expression false; PHP can short-circuit.
7. **B** — Only the first matching branch runs.
8. **B** — `>=` includes 18.
9. **B** — 17, 18 and 19 test below, at and above the boundary.
10. **B** — Expected is what should happen according to the requirement.
11. **A** — A logged-out denial check is negative testing.
12. **B** — Validation asks whether the right system is being built for users.
13. **A** — A person executes the test.
14. **B** — Unit testing checks an individual component.
15. **A** — Integration testing checks connected components.
16. **B** — System testing checks the whole application or workflow.
17. **B** — `Must` is generally an obligation; `should` generally a recommendation.
18. **A** — A common convention is `shall` for formal requirement and `will` for expected future behaviour; documents should define terms.
19. **B** — `May` commonly expresses permission or possibility, not a completed action.
20. **A** — Login is mandatory, booking is permitted under the condition, and confirmation is recommended/expected.
21. **A** — Age and login are mandatory; verification or admin approval are alternatives.
22. **A** — AND incorrectly requires both alternatives.
23. **B** — Administrator status satisfies the alternative, assuming other mandatory conditions are met.
24. **A** — All three refund conditions are necessary.
25. **B** — Affirming the consequent is invalid.
26. **A** — Denying the antecedent is invalid.
27. **A** — The expression preserves mandatory conditions and groups alternatives.
28. **B** — Verification cannot override the minimum age.
29. **B** — The administrator OR branch makes the faulty expression true despite failed mandatory conditions.
30. **A** — Only Patient 1 satisfies all requirements.

## Applied scenario answers

31. Mandatory conditions: age is at least 18; patient is logged in; patient is not suspended.
32. Alternatives: patient is verified OR approved by an administrator.
33. Correct condition:

```php
if (
    $age >= 18 &&
    $isLoggedIn &&
    ($isVerified || $isAdmin) &&
    !$isSuspended
) {
    echo "Booking permitted";
} else {
    echo "Booking denied";
}
```

34. The administrator condition is an alternative route only for the verification/approval part. It must not bypass the separate mandatory requirements.
35. Patient 1: permitted. Patient 2: denied (underage). Patient 3: denied (not logged in). Patient 4: denied (suspended).

## Important corrections and reasoning reminders

- “Only if” points to a necessary condition: `Q only if P` means `Q → P`.
- A conditional does not establish its converse.
- A false antecedent does not establish a false consequent.
- A true consequent does not establish a true antecedent.
- Parentheses prevent an OR alternative from bypassing mandatory conditions.
- “At least” includes equality; use `>=`.
- An unknown status should be handled explicitly rather than assumed to mean failure.
- Permission (`may`) is not a guarantee that an action occurred.
- One passing test does not establish that the whole system is correct.
