# Jira Epics and User Stories

## Project
Food Delivery Management System

## Overview

This document demonstrates how the requirements of the Food Delivery Management System can be organized in Jira using Epics, User Stories, and Acceptance Criteria.

The user stories are written from the perspective of the end user or stakeholder and follow the standard format:

> As a [user], I want [functionality], so that [business benefit].

---

# Epic 1: User Registration & Login

## Story 1.1 – Customer Registration

**User Story**

As a customer, I want to register an account so that I can use the food delivery application.

### Acceptance Criteria

- Customer should be able to enter name, email, mobile number and password.
- System should validate mandatory fields.
- Email and mobile number should be unique.
- Password should meet defined security rules.
- Customer should receive confirmation after successful registration.
- Customer should be able to log in after registration.

---

## Story 1.2 – Customer Login

**User Story**

As a registered customer, I want to log in so that I can access my account and place orders.

### Acceptance Criteria

- Customer should enter valid email/mobile number and password.
- System should validate login credentials.
- Customer should be redirected to the home page after successful login.
- System should display an appropriate error message for invalid credentials.

---

## Story 1.3 – Forgot Password

**User Story**

As a customer, I want to reset my password so that I can regain access to my account if I forget my password.

### Acceptance Criteria

- Customer should be able to select "Forgot Password".
- System should request registered email/mobile number.
- System should send OTP or password reset instructions.
- Customer should be able to create a new password.
- Customer should be able to log in using the new password.

---

# Epic 2: Restaurant & Menu Management

## Story 2.1 – Browse Restaurants

**User Story**

As a customer, I want to view available restaurants so that I can choose where to order food from.

### Acceptance Criteria

- Customer should be able to view available restaurants.
- Restaurant name should be displayed.
- Restaurant rating should be displayed where available.
- Estimated delivery time should be displayed.
- Restaurant availability should be clearly indicated.

---

## Story 2.2 – View Restaurant Menu

**User Story**

As a customer, I want to view a restaurant's menu so that I can select food items.

### Acceptance Criteria

- Customer should be able to view menu categories.
- Food item name should be displayed.
- Food item price should be displayed.
- Food item availability should be displayed.
- Customer should be able to select available food items.

---

## Story 2.3 – Restaurant Updates Menu

**User Story**

As a restaurant manager, I want to add, update and remove menu items so that customers see the latest menu information.

### Acceptance Criteria

- Restaurant manager should be able to add new food items.
- Restaurant manager should be able to update item details.
- Restaurant manager should be able to mark an item as available/unavailable.
- Restaurant manager should be able to remove menu items.
- Updated information should be visible to customers.

---

# Epic 3: Food Search & Browsing

## Story 3.1 – Search Food

**User Story**

As a customer, I want to search for food items so that I can quickly find what I want to order.

### Acceptance Criteria

- Customer should be able to enter a food name in the search box.
- System should display matching food items.
- Search should return an appropriate message when no results are found.

---

## Story 3.2 – Filter Restaurants

**User Story**

As a customer, I want to filter restaurants so that I can find restaurants based on my preferences.

### Acceptance Criteria

Customer should be able to filter restaurants based on available options such as:

- Cuisine
- Rating
- Delivery time
- Price range
- Offers

---

# Epic 4: Cart Management

## Story 4.1 – Add Food to Cart

**User Story**

As a customer, I want to add food items to my cart so that I can place an order.

### Acceptance Criteria

- Customer should be able to add available food items to the cart.
- Selected item should appear in the cart.
- Item quantity should default to 1.
- Cart total should be updated automatically.

---

## Story 4.2 – Update Cart Quantity

**User Story**

As a customer, I want to increase or decrease item quantity so that I can order the required quantity.

### Acceptance Criteria

- Customer should be able to increase quantity.
- Customer should be able to decrease quantity.
- Item subtotal should be recalculated.
- Cart total should be updated automatically.

---

## Story 4.3 – Remove Item from Cart

**User Story**

As a customer, I want to remove an item from my cart so that I can change my order before checkout.

### Acceptance Criteria

- Customer should be able to remove an item.
- Removed item should no longer appear in the cart.
- Cart total should be recalculated.

---

# Epic 5: Order Management

## Story 5.1 – Place Order

**User Story**

As a customer, I want to place an order so that the restaurant can prepare and deliver my food.

### Acceptance Criteria

- Customer should be logged in.
- Customer should have at least one item in the cart.
- Customer should select a delivery address.
- Customer should review the order summary.
- Customer should select a payment method.
- Order should be created after successful payment.
- Customer should receive an order confirmation.

---

## Story 5.2 – View Order History

**User Story**

As a customer, I want to view my previous orders so that I can track my order history.

### Acceptance Criteria

- Customer should be able to view previous orders.
- Order date should be displayed.
- Order amount should be displayed.
- Order status should be displayed.
- Customer should be able to view order details.

---

## Story 5.3 – Cancel Order

**User Story**

As a customer, I want to cancel an eligible order so that I can stop an order I no longer require.

### Acceptance Criteria

- Customer should be able to cancel an order only when cancellation is allowed.
- System should display the cancellation option for eligible orders.
- System should update the order status after cancellation.
- Customer should receive cancellation confirmation.
- Refund should be initiated where applicable.

---

# Epic 6: Payment Management

## Story 6.1 – Make Payment

**User Story**

As a customer, I want to make an online payment so that I can complete my food order.

### Acceptance Criteria

- Customer should be able to select an available payment method.
- System should display the final payable amount.
- Payment should be processed securely.
- Successful payment should create/confirm the order.
- Failed payment should display an appropriate error message.

---

## Story 6.2 – Payment Failure

**User Story**

As a customer, I want to know when my payment fails so that I can retry the payment or choose another method.

### Acceptance Criteria

- System should display a payment failure message.
- Order should not be confirmed for an unsuccessful payment.
- Customer should be able to retry payment.
- Customer should be able to select another payment method.

---

# Epic 7: Order Tracking

## Story 7.1 – Track Order

**User Story**

As a customer, I want to track my order so that I know the current delivery status.

### Acceptance Criteria

Order status should be displayed using stages such as:

- Order Placed
- Order Accepted
- Preparing
- Picked Up
- Out for Delivery
- Delivered

The customer should see the latest available status.

---

# Epic 8: Delivery Management

## Story 8.1 – Delivery Partner Accepts Delivery

**User Story**

As a delivery partner, I want to view and accept assigned deliveries so that I can deliver customer orders.

### Acceptance Criteria

- Delivery partner should receive assigned delivery details.
- Delivery partner should be able to accept the delivery.
- Delivery status should be updated after acceptance.

---

## Story 8.2 – Update Delivery Status

**User Story**

As a delivery partner, I want to update delivery status so that the customer can track the order.

### Acceptance Criteria

Delivery partner should be able to update status such as:

- Picked Up
- Out for Delivery
- Delivered

Customer should be able to see the updated status.

---

# Epic 9: Notifications

## Story 9.1 – Order Notifications

**User Story**

As a customer, I want to receive notifications about my order so that I remain informed about its progress.

### Acceptance Criteria

Customer should receive notifications for important events such as:

- Order confirmation
- Order acceptance
- Order preparation
- Out for delivery
- Order delivered
- Order cancellation

---

# Epic 10: Admin Management

## Story 10.1 – Manage Users

**User Story**

As an administrator, I want to manage users so that I can maintain proper control over the platform.

### Acceptance Criteria

- Admin should be able to view users.
- Admin should be able to activate/deactivate users.
- Admin should be able to view relevant user information.
- Changes should be recorded in the system.

---

# Jira Backlog Example

| Issue Type | Epic | Story | Priority |
|---|---|---|---|
| Epic | User Registration & Login | Customer Account Management | High |
| Story | User Registration & Login | Customer Registration | High |
| Story | User Registration & Login | Customer Login | High |
| Story | User Registration & Login | Forgot Password | Medium |
| Epic | Restaurant & Menu | Restaurant Management | High |
| Story | Restaurant & Menu | Browse Restaurants | High |
| Story | Restaurant & Menu | View Restaurant Menu | High |
| Epic | Cart Management | Shopping Cart | High |
| Story | Cart Management | Add Food to Cart | High |
| Story | Cart Management | Update Cart Quantity | Medium |
| Epic | Order Management | Order Processing | High |
| Story | Order Management | Place Order | Highest |
| Story | Order Management | Cancel Order | High |
| Epic | Payment Management | Payment Processing | Highest |
| Story | Payment Management | Make Payment | Highest |
| Epic | Order Tracking | Order Tracking | High |
| Story | Order Tracking | Track Order | High |
| Epic | Delivery Management | Delivery Processing | High |
| Story | Delivery Management | Update Delivery Status | High |

---

# Business Analyst Contribution

For this Jira project, the Business Analyst is responsible for:

1. Understanding business requirements.
2. Identifying actors and stakeholders.
3. Creating Epics based on major business capabilities.
4. Breaking Epics into User Stories.
5. Writing clear Acceptance Criteria.
6. Prioritizing requirements.
7. Clarifying requirements with stakeholders.
8. Supporting backlog refinement.
9. Coordinating with developers and QA.
10. Supporting UAT and validating delivered functionality.

---

# Key Jira Concepts Demonstrated

This portfolio demonstrates practical understanding of:

- Jira Project
- Epic
- User Story
- Acceptance Criteria
- Priority
- Product Backlog
- Sprint Planning
- Workflow
- Definition of Done
- Agile/Scrum
- Requirement Management
- UAT
