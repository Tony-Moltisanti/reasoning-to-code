# Lesson 8 — Testing Concepts Connected to Conditional Logic

This lesson introduces testing vocabulary to help reason about requirements and behaviour. Dedicated hands-on testing remains in Milestone 7.

## Requirement versus implementation

- A requirement states what the system is supposed to do.
- An implementation is the code or system behaviour created to meet it.

Code can run without syntax errors and still implement the wrong rule.

## Expected versus actual result

- Expected result: what should happen according to the requirement.
- Actual result: what happened when the system ran.

A test passes when actual matches expected for that test. One passing test does not prove the whole application is correct.

## Test case and coverage

A test case describes a particular situation, relevant input or conditions, and expected result.

Test coverage describes how much relevant functionality, conditions or requirements have been examined.

## Positive and negative testing

- Positive testing checks valid inputs and allowed behaviour.
- Negative testing checks invalid, prohibited or disallowed situations and confirms correct rejection or handling.

Examples: an eligible patient books (positive); an underage or suspended patient is denied (negative).

## Boundary-value versus ordinary testing

Ordinary testing may use age 25. Boundary testing for a minimum age of 18 uses 17, 18 and 19.

## Verification versus validation

- Verification: “Are we building the system correctly according to the specification?”
- Validation: “Are we building the right system for users' actual needs?”

A correct implementation of a poor requirement can pass verification but fail validation.

## Manual versus automated testing

- Manual: a person performs the steps and checks results.
- Automated: software executes predefined checks.

This describes how a test is executed, not its level.

## Unit, integration and system testing

- Unit: checks one small component, such as an age eligibility function.
- Integration: checks connected components, such as a registration form communicating with a database.
- System: checks the whole application or an end-to-end patient journey.

A unit, integration or system test can be manual or automated. Testing level and execution method are different distinctions.
