# Use Case 4: Produce Salary Report by Role

## Goal in Context
As an HR advisor I want to produce a report on the salary of employees of a given role so that I can support financial reporting of the organisation.

## Scope
Company-wide HR System

## Level
Primary task

## Preconditions
- The user is authenticated as an HR advisor.
- The employee database is available and populated.
- A valid role/title exists in the database (e.g. "Engineer").

## Success Condition
A report is produced listing all current employees with the specified role and their current salary, sorted by employee number.

## Failed Condition
No report is produced; an error message is shown indicating the role was not found or the report could not be generated.

## Primary Actor
HR Advisor

## Trigger
The HR advisor selects the "Salary Report by Role" option and enters a role name.

## Main Success Scenario
1. HR advisor selects "Salary Report by Role".
2. System prompts for the role/title.
3. HR advisor enters the role (e.g. "Engineer").
4. System queries the database for all current employees with that title.
5. System retrieves each employee's emp_no, first_name, last_name, and current salary.
6. System sorts the results by employee number (ascending).
7. System displays the report to the HR advisor.

## Extensions
- **3a.** Role entered is not found in the database.
    - 3a1. System displays "No employees found with that role."
    - 3a2. Use case ends in failure.
- **4a.** Database connection fails.
    - 4a1. System displays "Database connection error."
    - 4a2. Use case ends in failure.

## Sub-variations
- The report can be filtered by department (not implemented in current version).
- The report can be exported to CSV (future enhancement).

## Schedule
Delivered in Sprint 2 of the module.