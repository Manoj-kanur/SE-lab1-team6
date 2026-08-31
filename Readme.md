# Mock Interview and Alumni Mentorship Platform

## Software Engineering Lab Project

A platform designed to connect students with alumni mentors for mock interviews and mentorship sessions. The system supports mentor matching, session booking, double-booking prevention, post-interview scorecard recording, and privacy-focused data handling.

---

## Team Members

| SRN | Name |
|---|---|
| PES1UG24AM181 | Nishkal M R |
| PES1UG24AM151 | M N S Abhiram |
| PES1UG24AM125 | K R Manoj |
| PES1UG24AM127 | K Ravish Rao |

---

## Project Objective

The objective of this project is to design a software platform that enables students to:

- Find and match with suitable alumni mentors.
- View available mentor time slots.
- Book mentorship or mock-interview sessions.
- Prevent double-booking of mentor time slots.
- Record post-interview scorecards.
- Handle user data with appropriate privacy and soft-deletion mechanisms.

---

## Key Functional Requirements

The project covers the following major functional requirements:

- **FR-001:** Mentor Matching
- **FR-002:** Double-Booking Prevention
- **FR-003:** Post-Interview Scorecard Recording
- **FR-004:** Privacy / Soft-Deletion
- **FR-005:** Mentorship and Mock-Interview Booking

The project also includes non-functional requirements related to reliability, scalability, and system behavior under concurrent requests.

---

## Double-Booking Prevention

A major focus of the project is preventing two students from successfully booking the same mentor time slot.

The system verifies the availability of a slot and uses an atomic locking mechanism so that when multiple students attempt to book the same slot concurrently:

1. One request acquires the slot lock.
2. The slot is verified as available.
3. The successful request creates the booking.
4. The slot is marked as booked.
5. Other concurrent requests are rejected.
6. No duplicate booking is created.

---

## UML Use-Case Model

The system includes the following primary actors:

- **Student Mentee**
- **Alumni Mentor**
- **Calendar Service**

The use-case model represents major platform operations including mentor matching, booking, availability management, scorecard recording, notifications, and data deletion.

---

## Project Deliverables

The repository contains the project documentation and individual team-member submissions, including:

- Requirements Table
- UML Use-Case Diagram
- Use-Case Flow Specification
- Individual test-case reports
- Final PDF reports

---

## Test Cases

| Test Case | Description | Owner |
|---|---|---|
| TC-01 | Mentor Matching & Booking | Owner 1 |
| TC-02 | Double-Booking Prevention | Owner 2 |
| TC-03 | Post-Interview Scorecard Recording | Owner 3 |
| TC-04 | Privacy / Soft-Deletion | Owner 4 |

---

## Repository Structure

```text
Mock-interview-and-Alumni-Mentorship-platform/
│
├── Deliverables/
│   ├── Team and individual reports
│   ├── UML/use-case resources
│   └── Supporting project documents
│
├── Test_Cases/
│   ├── TC-01-mentor-matching-booking.md
│   ├── TC-02-double-booking-prevention.md
│   ├── TC-03-scorecard-recording.md
│   └── TC-04-privacy-soft-deletion.md
│
└── README.md