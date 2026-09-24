# Use Case 6: View an Employee's Details

## Goal in Context
As an HR advisor I want to view an employee's details so that the employee's promotion request can be supported.

## Scope
Company-wide HR System

## Level
Primary task

## Preconditions
- The user is authenticated as an HR advisor.
- The employee database is available.
- A valid employee ID is known.

## Success Condition
The employee's full current record (name, title, salary, department, manager) is displayed.

## Failed Condition
No record is displayed; an error message is shown.

## Primary Actor
HR Advisor

## Trigger
The HR advisor selects the "View Employee" option and enters an employee ID.

## Main Success Scenario
1. HR advisor selects "View Employee".
2. System prompts for the employee ID.
3. HR advisor enters the employee ID.
4. System queries the database for the current record of that employee.
5. System retrieves emp_no, first_name, last_name, title, salary, dept_name, and manager.
6. System displays the record to the HR advisor.

## Extensions
- **3a.** Employee ID entered is not found.
    - 3a1. System displays "No employee found with that ID."
    - 3a2. Use case ends in failure.
- **4a.** Database connection fails.
    - 4a1. System displays "Database connection error."
    - 4a2. Use case ends in failure.

## Sub-variations
- Employee's historical records can also be viewed (future enhancement).

## Schedule
Delivered in Sprint 1 of the module.