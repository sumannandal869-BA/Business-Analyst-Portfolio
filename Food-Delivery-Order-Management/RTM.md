# Requirement Traceability Matrix (RTM)

## 1. Introduction

The Requirement Traceability Matrix (RTM) is used to ensure that each business requirement is properly connected to the corresponding user story, functional requirement, and UAT/test scenario.

This helps ensure that requirements are not missed during development and testing.

---

## 2. Purpose

The purpose of this RTM is to:

- Maintain traceability between business and functional requirements.
- Ensure all requirements are covered by user stories.
- Ensure requirements are considered during testing and UAT.
- Identify any missing or untested requirements.
- Support requirement coverage throughout the project lifecycle.

---

## 3. Traceability Matrix

| Business Requirement ID | Business Requirement | User Story ID | Functional Requirement ID | UAT/Test ID | Status |
|---|---|---|---|---|---|
| BR-01 | Customers should be able to create an account. | US-01 | FR-01 | UAT-01 | Covered |
| BR-02 | Registered customers should be able to securely log in. | US-02 | FR-02 | UAT-02 | Covered |
| BR-03 | Customers should be able to search for restaurants. | US-03 | FR-03 | UAT-03 | Covered |
| BR-04 | Customers should be able to view restaurant menus. | US-04 | FR-04 | UAT-04 | Covered |
| BR-05 | Customers should be able to manage selected food items. | US-05 | FR-05 | UAT-05 | Covered |
| BR-06 | Customers should be able to place food orders. | US-06 | FR-06 | UAT-06 | Covered |
| BR-07 | Customers should be able to make online payments. | US-07 | FR-07 | UAT-07 | Covered |
| BR-08 | Restaurants should be able to receive and process orders. | US-08 | FR-08 | UAT-08 | Covered |
| BR-09 | Customers should be able to track their orders. | US-09 | FR-09 | UAT-09 | Covered |
| BR-10 | Delivery partners should be able to deliver orders and update status. | US-10 | FR-09 | UAT-10 | Covered |
| BR-11 | Customers should be able to cancel eligible orders. | US-11 | FR-10 | UAT-11 | Covered |
| BR-12 | Customers should receive notifications about important order events. | US-12 | FR-11 | UAT-12 | Covered |

---

## 4. Requirement Coverage

| Requirement Area | Total | Covered |
|---|---:|---:|
| Business Requirements | 12 | 12 |
| User Stories | 12 | 12 |
| Functional Requirements | 11 | 11 |
| UAT/Test Scenarios | 12 | 12 |

**Overall Requirement Coverage: 100%**

---

## 5. Traceability Flow

The relationship between the project artifacts is:

```text
Business Requirement
        ↓
    User Story
        ↓
Functional Requirement
        ↓
   UAT / Test Case
        ↓
 Requirement Validation

```

6. Requirement Status

The current requirements are considered covered because each business requirement has been mapped to a corresponding user story, functional requirement, and planned UAT/test scenario.

Possible requirement statuses during an actual project may include:

Not Started
In Analysis
Approved
In Development
In Testing
UAT
Completed
Deferred
Rejected
7. Change Management

If a requirement changes during the project, the BA should:

Identify the changed requirement.
Understand the reason for the change.
Perform impact analysis.
Identify affected user stories and functional requirements.
Update the RTM.
Update related test/UAT scenarios.
Obtain required stakeholder approval.
Communicate the change to the development and QA teams.
8. Benefits of RTM

The RTM helps the project team to:

Ensure complete requirement coverage.
Reduce the possibility of missing requirements.
Track changes more effectively.
Support QA and UAT activities.
Improve communication between BA, development, QA and stakeholders.
Provide evidence that requirements have been addressed.
9. Conclusion

The RTM provides end-to-end traceability across the Food Delivery Order Management System.

It connects business needs with user stories, functional requirements, and testing activities, helping ensure that the delivered solution meets the original business requirements.
