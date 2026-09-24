# Use Case 8: Delete an Employee's Details

## Goal in Context
As an HR advisor I want to delete an employee's details so that the company is compliant with data retention legislation.

## Scope
Company-wide HR System

## Level
Primary task

## Preconditions
- The user is authenticated as an HR advisor.
- The employee database is available.
- A valid employee ID is known.
- The employee is no longer actively employed by the organisation.

## Success Condition
The employee record is removed (or marked as deleted) in the database.

## Failed Condition
The employee record is not deleted; an error message is shown.

## Primary Actor
HR Advisor

## Trigger
The HR advisor selects the "Delete Employee" option and enters an employee ID.

## Main Success Scenario
1. HR advisor selects "Delete Employee".
2. System prompts for the employee ID.
3. HR advisor enters the employee ID.
4. System retrieves and displays the employee record for confirmation.
5. HR advisor confirms the deletion.
6. System deletes (or marks as deleted) the record in the database.
7. System confirms the deletion was successful.

## Extensions
- **3a.** Employee ID entered is not found.
    - 3a1. System displays "No employee found with that ID."
    - 3a2. Use case ends in failure.
- **5a.** HR advisor cancels the deletion.
    - 5a1. Use case ends without deleting the record.
- **6a.** Database deletion fails.
    - 6a1. System displays "Could not delete employee."
    - 6a2. Use case ends in failure.

## Sub-variations
- Deletion may be "soft" (mark as inactive) rather than hard delete, per company policy.

## Schedule
Delivered in Sprint 5 of the module.