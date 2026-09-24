# Use Case 7: Update an Employee's Details

## Goal in Context
As an HR advisor I want to update an employee's details so that employee's details are kept up-to-date.

## Scope
Company-wide HR System

## Level
Primary task

## Preconditions
- The user is authenticated as an HR advisor.
- The employee database is available.
- A valid employee ID is known.

## Success Condition
The employee's record is updated in the database with the new details.

## Failed Condition
The employee record is not updated; an error message is shown.

## Primary Actor
HR Advisor

## Trigger
The HR advisor selects the "Update Employee" option and enters an employee ID.

## Main Success Scenario
1. HR advisor selects "Update Employee".
2. System prompts for the employee ID.
3. HR advisor enters the employee ID.
4. System retrieves and displays the current employee record.
5. HR advisor edits one or more fields (name, title, salary, department).
6. HR advisor confirms the changes.
7. System validates the changes.
8. System updates the record in the database.
9. System confirms the update was successful.

## Extensions
- **3a.** Employee ID entered is not found.
    - 3a1. System displays "No employee found with that ID."
    - 3a2. Use case ends in failure.
- **7a.** New value is invalid (e.g. negative salary).
    - 7a1. System highlights the invalid field.
    - 7a2. Use case returns to step 5.
- **8a.** Database update fails.
    - 8a1. System displays "Could not update employee."
    - 8a2. Use case ends in failure.

## Sub-variations
- Salary change may trigger a payroll recalculation (future enhancement).

## Schedule
Delivered in Sprint 4 of the module.