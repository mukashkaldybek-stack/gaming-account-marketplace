# gaming-account-marketplace
A gaming account marketplace focused on transparency and trust.
Gaming Account Marketplace

A web marketplace concept for browsing gaming account listings, connecting buyers and sellers, and tracking purchase requests with greater transparency.

This project is being developed as part of AI-native development coursework.

1. Project Overview

Buying and selling gaming accounts can involve uncertainty. Buyers may have difficulty evaluating listings, understanding seller information, and tracking the progress of a transaction.

The Gaming Account Marketplace aims to provide a structured platform where users can browse listings, communicate with relevant users, submit purchase requests, and track transaction statuses.

The platform does not guarantee that a transaction is safe or that a gaming account cannot be recovered by its original owner. Supported games must comply with their publishers’ account-sale rules.

2. Project Goals
	•	Make gaming account listings easier to browse and compare.
	•	Provide clear listing information.
	•	Allow sellers to manage their own listings.
	•	Let buyers submit purchase requests.
	•	Make transaction progress visible to authorized participants.
	•	Support private messaging between relevant users.
	•	Allow users to submit complaints with supporting evidence.
	•	Protect private user information through appropriate access controls.
	•	Provide a responsive interface for desktop and mobile devices.

3. Target Users

Buyers

Users who want to browse gaming account listings, compare prices, contact sellers, and submit purchase requests.

Sellers

Users who want to publish gaming account listings, manage their offers, respond to purchase requests, and communicate with buyers.

4. Planned MVP Features

The initial version is planned to include:
	•	Public browsing of gaming account listings.
	•	Search, filtering, and sorting.
	•	Detailed listing pages.
	•	User registration and login.
	•	Seller profiles.
	•	Listing creation and management.
	•	Purchase requests.
	•	Transaction status tracking.
	•	Private text and image messaging.
	•	Complaint submission and evidence storage.
	•	Responsive desktop and mobile layouts.
	•	English-language interface.
	•	SQLite persistent storage.

These are planned features. Their presence in this document does not mean they have already been implemented or tested.

5. Features Planned for Later

Potential post-MVP features include:
	•	Real payment integration.
	•	Advanced seller verification.
	•	Ratings and reviews based on genuine completed transactions.
	•	An administrative interface for reviewing complaints and reports.
	•	Additional game-specific search filters.
	•	Google sign-in.
	•	More advanced spam and fraud prevention.

Payment protection, escrow, and refunds must not be advertised as available unless the corresponding systems are implemented and tested.

6. Development Approach

The project follows a spec-driven and issue-based development process.

The required development sequence is:
	1.	Review and refine the project specifications.
	2.	Build the frontend using mock data and mockService.
	3.	Define the API contract in openapi.yml.
	4.	Implement the backend with temporary in-memory storage.
	5.	Replace temporary storage with SQLite using a DBMS-agnostic ORM.
	6.	Connect the frontend to the backend.
	7.	Test the integrated application and fix identified bugs.

GitHub Issues are used to organize implementation tasks, acceptance criteria, and testing.

7. Technology Requirements

The project must use:
	•	A web frontend.
	•	A backend API.
	•	SQLite for persistent data storage.
	•	A DBMS-agnostic ORM.
	•	An API contract documented in openapi.yml.
	•	Automated and manual testing appropriate to the implemented features.

The exact framework and library choices must follow the approved technical plan.

8. Project Documentation

Important project documents:
	•	chat-brainstorm.md — brainstorming history and project decisions.
	•	AGENTS.md — general project instructions.
	•	CLAUDE.md — Claude AI development instructions.
	•	_docs/plan.md — project plan and requirements.
	•	_docs/process.md — development and testing workflow.
	•	_docs/task-template.md — GitHub Issue template.
	•	_docs/team/pm.md — Project Manager role.
	•	_docs/team/software-engineer.md — Software Engineer role.
	•	_docs/team/qa-engineer.md — QA Engineer role.
	•	openapi.yml — API contract, to be completed in the API-contract phase.

9. Privacy and Trust

The project must follow these principles:
	•	Users must not access private information belonging to other users.
	•	Gaming account passwords must not be requested or stored.
	•	Uploaded images must be validated.
	•	Seller verification must not be claimed without a real verification process.
	•	Ratings and transaction records must not be invented.
	•	Complaints must not automatically be treated as proof of wrongdoing.
	•	Games whose publishers prohibit account sales must not be supported.

10. Testing

The application must be tested throughout development.

Testing should cover:
	•	Listing creation and management.
	•	Search, filtering, and sorting.
	•	Registration and login.
	•	Authorization and private data access.
	•	Purchase requests and transaction statuses.
	•	Private messaging and image uploads.
	•	Complaint submission.
	•	SQLite persistence across application restarts.
	•	Responsive layouts.
	•	Regression testing after bug fixes.

Only functionality that has actually been implemented and tested should be reported as complete.

11. Running the Project

Setup and run instructions will be added after the application framework, dependencies, and development scripts have been established.

The project is currently in development. Do not assume that the application can be run until the required implementation and setup instructions are available.

12. Project Status

Current stage: Project documentation and planning.

The application will be implemented incrementally according to the documented development process and GitHub Issues.
