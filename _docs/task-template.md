Task Title

Write a short, specific title describing the task.

Label

Choose the appropriate label:
	•	mvp
	•	post-mvp
	•	user-test-bug

Goal

Describe the result this task should achieve.

The goal must be clear and focused on one main outcome.

Description

Background

Explain why this task is needed and which project requirement it supports.

Scope

Describe what must be implemented.
	•	Requirement 1
	•	Requirement 2
	•	Requirement 3

Out of Scope

List features or changes that are not included in this task.
	•	Feature or change intentionally excluded from this task.

Acceptance Criteria

The task is complete when:
	•	All required behavior matches the approved specification.
	•	Input validation and error handling work where applicable.
	•	Authorization and privacy requirements are satisfied where applicable.
	•	Relevant tests have been executed successfully.
	•	Related functionality has been checked for regressions.
	•	Necessary documentation has been updated.

Add task-specific acceptance criteria below:
	•	Specific criterion 1
	•	Specific criterion 2
	•	Specific criterion 3

Test Cases

Test Case 1: Successful Scenario

Preconditions:
Describe the required starting conditions.

Steps:
	1.	Perform the first action.
	2.	Perform the next action.
	3.	Observe the result.

Expected Result:
Describe the correct behavior.

Test Case 2: Invalid Input or Failure Scenario

Preconditions:
Describe the required starting conditions.

Steps:
	1.	Provide invalid input or perform an invalid action.
	2.	Submit the request or continue the workflow.
	3.	Observe the result.

Expected Result:
The application handles the problem correctly without exposing private information or corrupting data.

Additional Test Cases

Add further tests for permissions, boundary values, errors, and related functionality when relevant.

Dependencies

List tasks or decisions that must be completed first.
	•	Dependency 1
	•	Dependency 2

If there are no dependencies, write None.

Technical Notes

Document relevant technical constraints, affected components, and implementation decisions.

Follow the development sequence in _docs/process.md.

Do not implement features outside the approved scope without updating the requirements and relevant issue.

Definition of Done
	•	The implementation satisfies the acceptance criteria.
	•	Relevant tests have been run.
	•	Test results are recorded honestly.
	•	Known failures or limitations are documented.
	•	Required documentation has been updated.
	•	QA verification is complete.
	•	The issue is ready to be closed.

QA Results

Status: Not tested / Pass / Fail / Blocked

Tests executed:
List the tests actually performed.

Results:
Describe what passed and what failed.

Known limitations:
Document any remaining limitations.

Bug Report Fields

Complete this section when the issue has the user-test-bug label.

Steps to Reproduce:
	1.	First step.
	2.	Second step.
	3.	Third step.

Expected Result:
Describe what should happen.

Actual Result:
Describe what happened.

Evidence:
Add screenshots or relevant error messages when available. Remove passwords, access tokens, and other secrets.

Regression Tests:
List related features that must be retested.
