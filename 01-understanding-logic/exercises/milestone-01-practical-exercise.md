# Milestone 1: Practical Reasoning Exercise

## Scenario
A patient says they booked an appointment for 10 AM, but the appointment is missing from the application's appointment list.

You are given:
1. The patient has a screenshot showing an appointment for 10 AM.
2. The appointment cannot be found in the application's current appointment list.
3. Another patient appears as booked for the same 10 AM slot.

## Questions explored
1. What does the screenshot show, and what does it not prove by itself?
2. What is known from the current appointment list?
3. What is still unknown?
4. What should be investigated before deciding what happened?

## Additional information revealed
- The original appointment record exists.
- Its status is `cancelled`.
- Another patient is confirmed for the 10 AM slot.

## Reasoning demonstrated
The learner recognised that the screenshot supports the patient's claim that an appointment was displayed, but does not by itself establish successful database persistence.

The learner identified the database record and its status as important evidence. After learning that the original record existed with status `cancelled`, the learner correctly distinguished the known status from the still-unknown reason for cancellation.

The cancellation history or audit log was identified as a useful next place to investigate.

## Important limitation
The available information establishes that the original record exists and is marked `cancelled`. It does not, by itself, establish exactly when, why, or by whom the cancellation occurred.
