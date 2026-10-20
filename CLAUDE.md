Claude AI Instructions

1. Project Context

This project is a Gaming Account Marketplace designed to help buyers and sellers trade gaming accounts with better transparency and clearer transaction tracking.

The project is developed as part of AI-native development coursework.

The developer is a beginner, so all development steps must be explained clearly and implemented incrementally.

Before making any changes, read:
	•	AGENTS.md
	•	README.md
	•	_docs/plan.md
	•	_docs/process.md
	•	_docs/task-template.md
	•	_docs/team/pm.md
	•	_docs/team/software-engineer.md
	•	_docs/team/qa-engineer.md

Follow the project requirements and the development sequence described in these documents.

2. Main Development Rules
	•	Follow spec-driven development.
	•	Work from documented requirements and GitHub Issues.
	•	Do not implement features that are outside the approved scope of the current issue.
	•	Keep changes small, understandable, and testable.
	•	Explain important decisions in beginner-friendly language.
	•	Do not assume a feature works without testing it.
	•	Do not mark an issue as completed until its acceptance criteria are satisfied.
	•	Do not invent requirements or silently change agreed project decisions.
	•	If requirements conflict or are unclear, explain the conflict and ask for clarification.

3. Required Development Sequence

Follow this sequence:
	1.	Review and refine project specifications.
	2.	Prepare the frontend design and user interface using mock data and mockService.
	3.	Define the API contract in openapi.yml.
	4.	Implement the backend with temporary in-memory storage.
	5.	Replace in-memory storage with SQLite using a DBMS-agnostic ORM.
	6.	Connect the frontend to the backend.
	7.	Test the complete application and fix discovered bugs.

Do not skip stages or start a later stage prematurely.

4. Project Scope

The MVP should support:
	•	Public browsing of gaming account listings.
	•	Searching, filtering, sorting, and viewing listing details.
	•	User registration and login.
	•	Seller profiles.
	•	Creating, editing, hiding, deleting, and marking listings as sold, where appropriate.
	•	Purchase requests.
	•	Transaction status tracking.
	•	Private text and image messaging between relevant users.
	•	Complaint submission with a reason and supporting evidence.
	•	Responsive layouts for desktop and mobile.
	•	English-language interface.
	•	A professional gaming-inspired design.

Consult _docs/plan.md for the complete requirements.

5. Security and Trust
	•	Never request or store gaming account passwords or other unnecessary sensitive credentials.
	•	Enforce authorization on the backend, not only in the frontend.
	•	Users must only access private information and conversations they are authorized to see.
	•	Validate and sanitize user input.
	•	Validate uploaded image types and sizes.
	•	Prevent users from editing or deleting other users’ listings.
	•	Preserve transaction history when listing information changes.
	•	Do not claim that a seller is verified unless the verification process has actually occurred.
	•	Do not invent seller ratings, reviews, or transaction history.
	•	Do not claim that payments, escrow, refunds, or buyer protection exist unless implemented and tested.
	•	Do not present a complaint or report as proof of fraud.
	•	Support only games whose publishers’ rules permit account sales. If permission is unclear, flag the uncertainty instead of assuming sales are allowed.

6. GitHub Issues
	•	Treat GitHub Issues as the source of truth for planned work.
	•	Follow the issue’s Goal, Description, acceptance criteria, and test cases.
	•	Use the labels mvp, post-mvp, and user-test-bug according to the project’s workflow.
	•	Keep changes connected to the relevant issue.
	•	Do not close an issue simply because code has been written.
	•	Close issues only after the required implementation and testing are complete.
	•	Follow the bug workflow in AGENTS.md and _docs/process.md.

7. Testing
	•	Add tests for important functionality.
	•	Test successful and unsuccessful scenarios.
	•	Test input validation and authorization.
	•	Test transaction status transitions.
	•	Test listing search, filtering, and sorting.
	•	Test complaint submission and private messaging.
	•	Check responsive layouts.
	•	Run relevant tests after changes and report the actual results.
	•	Never claim tests passed if they were not run.

8. Code Quality
	•	Prefer clear, maintainable code over unnecessary complexity.
	•	Use reusable components where appropriate.
	•	Keep frontend, backend, business logic, and data access responsibilities organized.
	•	Use SQLite for persistent storage.
	•	Use a DBMS-agnostic ORM for database access.
	•	Avoid unnecessary dependencies.
	•	Never commit passwords, API keys, access tokens, or other secrets.
	•	Update documentation when implementation changes affect documented behavior.

9. Working with a Beginner

For every development task:
	1.	Explain the goal in simple language.
	2.	Identify the GitHub Issue being implemented.
	3.	Describe the planned changes briefly.
	4.	Implement only the agreed scope.
	5.	Explain which files were created or modified.
	6.	Run appropriate tests and report the results.
	7.	Explain any manual steps the developer must complete.
	8.	Identify the next logical step without skipping required stages.

Do not overwhelm the developer with unrelated tasks.

10. Completion Criteria

A task is complete only when:
	•	Its acceptance criteria are satisfied.
	•	The implementation matches the project specification.
	•	Relevant tests have been run.
	•	Known failures are reported honestly.
	•	Necessary documentation is updated.
	•	The related GitHub Issue can be reviewed against its requirements.

The overall MVP is complete only after the application is implemented, connected to persistent SQLite storage, and thoroughly tested.
