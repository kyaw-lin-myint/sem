# Use Case 2: Produce Salary Report for Employees in a Department

## Goal in Context
As an HR advisor I want to produce a report on the salary of employees in a department so that I can support financial reporting of the organisation.

## Scope
Company-wide HR System

## Level
Primary task

## Preconditions
- The user is authenticated as an HR advisor.
- The employee database is available and populated.
- A valid department exists.

## Success Condition
A report is produced listing all current employees in the specified department with their current salary.

## Failed Condition
No report is produced; an error message is shown.

## Primary Actor
HR Advisor

## Trigger
The HR advisor selects the "Salary Report by Department" option and enters a department name.

## Main Success Scenario
1. HR advisor selects "Salary Report by Department".
2. System prompts for the department name.
3. HR advisor enters the department name (e.g. "Development").
4. System queries the database for all current employees in that department.
5. System retrieves each employee's emp_no, first_name, last_name, and current salary.
6. System sorts the results by employee number (ascending).
7. System displays the report to the HR advisor.

## Extensions
- **3a.** Department entered is not found.
    - 3a1. System displays "No employees found in that department."
    - 3a2. Use case ends in failure.
- **4a.** Database connection fails.
    - 4a1. System displays "Database connection error."
    - 4a2. Use case ends in failure.

## Sub-variations
- The report can be filtered by role (future enhancement).

## Schedule
Delivered in Sprint 2 of the module.