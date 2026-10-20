Development Process

1. Purpose

This document defines the development workflow for the Gaming Account Marketplace.

The project follows spec-driven, issue-based, and iterative development. Requirements are documented before implementation, work is divided into GitHub Issues, and completed features are tested before their issues are closed.

2. General Workflow

For each feature or task, follow these steps:
	1.	Review the project requirements in _docs/plan.md.
	2.	Identify or create the relevant GitHub Issue.
	3.	Define the issue’s goal, description, acceptance criteria, and test cases.
	4.	Ask the Project Manager role to review and refine the issue.
	5.	Ask the QA Engineer role to identify test scenarios.
	6.	Implement the feature according to the approved requirements.
	7.	Run the relevant tests.
	8.	Fix any discovered bugs.
	9.	Update documentation when necessary.
	10.	Close the issue only after all acceptance criteria have been met and the required tests have passed.

Do not implement unrelated features while working on an issue.

3. Required Development Phases

Development must follow this order.

Phase 1: Specifications and Planning
	•	Review the project idea and brainstorming history.
	•	Finalize MVP requirements.
	•	Identify functional and non-functional requirements.
	•	Create GitHub Issues for planned work.
	•	Define acceptance criteria and test scenarios.

Phase 2: Frontend with Mock Data
	•	Design the main pages and user flows.
	•	Implement the frontend using mock data.
	•	Create a mockService to simulate data operations.
	•	Test the user interface without a real backend.
	•	Check responsive layouts on desktop and mobile.

The interface should be usable before real backend integration begins.

Phase 3: API Contract
	•	Define the API contract in openapi.yml.
	•	Document endpoints, request bodies, responses, and error cases.
	•	Keep the API contract consistent with the frontend requirements.
	•	Review the contract before implementing the backend.

Phase 4: Backend with In-Memory Storage
	•	Implement the backend API.
	•	Use temporary in-memory storage.
	•	Validate requests and handle errors.
	•	Implement authentication and authorization requirements.
	•	Test API behavior against the documented contract.

In-memory storage is temporary and is not the final persistence solution.

Phase 5: SQLite Persistence
	•	Configure SQLite.
	•	Use a DBMS-agnostic ORM.
	•	Define the necessary data models and relationships.
	•	Replace temporary in-memory storage with database-backed operations.
	•	Test data creation, reading, updating, and deletion.
	•	Verify that data remains available after the application restarts.

Phase 6: Frontend and Backend Integration
	•	Connect the frontend to the backend API.
	•	Replace mock data operations with real API requests.
	•	Handle loading states, empty states, validation errors, and server errors.
	•	Test complete user flows from the interface to the database.

Phase 7: Final Testing and Bug Fixing
	•	Run unit and integration tests.
	•	Test important end-to-end user flows.
	•	Check authentication and authorization.
	•	Test transaction status changes and complaint submission.
	•	Test private messaging and image upload restrictions.
	•	Check responsive layouts.
	•	Create GitHub Issues for discovered bugs.
	•	Fix and retest bugs before the final release.

4. GitHub Issue Structure

Each implementation issue should contain:

Goal

A short statement explaining what the task should achieve.

Description

Explain:
	•	What needs to be implemented.
	•	Why it is needed.
	•	Which part of the application it affects.
	•	Any important constraints or dependencies.

Acceptance Criteria

List clear conditions that must be satisfied before the issue can be closed.

Test Cases

Describe how the feature should be tested, including successful and unsuccessful scenarios where relevant.

Dependencies

Identify any tasks that must be completed first.

Use _docs/task-template.md when creating issues.

5. Issue Labels

Use the following labels consistently.

mvp

Required work for the minimum viable product.

All issues labeled mvp must be completed and closed before the final submission.

post-mvp

Useful features intentionally postponed until after the MVP.

These features must not delay completion of required MVP functionality.

user-test-bug

Bugs discovered while manually testing the application.

Each bug issue must include:
	•	Goal
	•	Description
	•	Steps to reproduce
	•	Expected result
	•	Actual result
	•	Relevant screenshots or error messages, if available
	•	Acceptance criteria
	•	QA test cases

The Project Manager should review and refine the issue, and the QA Engineer should verify the fix before closure.

6. Bug-Fixing Workflow

When a bug is discovered:
	1.	Stop and document the problem.
	2.	Create a GitHub Issue with the user-test-bug label.
	3.	Describe the steps needed to reproduce the bug.
	4.	Record the expected and actual behavior.
	5.	Ask the Project Manager role to review and refine the issue.
	6.	Ask the QA Engineer role to add test cases.
	7.	Ask the Software Engineer role to investigate and implement a fix.
	8.	Run the relevant tests.
	9.	Reproduce the original scenario to confirm that the bug is fixed.
	10.	Check for regressions in related features.
	11.	Close the issue only after the fix has been verified.

Do not hide known bugs or claim that an issue is fixed without testing it.

7. Testing Strategy

Use several testing levels.

Unit Testing

Test individual functions and components in isolation.

Integration Testing

Test interactions between components, API endpoints, and the database.

End-to-End Testing

Test complete user journeys through the application.

Manual Testing

Use the application as a real user would and check the visible behavior.

Regression Testing

After fixing a bug or changing a feature, retest related functionality to ensure existing behavior still works.

Testing must include both valid inputs and relevant invalid or unauthorized requests.

8. Security and Privacy
	•	Users must not access another user’s private information.
	•	Backend authorization must protect private resources.
	•	Validate user input on the server.
	•	Restrict uploaded image types and file sizes.
	•	Do not store gaming account passwords or unnecessary sensitive credentials.
	•	Do not expose secrets in source code or logs.
	•	Preserve transaction history.
	•	Do not claim payment protection, escrow, or refunds unless those capabilities have been implemented and tested.
	•	Do not claim that an account listing or seller is verified without a real verification process.

9. Documentation

Update project documentation whenever requirements, architecture, API behavior, or implementation decisions change.

Keep these files consistent:
	•	AGENTS.md
	•	CLAUDE.md
	•	README.md
	•	_docs/plan.md
	•	_docs/process.md
	•	_docs/task-template.md
	•	_docs/team/pm.md
	•	_docs/team/software-engineer.md
	•	_docs/team/qa-engineer.md
	•	openapi.yml, when the API contract phase begins

Do not create conflicting instructions across documents.

10. Definition of Done

A GitHub Issue can be closed when:
	•	Its acceptance criteria are satisfied.
	•	The implementation follows the approved specification.
	•	Relevant tests have been run.
	•	The tests pass, or any remaining limitations are explicitly documented.
	•	Related functionality has been checked for regressions.
	•	Necessary documentation has been updated.
	•	The QA Engineer has verified the result according to the project workflow.

The MVP is ready for submission only when the required MVP functionality has been implemented, the frontend and backend are connected, persistent SQLite storage works, and the application has been thoroughly tested.
