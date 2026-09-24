# Use Case 3: Department Manager Salary Report

## Goal in Context
As a department manager I want to produce a report on the salary of employees in my department so that I can support financial reporting for my department.

## Scope
Company-wide HR System, scoped to a single department

## Level
Primary task

## Preconditions
- The user is authenticated as a department manager.
- The manager is assigned to a specific department.
- The employee database is available and populated.

## Success Condition
A report is produced listing all current employees in the manager's department with their current salary.

## Failed Condition
No report is produced; an error message is shown.

## Primary Actor
Department Manager

## Trigger
The manager selects the "Department Salary Report" option.

## Main Success Scenario
1. Department manager selects "Department Salary Report".
2. System identifies the manager's department from their profile.
3. System queries the database for all current employees in that department.
4. System retrieves each employee's emp_no, first_name, last_name, and current salary.
5. System sorts the results by employee number (ascending).
6. System displays the report to the manager.

## Extensions
- **2a.** Manager is not assigned to a department.
    - 2a1. System displays "No department assigned."
    - 2a2. Use case ends in failure.
- **3a.** Database connection fails.
    - 3a1. System displays "Database connection error."
    - 3a2. Use case ends in failure.

## Sub-variations
- The manager may choose to view only their team (excludes sub-departments) — future enhancement.

## Schedule
Delivered in Sprint 3 of the module.