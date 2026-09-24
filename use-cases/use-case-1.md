# Use Case 1: Produce Salary Report for All Employees

## Goal in Context
As an HR advisor I want to produce a report on the salary of all employees so that I can support financial reporting of the organisation.

## Scope
Company-wide HR System

## Level
Primary task

## Preconditions
- The user is authenticated as an HR advisor.
- The employee database is available and populated.

## Success Condition
A report is produced listing all current employees and their current salary.

## Failed Condition
No report is produced; an error message is shown.

## Primary Actor
HR Advisor

## Trigger
The HR advisor selects the "Salary Report for All Employees" option.

## Main Success Scenario
1. HR advisor selects "Salary Report for All Employees".
2. System queries the database for all current employees.
3. System retrieves each employee's emp_no, first_name, last_name, and current salary.
4. System sorts the results by employee number (ascending).
5. System displays the report to the HR advisor.

## Extensions
- **2a.** Database connection fails.
    - 2a1. System displays "Database connection error."
    - 2a2. Use case ends in failure.
- **3a.** No employees exist in the database.
    - 3a1. System displays "No employees found."
    - 3a2. Use case ends in failure.

## Sub-variations
- The report can be exported to CSV (future enhancement).

## Schedule
Delivered in Sprint 1 of the module.