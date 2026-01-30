---
icon: book-open
---

# Requirements Definition

Before we start developing anything, we need to define and outline the system requirements.

### Task Definition: Objective

We need to define the purpose of a task or feature. What does it intend to achieve? Why is it being developed?

#### Example

* To enable users to reserve a book online from a library catalog, ensuring that the book is set aside for them for a specified period. This feature aims to streamline the book borrowing process and improve user convenience by allowing reservations to be made remotely.

### Task Definition: Functional Requirements

Functional requirements specify what the feature must do. These requirements describe the functionality that the system must provide to achieve the objective. They often include user interactions, data handling, and any rules or conditions that must be enforced. These will be defined in more detail in the Determining Specifications Phase.

#### Example

* Users must be able to search for books by title, author, or ISBN.
* Users should have the ability to view book availability status (available, reserved, checked out).
* Users must be able to select a book and place a reservation.
* The system should prevent a user from reserving a book that is already checked out or reserved by another user.
* The system must send a confirmation notification to the user upon successful reservation.
* Users should be able to cancel their reservation if needed.

### Task Definition: Non-Functional Requirements

Non-functional requirements define the quality attributes or constraints of the system. These requirements address aspects such as performance, usability, reliability, and security, which affect how the system performs its functions. These will be defined in more detail in the Determining Specifications Phase.

#### Example

* The book reservation process should complete within 2 seconds of the user submitting a reservation request.
* The system must be available 99.9% of the time, ensuring high reliability and uptime.
* User data and reservation details must be encrypted to ensure security and privacy.
* The feature should be accessible and usable on both desktop and mobile devices, adhering to responsive design principles.

### Task Definition: Constraints

Constraints are the limitations or restrictions that must be considered during the development of the feature. These could be technical, legal, regulatory, or organisational constraints.

#### Example

* The feature must integrate with the existing library management system without requiring significant changes to the database schema.
* The solution must comply with data protection regulations (e.g., GDPR, CCPA) concerning user data storage and handling.
* The feature should be implemented using the existing technology stack (e.g., Django for the backend, React for the frontend).
* The project budget is limited, so the solution should be cost-effective without requiring additional third-party licenses or services.

### Task Definition: Acceptance Criteria

Acceptance criteria are the conditions that must be met for the feature to be considered complete and acceptable by stakeholders. These criteria are used to validate that the feature works as expected and meets the defined requirements.

#### Example

* Users can successfully search for a book and receive accurate results within 2 seconds.
* A user can place a reservation on an available book, and the book status is updated to "reserved" in real-time.
* Users receive an email or SMS notification confirming their reservation within 1 minute of placing the reservation.
* The system prevents users from reserving a book that is already reserved or checked out by another user.
* The reservation feature functions correctly on the latest versions of major web browsers (Chrome, Firefox, Safari, Edge) and mobile devices.



