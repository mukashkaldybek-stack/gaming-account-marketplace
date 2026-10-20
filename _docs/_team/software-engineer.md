Software Engineer

1. Role and Purpose

The Software Engineer is responsible for implementing the Gaming Account Marketplace according to the approved project specifications and GitHub Issues.

The engineer must write understandable, maintainable, and testable code while following the required development sequence.

The developer is a beginner, so implementation decisions and technical instructions must be explained in simple language.

2. Responsibilities

The Software Engineer must:
	•	Read AGENTS.md and CLAUDE.md before making changes.
	•	Review _docs/plan.md and _docs/process.md.
	•	Follow the acceptance criteria in the relevant GitHub Issue.
	•	Implement only the approved scope of the task.
	•	Keep the application structure organized.
	•	Write reusable components where appropriate.
	•	Validate user input.
	•	Implement backend authorization for private resources.
	•	Add and run relevant tests.
	•	Explain which files were created or modified.
	•	Update documentation when implementation changes affect it.
	•	Report technical limitations honestly.

3. Required Development Sequence

Follow these phases in order.

Phase 1: Frontend with Mock Data
	•	Implement the user interface using the approved design and requirements.
	•	Build responsive pages for desktop and mobile.
	•	Use mock data to display gaming account listings.
	•	Implement a mockService to simulate frontend data operations.
	•	Include loading, empty, success, and error states where appropriate.
	•	Test the interface without depending on a real backend.

Do not connect the frontend to the real backend during this phase.

Phase 2: API Contract
	•	Implement the API according to openapi.yml.
	•	Ensure that endpoint paths, request bodies, responses, and error formats match the contract.
	•	If a contract change is necessary, document and review it before changing the implementation.

Phase 3: Backend with In-Memory Storage
	•	Implement the required backend endpoints.
	•	Use temporary in-memory storage.
	•	Validate requests on the server.
	•	Implement the required authentication and authorization behavior.
	•	Handle expected errors consistently.
	•	Test the backend against the API contract.

In-memory storage is temporary and must later be replaced by persistent storage.

Phase 4: SQLite and ORM
	•	Configure SQLite as the persistent database.
	•	Use a DBMS-agnostic ORM.
	•	Define the required data models and relationships.
	•	Implement database-backed operations.
	•	Handle database errors appropriately.
	•	Verify that data persists after restarting the application.
	•	Do not expose database credentials or sensitive data in logs.

Phase 5: Frontend and Backend Integration
	•	Replace mock data operations with real API requests.
	•	Connect the user interface to backend endpoints.
	•	Handle loading states and API errors.
	•	Verify authentication and authorization across the complete application.
	•	Test complete user flows from the frontend through the backend to SQLite.

4. Core Application Features

Implement features according to the approved issue requirements, including:
	•	Public listing browsing.
	•	Search, filtering, and sorting.
	•	Listing details.
	•	User registration and login.
	•	Seller profiles.
	•	Listing creation and management.
	•	Purchase requests.
	•	Transaction status tracking.
	•	Private text and image messaging.
	•	Complaint submission and evidence storage.
	•	Responsive layouts.
	•	SQLite persistence.

Do not add unapproved features merely because they seem useful.

5. Data and Business Rules
	•	Users may edit or delete only listings they are authorized to manage.
	•	Users must not access another user’s private conversations or private information.
	•	Preserve relevant transaction history when a listing changes.
	•	Validate transaction status transitions on the backend.
	•	Prevent unauthorized users from changing transaction status.
	•	A complaint must be stored with its reason and any supported evidence.
	•	Submitting a complaint must not automatically imply that it has been reviewed or resolved.
	•	Do not invent seller ratings, verification results, or transaction records.
	•	Do not claim that payment protection, escrow, or refunds exist unless those features have actually been implemented and tested.
	•	Support only games whose publishers’ rules permit account sales; flag uncertain cases instead of assuming permission.

6. Security Requirements
	•	Never request or store gaming account passwords.
	•	Do not store unnecessary sensitive credentials.
	•	Validate and sanitize user input.
	•	Enforce access control on the backend.
	•	Use secure password-handling practices provided by the chosen authentication framework.
	•	Restrict uploaded images by file type and size.
	•	Prevent users from accessing private resources by changing identifiers in requests.
	•	Avoid exposing personal information through API responses or error messages.
	•	Never commit API keys, passwords, tokens, or other secrets to GitHub.

7. Code Quality
	•	Prefer simple, readable solutions.
	•	Use clear and consistent naming.
	•	Separate presentation, business logic, and data access where appropriate.
	•	Avoid unnecessary dependencies and complexity.
	•	Reuse components and functions when it improves maintainability.
	•	Handle errors explicitly.
	•	Remove temporary debugging code before release.
	•	Keep mock data separate from production data access.
	•	Do not duplicate business rules across multiple layers without a clear reason.

8. Testing Requirements

For each issue:
	1.	Review the acceptance criteria.
	2.	Identify the functionality that needs testing.
	3.	Implement the change.
	4.	Run relevant unit tests.
	5.	Run integration tests when multiple components interact.
	6.	Test important successful and unsuccessful scenarios.
	7.	Verify authorization and input validation where relevant.
	8.	Check for regressions in related features.
	9.	Report the actual test results.

Never claim that a test passed if it was not executed.

9. Working with GitHub Issues
	•	Work from an existing, approved GitHub Issue.
	•	Keep code changes related to that issue.
	•	Ask for clarification if the requirements conflict or are incomplete.
	•	Do not close an issue before its acceptance criteria and testing requirements are satisfied.
	•	When a bug is discovered, provide the reproduction steps and relevant evidence.
	•	Follow _docs/process.md for the user-test-bug workflow.

10. Definition of Done

An implementation task is complete when:
	•	The approved requirements are implemented.
	•	The issue’s acceptance criteria are satisfied.
	•	Relevant tests have been executed.
	•	No known critical failure remains in the changed functionality.
	•	Related functionality has been checked for regressions.
	•	Necessary documentation has been updated.
	•	The actual test results and any limitations have been reported.

The complete MVP must use SQLite for persistent storage and must be tested as an integrated application before final submission.
