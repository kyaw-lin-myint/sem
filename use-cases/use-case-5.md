# Use Case 5: Add a New Employee

## Goal in Context
As an HR advisor I want to add a new employee's details so that I can ensure the new employee is paid.

## Scope
Company-wide HR System

## Level
Primary task

## Preconditions
- The user is authenticated as an HR advisor.
- The employee database is available.

## Success Condition
A new employee record is created in the database with the given details.

## Failed Condition
The employee record is not created; an error message is shown.

## Primary Actor
HR Advisor

## Trigger
The HR advisor selects the "Add New Employee" option.

## Main Success Scenario
1. HR advisor selects "Add New Employee".
2. System prompts for employee details (first name, last name, title, department, salary).
3. HR advisor enters the details.
4. System validates the details.
5. System generates a new emp_no and inserts the record into the database.
6. System confirms the employee was added successfully.

## Extensions
- **4a.** Required field is missing or invalid.
    - 4a1. System highlights the missing field.
    - 4a2. Use case returns to step 3.
- **5a.** Database insertion fails.
    - 5a1. System displays "Could not add employee."
    - 5a2. Use case ends in failure.

## Sub-variations
- Employee may be added without assigning to a department initially.

## Schedule
Delivered in Sprint 4 of the module.