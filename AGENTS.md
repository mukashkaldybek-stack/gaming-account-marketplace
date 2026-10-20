1. Project Overview

This repository contains Gaming Account Marketplace, a responsive web application for browsing, buying, and selling gaming accounts for games whose applicable publisher rules permit account sales.

The project is developed for AI-native development coursework.

The goal is to build a functional, well-tested marketplace through specification-driven development, GitHub Issues, clear project documentation, and incremental implementation.

2. Read the Documentation First

Before making changes, read the relevant project documents:
	1.	_docs/plan.md — project goals, scope, features, requirements, and technical constraints.
	2.	_docs/process.md — required development workflow.
	3.	_docs/team/pm.md — product planning and issue refinement.
	4.	_docs/team/software-engineer.md — implementation rules.
	5.	_docs/team/qa-engineer.md — testing and defect-handling rules.
	6.	_docs/task-template.md — GitHub Issue structure.

Read CLAUDE.md as well when working through Claude-specific instructions.

If a task conflicts with the project plan or coursework requirements, do not silently change the requirements. Identify the conflict and explain it.

3. Required Development Sequence

Follow this sequence without skipping stages:
	1.	Build the frontend using mock data and a mockService.
	2.	Define the API contract in openapi.yml.
	3.	Implement the backend using in-memory storage.
	4.	Replace in-memory storage with SQLite persistence through a database-agnostic ORM.
	5.	Integrate the frontend with the real backend.
	6.	Test the complete application and fix defects.

Do not implement the entire application in one unreviewed step.

Before moving to the next stage, verify that the current stage works and its relevant acceptance criteria are satisfied.

4. General Development Rules
	•	Inspect the existing repository before changing files.
	•	Follow the existing architecture and coding conventions.
	•	Prefer simple, maintainable solutions suitable for a beginner-friendly project.
	•	Keep changes focused on the current GitHub Issue.
	•	Do not rewrite unrelated code.
	•	Do not introduce unnecessary dependencies.
	•	Do not create duplicate files or nested copies of existing directories.
	•	Update documentation when implementation decisions or behavior change.
	•	Never claim a feature is complete without verifying it.
	•	Never claim tests passed unless they were actually run.
	•	Do not invent test results, user feedback, ratings, or verification outcomes.
	•	Explain important decisions clearly.

5. Product Requirements

The MVP includes:
	•	Public marketplace browsing.
	•	Listing search, filtering, and sorting.
	•	User registration and login.
	•	Seller profiles.
	•	Listing creation and management.
	•	Purchase requests.
	•	Transaction status tracking.
	•	Private buyer-seller messaging with supported images.
	•	Complaint and suspicious-listing reporting.
	•	Responsive design.
	•	Dark Mode and Light Mode, provided they do not delay essential functionality.
	•	SQLite persistence through a database-agnostic ORM in the final architecture.

Use _docs/plan.md as the authoritative description of the product scope.

6. Security and Privacy
	•	Enforce authentication and authorization on the server.
	•	Users must only manage their own listings.
	•	Private conversations must only be accessible to authorized participants.
	•	Transaction data must be restricted to authorized participants.
	•	Never store passwords as plain text.
	•	Validate user input on the server.
	•	Validate uploaded file types and sizes.
	•	Do not expose private information through public pages or API responses.
	•	Never request gaming account passwords or recovery codes.
	•	Never invent identity-verification or seller-trust claims.

7. Publisher Policies and Honest Claims

Only support games whose applicable official rules permit account sales.

Do not assume that account sales are allowed when a publisher’s policy is unclear.

The MVP does not provide real payments, escrow, automatic refunds, or guaranteed account-transfer protection.

Do not claim that the platform eliminates fraud or guarantees account ownership after transfer.

Complaints are reports, not confirmed findings.

Verification indicators may only be displayed when the corresponding verification process has actually been implemented and completed.

8. GitHub Issues

Use GitHub Issues to organize development.

Required labels:
	•	mvp
	•	post-mvp
	•	user-test-bug

Each implementation issue should have a clear goal, description, and acceptance criteria.

Work on the requested issue without silently expanding its scope.

Do not close an issue until its acceptance criteria have been verified.

When a user-testing defect is discovered:
	1.	Create an issue describing the goal and defect.
	2.	Apply the user-test-bug label.
	3.	Ask the Product Manager role to refine the issue.
	4.	Ask the QA Engineer role to add relevant test cases.
	5.	Fix the defect.
	6.	Run the relevant tests.
	7.	Close the issue only after verification.

9. Testing Requirements

Test relevant functionality at each development stage.

Prioritize:
	•	Input validation.
	•	Authentication and authorization.
	•	Listing ownership and management.
	•	Purchase-request rules.
	•	Transaction-status transitions.
	•	Private-message access control.
	•	Complaint submission.
	•	Database persistence.
	•	Frontend-backend integration.
	•	Responsive layouts.
	•	Regression testing after fixes.

Never report a test as successful without running it.

10. Definition of Done

A feature is complete only when:
	•	It matches the documented requirements.
	•	Its acceptance criteria are satisfied.
	•	Required validation and access controls are implemented.
	•	Relevant tests have been run and passed.
	•	Related functionality has been checked for regressions.
	•	Relevant documentation has been updated.
	•	Its GitHub Issue is ready to close.

11. Communication

When explaining work to the project owner:
	•	Use clear, beginner-friendly language.
	•	Summarize the changes made.
	•	Explain how to verify the result.
	•	Identify remaining work and limitations.
	•	Be explicit when an action has not been performed.
	•	Never claim to have changed GitHub files or run commands unless that actually happened.

The priority is to deliver a functional, maintainable, and thoroughly tested MVP that follows the coursework requirements.
