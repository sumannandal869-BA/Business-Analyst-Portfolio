# Jira Workflow

## Project

Food Delivery Management System

## Purpose

This document demonstrates the Jira workflow followed by a Business Analyst and project team to move a User Story from requirement analysis to completion.

---

# Standard Jira Workflow

```text
Backlog
   ↓
To Do
   ↓
In Progress
   ↓
Code Review
   ↓
Testing
   ↓
UAT
   ↓
Done
```

1. Backlog
Description

The Product Backlog contains all identified requirements, improvements, changes and features that may be implemented in the product.

Business Analyst Responsibilities
Gather and analyze requirements.
Discuss requirements with stakeholders.
Create Epics and User Stories.
Define Acceptance Criteria.
Identify dependencies and assumptions.
Clarify unclear requirements.
Support prioritization with the Product Owner.
Example

Requirement:

Customer should be able to cancel an eligible food order.

The BA converts this requirement into a User Story:

As a customer, I want to cancel an eligible order so that I can stop an order I no longer require.

2. To Do
Description

The User Story is refined and ready for development.

Entry Criteria

Before moving a story to "To Do":

Requirement is understood.
User Story is clearly written.
Acceptance Criteria are defined.
Dependencies are identified.
Required designs/wireframes are available where applicable.
Story is prioritized.
Product Owner has reviewed the requirement.
BA Responsibilities

The BA ensures that the development and QA teams understand the requirement.

3. In Progress
Description

The development team has started working on the User Story.

Developer Activities
Understand the User Story.
Review Acceptance Criteria.
Ask questions if requirements are unclear.
Implement the functionality.
Perform developer-level testing.
BA Responsibilities

The BA:

Clarifies business requirements.
Answers developer questions.
Resolves requirement ambiguity.
Discusses changes with the Product Owner.
Updates requirements when necessary.
Ensures changes do not introduce unexpected scope.
4. Code Review
Description

Development is completed and the code is reviewed before moving to QA.

Activities
Developer completes implementation.
Code is submitted for review.
Technical team reviews the implementation.
Required corrections are completed.
Story is prepared for QA testing.
BA Responsibilities

The BA may verify that the implemented functionality still aligns with the User Story and Acceptance Criteria.

5. Testing
Description

The QA team validates whether the implemented functionality meets the defined requirements.

QA Activities

QA validates:

Functional requirements.
Acceptance Criteria.
Positive scenarios.
Negative scenarios.
Validation rules.
Error messages.
Integration points.
Business rules.
Example Test Scenarios
Scenario 1 – Eligible Order

Given the customer has placed an order that is eligible for cancellation,

When the customer selects "Cancel Order",

Then the system should cancel the order successfully.

Scenario 2 – Non-Eligible Order

Given the order has already been delivered,

When the customer opens the order details,

Then the "Cancel Order" option should not be available.

BA Responsibilities

The BA:

Clarifies business rules.
Supports QA with requirement questions.
Reviews defects related to business requirements.
Helps determine whether reported behavior is a defect or expected behavior.
6. UAT
Description

User Acceptance Testing validates whether the solution satisfies the business need from the user's or business stakeholder's perspective.

UAT Participants
Business Analyst
Product Owner
Business Stakeholder
QA Team
Relevant Business Users
UAT Example
Requirement

Customer should be able to cancel an eligible order.

UAT Steps
Login as a customer.
Open an eligible order.
Select "Cancel Order".
Confirm cancellation.
Verify the order status.
Verify cancellation notification.
Verify refund process where applicable.
Expected Result

The order should be cancelled successfully and the customer should receive appropriate confirmation.

7. Done
Description

A User Story is moved to "Done" when all agreed requirements and quality criteria have been satisfied.

Definition of Done

A story can be marked as Done when:

Development is completed.
Code review is completed.
Acceptance Criteria are satisfied.
QA testing is completed.
Critical/high-priority defects are resolved.
UAT is completed where applicable.
Business/Product Owner approval is received.
Required documentation is updated.
Defect Workflow

If QA identifies an issue, the defect follows a separate workflow.

Open
  ↓
Assigned
  ↓
In Progress
  ↓
Fixed
  ↓
Retest
  ↓
Closed

If the issue still exists:

Retest
   ↓
Failed
   ↓
Reopened
   ↓
In Progress
Example: Complete Jira Story Lifecycle
User Story

Title: Customer Cancels Order

User Story:

As a customer, I want to cancel an eligible order so that I can stop an order I no longer require.

Step 1 – Backlog

The requirement is identified and added to the Product Backlog.

Priority: High

Step 2 – Requirement Analysis

The BA discusses the requirement with the Product Owner and identifies:

Which order statuses can be cancelled?
Is cancellation allowed after restaurant acceptance?
Is cancellation allowed after food preparation?
Will the customer receive a refund?
How will the refund be processed?
What notification should the customer receive?
Step 3 – Acceptance Criteria
Customer can cancel an eligible order.
Customer cannot cancel an order after the defined cancellation stage.
System asks for cancellation confirmation.
Order status changes to "Cancelled".
Customer receives cancellation confirmation.
Refund is initiated where applicable.
Step 4 – Development

Developer implements the cancellation functionality based on the User Story and Acceptance Criteria.

Step 5 – QA Testing

QA tests:

Successful cancellation.
Cancellation of non-eligible order.
Multiple cancellation attempts.
Cancellation after restaurant acceptance.
Cancellation after preparation.
Refund scenario.
Notification scenario.
Step 6 – UAT

Business stakeholder validates that the cancellation process meets the business requirement.

Step 7 – Done

Once all Acceptance Criteria are satisfied and required approvals are completed, the story is moved to Done.

Business Analyst Activities Throughout the Workflow
Stage	BA Responsibility
Backlog	Requirement gathering and analysis
To Do	Story refinement and Acceptance Criteria
In Progress	Requirement clarification
Code Review	Verify business alignment
Testing	Support QA and clarify requirements
UAT	Support business validation
Done	Confirm requirement completion
Requirement Change During Development

If a stakeholder requests a change after development has started, the BA should not directly add the change without analysis.

The BA should:

Understand the requested change.
Identify the reason for the change.
Perform impact analysis.
Identify affected requirements.
Discuss effort and timeline impact with the team.
Discuss priority with the Product Owner.
Document the change.
Update the User Story/Acceptance Criteria if approved.
Create a new User Story if the change is outside the existing scope.
Example Change Request
Original Requirement

Customer can cancel an order before the restaurant starts preparing the food.

New Request

Stakeholder wants customers to cancel orders even after food preparation has started.

BA Analysis

The BA should analyze:

Business impact.
Restaurant impact.
Refund implications.
Payment gateway impact.
Customer experience.
Existing cancellation rules.
Development effort.
QA effort.
UAT impact.

After impact analysis, the Product Owner can decide whether to approve, reject or defer the change.

Jira Communication Example
Developer Question

"What should happen if the customer tries to cancel an order after preparation has started?"

BA Response

"Based on the current business rule, cancellation should not be allowed once food preparation has started. The customer should see an appropriate message explaining that the order cannot be cancelled at this stage."

QA Question

"Should the cancellation button be visible for delivered orders?"

BA Response

"No. The cancellation option should not be available once the order has been delivered."

Business Analyst Skills Demonstrated

This Jira workflow demonstrates practical knowledge of:

Requirement Analysis
User Stories
Acceptance Criteria
Agile/Scrum
Backlog Management
Jira Workflow
Requirement Clarification
Defect Management
UAT
Stakeholder Communication
Impact Analysis
Change Request Management
Cross-functional Collaboration
Portfolio Note

This Jira documentation is a practical portfolio project created to demonstrate Business Analyst skills using a simulated Food Delivery Management System.

The project demonstrates how a Business Analyst can manage requirements and collaborate with Product Owners, Developers, QA and Business Stakeholders throughout the software development lifecycle.
