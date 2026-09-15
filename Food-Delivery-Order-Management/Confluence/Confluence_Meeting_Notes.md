# Confluence Meeting Notes & MOM

## Project

Food Delivery Management System

## Meeting Title

Requirement Gathering Workshop – Order & Delivery Management

## Meeting Type

Requirement Gathering / Stakeholder Workshop

## Date

TBD

## Duration

60 Minutes

## Location

Online Meeting

---

# Meeting Objective

The purpose of this meeting was to understand and document the business requirements related to:

- Order placement
- Order cancellation
- Payment
- Restaurant order processing
- Delivery assignment
- Order tracking
- Customer notifications

The discussion focused on understanding the current business process, identifying business rules and clarifying requirements for the proposed system.

---

# Participants

| Participant | Role |
|---|---|
| Product Owner | Product & Business Decisions |
| Business Analyst | Requirement Gathering & Analysis |
| Restaurant Representative | Restaurant Operations |
| Delivery Operations Representative | Delivery Process |
| QA Representative | Testing & Validation |
| Technical Lead | Technical Feasibility |

---

# Agenda

1. Review order placement process.
2. Discuss order cancellation rules.
3. Understand payment process.
4. Discuss restaurant order acceptance.
5. Discuss delivery assignment.
6. Define order tracking statuses.
7. Identify customer notification requirements.
8. Identify open questions and dependencies.

---

# Discussion Points

## 1. Order Placement

### Discussion

The customer should be able to:

- Browse restaurants.
- Select food items.
- Add items to the cart.
- Review the order.
- Select a delivery address.
- Select a payment method.
- Place the order.

### Decision

An order should be created only after successful payment confirmation.

---

# 2. Order Cancellation

### Discussion

The team discussed whether customers should be able to cancel orders at every stage.

### Proposed Business Rule

Customers can cancel an order only before the restaurant starts preparing the food.

### Decision

Cancellation will not be allowed after food preparation has started.

### Open Question

The refund policy for cancelled orders needs confirmation from the business/payment team.

---

# 3. Payment

### Discussion

The system should support online payment.

Possible payment methods may include:

- UPI
- Credit/Debit Card
- Net Banking
- Wallet

### Decision

The order should not be confirmed if the payment transaction fails.

### Open Question

The business team needs to confirm the supported payment methods for the first release.

---

# 4. Restaurant Order Processing

### Discussion

After successful order placement, the restaurant should receive the order.

The restaurant should be able to:

- View new orders.
- Accept an order.
- Reject an order where applicable.
- Start food preparation.
- Mark the order as ready for pickup.

### Decision

Restaurant acceptance should update the customer's order status.

---

# 5. Delivery Assignment

### Discussion

Once the restaurant marks an order as ready, the delivery process should begin.

The delivery partner should receive:

- Order ID
- Restaurant information
- Pickup location
- Customer delivery location
- Relevant delivery information

### Decision

The delivery partner should update the delivery status throughout the delivery lifecycle.

---

# 6. Order Tracking

The following order statuses were discussed:

```text
Order Placed
      ↓
Order Accepted
      ↓
Preparing
      ↓
Ready for Pickup
      ↓
Picked Up
      ↓
Out for Delivery
      ↓
Delivered
```

Decision

Customers should be able to view the latest available order status.

7. Customer Notifications
Discussion

The team identified the following events where notifications may be required:

Order placed
Order accepted
Order rejected
Food preparation started
Order ready for pickup
Out for delivery
Order delivered
Order cancelled
Payment failed
Decision

Notifications should be triggered for important order lifecycle events.

Requirements Identified
Requirement ID	Requirement	Priority
REQ-01	Customer can place an order	High
REQ-02	Customer can cancel eligible orders	High
REQ-03	System processes online payment	High
REQ-04	Restaurant can accept/reject orders	High
REQ-05	Restaurant can update order preparation status	High
REQ-06	Delivery partner can update delivery status	High
REQ-07	Customer can track order	High
REQ-08	System sends order notifications	Medium
Business Rules
BR-01

An order should be created only after successful payment confirmation.

BR-02

Customer cancellation is allowed only before food preparation starts.

BR-03

Restaurant must accept an order before preparation begins.

BR-04

Only assigned delivery partners can update delivery status.

BR-05

Customer should be able to view the latest order status.

Decisions Made
Decision ID	Decision
DEC-01	Order will be confirmed after successful payment
DEC-02	Cancellation will be restricted after food preparation starts
DEC-03	Restaurant acceptance is required before preparation
DEC-04	Delivery status will be updated by the delivery partner
DEC-05	Customers will receive important order notifications
Open Questions
Question ID	Question	Owner	Status
OQ-01	What is the refund policy for cancelled orders?	Business Team	Open
OQ-02	Which payment methods are supported in Release 1?	Product Owner	Open
OQ-03	What happens if the restaurant rejects an order after payment?	Product Owner	Open
OQ-04	How will delivery partners be assigned?	Delivery Operations	Open
OQ-05	What is the maximum delivery distance?	Business Team	Open
Action Items
Action ID	Action Item	Owner	Due Date	Status
AI-01	Confirm cancellation and refund policy	Product Owner	TBD	Open
AI-02	Confirm supported payment methods	Product Owner	TBD	Open
AI-03	Define restaurant rejection process	Business Analyst	TBD	Open
AI-04	Define delivery assignment rules	Delivery Operations	TBD	Open
AI-05	Document notification requirements	Business Analyst	TBD	Open
BA Follow-Up Activities

After the meeting, the Business Analyst will:

Update the Business Requirements.
Update Functional Requirements.
Create or update User Stories.
Define Acceptance Criteria.
Update the Process Flow.
Document confirmed Business Rules.
Track Open Questions.
Follow up on Action Items.
Share updated documentation with stakeholders.
Obtain confirmation/sign-off where required.
Meeting Outcome

The meeting helped clarify the major requirements and business rules related to order and delivery management.

The identified requirements will be further analyzed and converted into detailed User Stories and Acceptance Criteria in Jira.

Open questions will be tracked until the relevant stakeholders provide confirmation.

Confluence Documentation

This meeting note demonstrates how a Business Analyst can use Confluence to maintain:

Minutes of Meeting (MOM)
Requirements
Business Rules
Decisions
Open Questions
Action Items
Follow-up Activities

This provides a centralized source of project information for business and technical stakeholders.
