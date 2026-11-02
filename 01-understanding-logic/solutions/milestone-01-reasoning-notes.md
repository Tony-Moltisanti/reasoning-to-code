# Milestone 1: Reasoning Notes

These notes record the reasoning principles used in the practical exercise. They are explanations, not a claim that every possible investigation step was independently completed.

## Screenshot evidence
A screenshot showing an appointment at 10 AM supports the claim that the appointment information appeared on the patient's screen. It does not necessarily prove that the application successfully saved the appointment in the database.

## Missing appointment
Not seeing an appointment in the current list is an observation about what the list displays. It does not, on its own, explain why the appointment is missing.

## Checking the record
Finding the original record and checking its status provides more specific information than relying only on the screenshot or list. The record was found with status `cancelled`.

## What remains unknown
The status tells us that the record is currently marked as cancelled. It does not tell us the reason, actor, or exact sequence of events. A cancellation history or audit log may help establish those details.

## General reasoning habit
Separate:
1. What was reported.
2. What was observed.
3. What evidence supports.
4. What is inferred.
5. What remains unknown.
6. What should be checked next.
