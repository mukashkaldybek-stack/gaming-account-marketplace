Gaming Account Marketplace — Project Plan

1. Project Overview

Project Name: Gaming Account Marketplace

Project Type: Responsive web application

Target Users: Gamers who want to buy or sell gaming accounts.

Primary Language: English

Database: SQLite

ORM: A database-agnostic ORM compatible with SQLite.

Description

Gaming Account Marketplace is a web platform where users can browse, search, buy, and sell gaming accounts for games that permit account sales under their applicable official rules.

The platform aims to make account trading more transparent by providing detailed listings, seller profiles, purchase requests, transaction status tracking, private messaging, and complaint submission.

The MVP will not include real payments, escrow, automatic refunds, or guaranteed account-transfer protection.

2. Problem Statement

Gaming account buyers and sellers may face several problems:
	•	Listings may contain incomplete or misleading information.
	•	Buyers may find it difficult to compare available offers.
	•	Buyers and sellers may lack a clear record of transaction progress.
	•	Communication may happen across unrelated platforms.
	•	Users may not have a structured way to report suspicious listings or transaction problems.
	•	Verification claims may be difficult to evaluate.

The project addresses these problems by organizing listings, communication, purchase requests, transaction tracking, and complaints in one platform.

The platform cannot eliminate fraud or guarantee that a gaming account will remain accessible after transfer.

3. Project Goals

The main goals are to:
	1.	Build a searchable marketplace for eligible gaming accounts.
	2.	Allow registered users to create and manage listings.
	3.	Help buyers compare offers using prices, game names, and listing statuses.
	4.	Allow buyers to send purchase requests to sellers.
	5.	Track transaction progress using defined statuses.
	6.	Provide private communication between buyers and sellers.
	7.	Allow users to submit complaints and suspicious-listing reports.
	8.	Protect private user information through authentication and access control.
	9.	Provide a responsive interface for desktop and mobile devices.
	10.	Follow a specification-driven, issue-based AI-native development process.

4. Target Users

4.1 Buyers

Buyers need to:
	•	Browse listings without logging in.
	•	Search and filter available offers.
	•	View listing details and seller information.
	•	Register or log in to send purchase requests.
	•	Communicate privately with sellers.
	•	Track their transactions.
	•	Submit complaints when problems occur.

4.2 Sellers

Sellers need to:
	•	Register and log in.
	•	Create gaming account listings.
	•	Edit, hide, republish, or delete their own listings.
	•	Mark listings as sold or unavailable.
	•	Receive and respond to purchase requests.
	•	Communicate with buyers.
	•	Track transaction progress.
	•	Submit complaints when necessary.

4.3 Administrators

A full administrative dashboard is outside the initial MVP scope.

However, the application should store reports and complaints in a structured format so that administrative review can be added later.

5. MVP Features

The MVP is the first usable version of the application. It focuses on marketplace functionality without real payment processing.

5.1 Public Marketplace

Visitors can:
	•	Browse published listings without logging in.
	•	Search listings by game name or relevant keywords.
	•	Filter listings by minimum and maximum price.
	•	Filter by availability status.
	•	Sort listings by price or publication date.
	•	View listing details.
	•	View public seller profile information.

5.2 Authentication

Users can:
	•	Register using an email address and password.
	•	Log in and log out.
	•	Access their own account area.
	•	Use authenticated features such as publishing listings, sending purchase requests, and private messaging.

The server must enforce authentication and authorization.

Google login is a possible post-MVP feature.

5.3 Seller Profiles

Seller profiles can display:
	•	Username.
	•	Registration date.
	•	Published listings.
	•	Email verification status, only if email verification is actually implemented.

The MVP must not display fabricated ratings, reviews, or verification badges.

Email verification confirms control of an email address, not a person’s identity or trustworthiness.

5.4 Listing Management

Registered users can create listings containing:
	•	Game name.
	•	Listing title.
	•	Account description.
	•	Price.
	•	Screenshots.
	•	Main account characteristics.
	•	Availability status.
	•	Publication date.
	•	Seller information.

Sellers can:
	•	Create listings.
	•	Edit their own listings.
	•	Delete their own listings when permitted.
	•	Hide or republish listings.
	•	Mark listings as sold or unavailable.

Required fields must be validated.

The application must not request gaming account passwords or recovery codes.

Listing changes must not silently corrupt existing transaction history.

5.5 Search, Filtering, and Sorting

Users can:
	•	Search by game name or keywords.
	•	Filter by minimum price.
	•	Filter by maximum price.
	•	Filter by availability status.
	•	Sort by price from low to high.
	•	Sort by price from high to low.
	•	Sort by newest listings.
	•	Sort by oldest listings.

Seller-rating filters may be added when genuine ratings based on a defined process exist.

5.6 Purchase Requests

Buyers can send purchase requests for available listings.

Sellers can accept or reject pending requests.

The system must prevent invalid requests, such as requests for unavailable listings.

The MVP records purchase requests and their statuses but does not process real payments.

A purchase request does not mean payment has occurred or ownership has been transferred.

5.7 Transaction Tracking

Transactions use the following statuses:
	1.	Request Sent — the buyer has submitted a purchase request.
	2.	Accepted — the seller has accepted the request.
	3.	Transfer in Progress — the parties indicate that the transfer process is underway.
	4.	Completed — both parties have confirmed completion.
	5.	Disputed — a participant has submitted a complaint about the transaction.
	6.	Cancelled — the transaction has been cancelled according to the permitted rules.

The application must validate permitted status transitions and record who made each change and when.

Completion requires confirmation from both parties.

A transaction can be disputed when either participant submits a complaint.

Transaction tracking does not guarantee successful transfer, prevent account recovery by a previous owner, or provide financial protection.

5.8 Private Chat

Buyers and sellers can communicate through private conversations associated with a listing or transaction.

The MVP supports:
	•	Sending text messages.
	•	Sharing screenshots or images.
	•	Viewing conversation history.
	•	Restricting conversations to authorized participants.

Uploaded images must be validated for permitted file types and sizes.

The server must verify that users are authorized to read or send messages.

5.9 Complaints and Reports

Users can submit complaints about listings or transactions.

A complaint can include:
	•	Related listing or transaction.
	•	Complaint reason.
	•	Description of the problem.
	•	Supporting screenshots, where supported.

The system stores submitted complaints for possible future review.

Users can also report suspicious listings.

The MVP does not include a complete administrative investigation system.

A complaint is an allegation, not proof of wrongdoing. Submitting a complaint does not guarantee a resolution or refund.

5.10 Responsive Interface

The website must work on:
	•	Desktop computers.
	•	Tablets.
	•	Mobile phones.

The design should combine a professional marketplace layout with a gaming-inspired visual style.

Dark Mode and Light Mode should be supported in the MVP if they can be implemented without delaying essential functionality.

The initial interface language is English.

6. Post-MVP Features

The following features are planned for possible future versions:
	•	Real payment integration.
	•	Escrow or holding funds during transactions.
	•	Automatic refunds.
	•	Financial transaction protection.
	•	Advanced identity verification.
	•	Genuine transaction-based seller ratings and reviews.
	•	Full administrative dashboard.
	•	Administrative complaint investigation and resolution.
	•	Advanced fraud detection.
	•	More sophisticated spam prevention.
	•	Google authentication.
	•	Game-specific search filters.
	•	Additional interface languages.
	•	Advanced marketplace analytics.
	•	Monetization features.

These features must not be presented as available until they have been implemented and tested.

7. Functional Requirements

FR-01: Public Browsing

The system shall allow visitors to browse published listings without logging in.

FR-02: Search

The system shall allow users to search listings by game name or relevant keywords.

FR-03: Filtering

The system shall allow users to filter listings by price range and availability status.

FR-04: Sorting

The system shall allow users to sort listings by price and publication date.

FR-05: Registration

The system shall allow users to create accounts using email and password.

FR-06: Authentication

The system shall allow registered users to log in and log out securely.

FR-07: Seller Profiles

The system shall display permitted public seller information.

FR-08: Listing Creation

The system shall allow registered users to create listings with all required fields.

FR-09: Listing Management

The system shall allow sellers to manage their own listings.

FR-10: Purchase Requests

The system shall allow buyers to submit requests for available listings.

FR-11: Request Management

The system shall allow sellers to accept or reject pending purchase requests.

FR-12: Transaction Tracking

The system shall maintain transaction statuses and validate permitted transitions.

FR-13: Private Messaging

The system shall allow authorized participants to exchange private text messages and supported images.

FR-14: Complaint Submission

The system shall allow users to submit complaints about relevant listings or transactions.

FR-15: Report Storage

The system shall store listing reports and complaints.

FR-16: Access Control

The system shall prevent users from accessing private data or performing unauthorized actions.

FR-17: Responsive Design

The system shall provide a usable interface across desktop and mobile screen sizes.

FR-18: Publisher Policy Restrictions

The system shall not support listings for games known to prohibit account sales under their applicable official rules.

FR-19: Honest Verification

The system shall display verification indicators only when the corresponding process has actually been completed.

FR-20: Persistent Storage

The final MVP shall persist application data in SQLite using a database-agnostic ORM.

8. Non-Functional Requirements

NFR-01: Security

Passwords must be stored using an appropriate password-hashing mechanism. Sensitive operations must require authentication and server-side authorization.

NFR-02: Privacy

Private messages, transaction details, and account-specific information must only be accessible to authorized users.

NFR-03: Data Integrity

The system must validate inputs and maintain consistent relationships between users, listings, requests, transactions, messages, and complaints.

NFR-04: Reliability

Errors must be handled appropriately. Invalid requests must not corrupt stored data.

NFR-05: Usability

The interface must be understandable to users with limited technical knowledge.

NFR-06: Responsiveness

Core pages must remain usable on mobile and desktop screens.

NFR-07: Maintainability

The codebase must have a clear structure and separate frontend, API, business logic, and data storage responsibilities.

NFR-08: Testability

Critical functionality, validation rules, access control, and transaction-status transitions must be tested.

NFR-09: Honest Communication

The application must not claim guaranteed safety, identity verification, payment completion, refunds, escrow, or successful account transfer unless those capabilities genuinely exist.

NFR-10: Publisher Policy Compliance

The marketplace must respect applicable game-publisher rules and avoid supporting account sales known to be prohibited.

9. Privacy and Security Rules
	1.	Users must authenticate before accessing private account features.
	2.	Users must only manage their own listings, except for explicitly authorized future administrative actions.
	3.	Private conversations must only be accessible to their authorized participants.
	4.	Transaction records must only be accessible to authorized participants.
	5.	Passwords must never be stored as plain text.
	6.	Gaming account passwords and recovery codes must not be requested.
	7.	Uploaded images must be validated.
	8.	Server-side validation is required even when frontend validation exists.
	9.	Sensitive information must not be unnecessarily exposed in logs or public profiles.
	10.	Verification indicators must accurately describe what was verified.
	11.	Complaints must not be presented as confirmed findings without investigation.
	12.	Publisher-policy restrictions must be respected.

10. Technical Requirements

The project must use:
	•	A responsive web frontend.
	•	A backend API documented with OpenAPI.
	•	SQLite for persistent storage.
	•	A database-agnostic ORM.
	•	Automated tests for critical functionality.
	•	GitHub Issues for task management, bug tracking, and completion.

The implementation must follow the required coursework sequence.

11. Required Development Sequence

Phase 1: Frontend with MockService

Build the frontend using mock data and a mock service.

Implement:
	•	Main pages and navigation.
	•	Listing cards and listing details.
	•	Search, filtering, and sorting.
	•	Authentication screens.
	•	Listing-management interfaces.
	•	Purchase requests and transaction statuses.
	•	Private chat interfaces.
	•	Complaint submission.
	•	Responsive layouts.
	•	Loading, empty, and error states.

The frontend must work with mock data before backend integration.

Phase 2: OpenAPI Contract

Create openapi.yml to define:
	•	API endpoints.
	•	Request parameters and bodies.
	•	Response structures.
	•	Error responses.
	•	Authentication requirements.
	•	Input validation rules.

The API contract must match the frontend requirements.

Phase 3: In-Memory Backend

Implement the backend API using temporary in-memory storage.

At this stage:
	•	Implement endpoints from openapi.yml.
	•	Validate incoming requests.
	•	Implement business rules.
	•	Enforce authorization.
	•	Validate transaction-status transitions.
	•	Add backend tests.
	•	Verify compatibility with frontend data structures.

Data loss after a restart is expected during this temporary phase.

Phase 4: SQLite and ORM

Replace temporary storage with SQLite persistence using a database-agnostic ORM.

At this stage:
	•	Define database models and relationships.
	•	Establish a schema-management process.
	•	Persist users, listings, requests, transactions, messages, and complaints.
	•	Verify data integrity.
	•	Test persistence after application restarts.

Phase 5: Frontend-Backend Integration

Connect the frontend to the completed backend.

At this stage:
	•	Replace mock-service calls with real API calls.
	•	Implement loading and error handling.
	•	Verify authentication and access control.
	•	Test complete user workflows.
	•	Confirm SQLite persistence.
	•	Run regression tests.
	•	Fix integration defects.

The MVP is not complete until the main workflows function through the real frontend, backend, and SQLite database.

12. Main Data Entities

User

Represents a registered user.

Possible fields:
	•	ID.
	•	Username.
	•	Email.
	•	Password hash.
	•	Registration date.
	•	Email verification status, if implemented.

Listing

Represents a gaming account offer.

Possible fields:
	•	ID.
	•	Seller ID.
	•	Game name.
	•	Title.
	•	Description.
	•	Price.
	•	Image references.
	•	Availability status.
	•	Publication date.
	•	Last updated date.

PurchaseRequest

Represents a buyer’s request to purchase a listing.

Possible fields:
	•	ID.
	•	Listing ID.
	•	Buyer ID.
	•	Seller ID.
	•	Request status.
	•	Creation date.
	•	Last updated date.

Transaction

Represents a tracked transaction.

Possible fields:
	•	ID.
	•	Purchase request ID.
	•	Buyer ID.
	•	Seller ID.
	•	Transaction status.
	•	Buyer completion confirmation.
	•	Seller completion confirmation.
	•	Creation date.
	•	Last updated date.

Message

Represents a private message.

Possible fields:
	•	ID.
	•	Conversation or transaction ID.
	•	Sender ID.
	•	Message text.
	•	Optional image reference.
	•	Creation date.

Complaint

Represents a complaint submitted by a user.

Possible fields:
	•	ID.
	•	Reporter ID.
	•	Related listing or transaction ID.
	•	Reason.
	•	Description.
	•	Optional evidence references.
	•	Submission date.

ListingReport

Represents a report about a potentially suspicious listing.

Possible fields:
	•	ID.
	•	Reporter ID.
	•	Listing ID.
	•	Report reason.
	•	Description.
	•	Submission date.

These are conceptual models. Their exact structure should be refined during API and database design.

13. Design Direction

The application should combine a professional marketplace layout with a subtle gaming aesthetic.

Visual Style
	•	Dark background with restrained neon accents.
	•	Light theme as an alternative.
	•	Clear typography and readable contrast.
	•	Consistent spacing and reusable components.
	•	Listing cards with clear prices and availability.
	•	Accurate trust indicators.
	•	Responsive layouts.

Main Pages
	1.	Homepage.
	2.	Marketplace and search results.
	3.	Listing details.
	4.	Registration and login.
	5.	User profile.
	6.	Create and edit listing.
	7.	My listings.
	8.	Purchase requests.
	9.	Transaction details.
	10.	Private chat.
	11.	Complaint submission.
	12.	Account settings.

The design should prioritize usability over unnecessary animations.

14. Testing Strategy

Testing must happen throughout development.

Frontend Testing
	•	Check navigation.
	•	Check form validation.
	•	Check search, filters, and sorting.
	•	Check empty states.
	•	Check loading and error states.
	•	Check responsive layouts.
	•	Check Dark Mode and Light Mode if implemented.

Backend Testing
	•	Test successful API requests.
	•	Test invalid input.
	•	Test missing or invalid authentication.
	•	Test unauthorized access to other users’ data.
	•	Test listing permissions.
	•	Test purchase-request rules.
	•	Test valid and invalid transaction-status transitions.
	•	Test complaint and report submission.

Database Testing
	•	Confirm data persists after restart.
	•	Confirm relationships are maintained.
	•	Confirm invalid data is rejected.
	•	Confirm listing changes do not corrupt transaction history.

End-to-End Testing

Test the following workflow:
	1.	A visitor browses the marketplace.
	2.	A user registers and logs in.
	3.	A seller creates a listing.
	4.	A buyer finds the listing and submits a purchase request.
	5.	The seller accepts the request.
	6.	The participants communicate privately.
	7.	The transaction status changes correctly.
	8.	Both parties confirm completion, or a participant submits a complaint.
	9.	The application stores the resulting records.
	10.	Unauthorized users cannot access private information.

After fixes, run the relevant tests again to ensure existing functionality has not broken.

15. GitHub Issues and Development Workflow

GitHub Issues must be used to organize implementation and testing.

Each issue should contain:
	•	A clear title.
	•	A specific goal.
	•	A detailed description.
	•	Acceptance criteria.
	•	Relevant implementation or testing notes.
	•	An appropriate label.

Required labels:
	•	mvp — features required for the initial MVP.
	•	post-mvp — features planned for a future version.
	•	user-test-bug — defects discovered during user testing.

Issues should be small enough to implement and verify independently.

Project Roles

Product Manager (PM)
	•	Reviews requirements.
	•	Refines and prioritizes issues.
	•	Defines acceptance criteria.
	•	Ensures issues match the project plan.

Software Engineer
	•	Implements approved features.
	•	Follows project specifications.
	•	Adds and maintains automated tests.
	•	Updates documentation when necessary.

QA Engineer
	•	Defines and executes tests.
	•	Reports defects.
	•	Verifies fixes.
	•	Closes issues only after their acceptance criteria have been met.

User-Test Bug Workflow

When a defect is discovered:
	1.	Create a GitHub Issue with a goal and description.
	2.	Apply the user-test-bug label.
	3.	Ask the PM role to review and refine the issue.
	4.	Ask the QA role to add relevant test cases.
	5.	Implement the fix.
	6.	Run the relevant tests.
	7.	Close the issue only after verification.

All required mvp and user-test-bug issues must be completed and closed before the coursework deadline.

16. Definition of Done

A feature is complete when:
	•	Its requirements are documented.
	•	Its GitHub Issue has acceptance criteria.
	•	Its implementation follows the project specifications.
	•	Necessary validation and access control are implemented.
	•	Relevant tests pass.
	•	The feature works in the actual application.
	•	Related functionality has been regression-tested.
	•	Documentation is updated.
	•	The issue is closed only after verification.

The MVP is complete when the main workflows work correctly, data persists in SQLite, the application has been thoroughly tested, and no unresolved blocking defects remain.

17. Project Risks and Constraints

Publisher Restrictions

Some publishers prohibit account sales or restrict account transfers.

Mitigation: Support only games whose applicable official rules permit account sales. Do not assume unclear policies allow trading.

Fraud and Misrepresentation

A seller may provide misleading information, or an account may later be recovered by its previous owner.

Mitigation: Provide structured listings, transaction tracking, private messaging, and complaint submission. Do not claim these features eliminate fraud.

Scope Creep

Real payments, escrow, advanced identity verification, and administrative workflows can increase implementation complexity.

Mitigation: Keep the MVP focused on the features defined in this document.

Privacy and Unauthorized Access

Private messages and transaction information could be exposed through implementation mistakes.

Mitigation: Enforce server-side authentication and authorization and test access-control rules.

Beginner Development Experience

Complex architecture may make the project difficult to complete.

Mitigation: Use a simple, documented architecture and implement one development phase at a time.

18. Success Criteria

The MVP will be successful when:
	1.	Visitors can browse and search supported listings.
	2.	Users can register and log in.
	3.	Sellers can create and manage their own listings.
	4.	Buyers can submit purchase requests.
	5.	Sellers can respond to purchase requests.
	6.	Transactions follow valid status transitions.
	7.	Authorized participants can exchange private messages and supported images.
	8.	Users can submit complaints and listing reports.
	9.	Users cannot access other users’ private data.
	10.	Data persists in SQLite.
	11.	The frontend communicates successfully with the backend API.
	12.	The main workflows pass testing.
	13.	The interface works on mobile and desktop.
	14.	Documentation and GitHub Issues reflect the implemented behavior.
	15.	The application does not claim unsupported features or protections.

⸻

Final Principle: Build a transparent and usable marketplace first. Add advanced trust, payment, and administrative features only when they can be implemented reliably, tested thoroughly, and described honestly.
