# Functional Requirements Document (FRD)

## 1. Introduction

The Food Delivery Order Management System is an online platform that allows customers to search for restaurants, browse menus, place food orders, make payments, and track their orders.

This document defines the functional requirements of the system based on the business requirements and proposed process flow.

---

## 2. Purpose

The purpose of this document is to define how the system should function and describe the expected behavior of each major feature.

---

## 3. Scope

### In Scope

- Customer registration and login
- Restaurant search
- Restaurant and menu browsing
- Food item selection
- Cart management
- Order placement
- Online payment
- Order confirmation
- Order tracking
- Order cancellation
- Customer notifications

### Out of Scope

- Restaurant employee payroll management
- Restaurant inventory management
- Delivery partner salary management
- Restaurant accounting

---

## 4. Actors

| Actor | Responsibility |
|---|---|
| Customer | Search restaurants, select food, place and track orders |
| Restaurant | Accept and prepare customer orders |
| Delivery Partner | Pick up and deliver orders |
| Payment Gateway | Process online payments |
| System | Manage orders, notifications and status updates |

---

## 5. Functional Requirements

### FR-01: Customer Registration

The system shall allow new customers to create an account.

**Requirements:**
- Customer shall provide name, mobile number/email and password.
- System shall validate the provided information.
- System shall prevent registration with an already registered email/mobile number.
- System shall display a confirmation message after successful registration.

---

### FR-02: Customer Login

The system shall allow registered customers to log in.

**Requirements:**
- Customer shall enter registered email/mobile number and password.
- System shall validate login credentials.
- System shall display an error message for invalid credentials.
- Successful login shall redirect the customer to the home page.

---

### FR-03: Restaurant Search

The system shall allow customers to search for restaurants.

**Requirements:**
- Customer shall be able to search by restaurant name.
- Customer shall be able to filter restaurants by cuisine.
- Customer shall be able to view available restaurants based on location.
- System shall display a suitable message when no restaurant is found.

---

### FR-04: Restaurant and Menu Browsing

The system shall allow customers to view restaurant details and menus.

**Requirements:**
- Customer shall be able to view restaurant name and details.
- Customer shall be able to view available food items.
- Each food item shall display name, price and availability.
- Customer shall be able to select available food items.

---

### FR-05: Cart Management

The system shall allow customers to manage selected food items.

**Requirements:**
- Customer shall be able to add food items to the cart.
- Customer shall be able to increase or decrease item quantity.
- Customer shall be able to remove items from the cart.
- System shall calculate the total order amount.
- System shall display applicable taxes and delivery charges.

---

### FR-06: Place Order

The system shall allow customers to place an order.

**Requirements:**
- Customer shall select or enter a delivery address.
- Customer shall review order details before placing the order.
- System shall display food items, quantities and total amount.
- Customer shall select a payment method.
- System shall create an order after successful payment or applicable payment confirmation.

---

### FR-07: Payment Processing

The system shall process online payments through the payment gateway.

**Requirements:**
- Customer shall be able to select an available payment method.
- System shall send payment information securely to the payment gateway.
- System shall receive payment success or failure status.
- Order shall not be confirmed if payment fails.
- System shall display an appropriate payment status to the customer.

---

### FR-08: Order Confirmation

The system shall confirm successfully placed orders.

**Requirements:**
- System shall generate a unique order ID.
- Customer shall receive order confirmation.
- Order details shall include items, amount, delivery address and estimated delivery time.
- Restaurant shall receive the new order notification.

---

### FR-09: Order Tracking

The system shall allow customers to track their orders.

**Order Status:**

```text
Order Placed
     ↓
Restaurant Accepted
     ↓
Food Being Prepared
     ↓
Ready for Pickup
     ↓
Out for Delivery
     ↓
Delivered

```
---

FR-10: Order Cancellation

The system shall allow customers to cancel orders based on defined business rules.

Requirements:

- Customer shall be able to request cancellation before the order reaches a defined preparation stage.
- System shall validate whether cancellation is allowed.
- System shall display the cancellation status.
- If applicable, the system shall initiate a refund through the payment gateway.
- Restaurant shall receive a cancellation notification.

---

FR-11: Notifications

The system shall send notifications to customers regarding important order events.

Notifications may include:

- Order successfully placed
- Restaurant accepted order
- Food preparation started
- Order ready for pickup
- Order out for delivery
- Order delivered
- Order cancelled
- Payment failed

---

## 6. Business Rules

|---|---|
| A customer must be logged in to place an order |
| Only available food items can be added to the cart |
| An order must have at least one food item |
| Customer must provide a valid delivery address |
| Order confirmation depends on successful payment or an approved payment method |
| Order cancellation is subject to the restaurant's preparation status |
| Refunds shall follow the applicable cancellation and payment rules |

---

7. Validation Rules

| Field            | Validation                               |
| ---------------- | ---------------------------------------- |
| Email            | Must be in valid email format            |
| Mobile Number    | Must contain a valid number              |
| Password         | Must meet defined password criteria      |
| Quantity         | Must be greater than zero                |
| Delivery Address | Required before placing order            |
| Payment          | Must receive successful payment response |

--- 

8. Error Handling

The system shall display appropriate messages when:

- Invalid login credentials are entered.
- Restaurant is unavailable.
- Food item is unavailable.
- Payment fails.
- Delivery address is missing or invalid.
- Order cancellation is not permitted.
- Network or system error occurs.

---

9. Non-Functional Requirements

Performance
- Restaurant search results should load within an acceptable response time.
- Order status should be updated without significant delay.

Security
- Customer credentials shall be stored securely.
- Payment information shall be handled through a secure payment gateway.
- Unauthorized users shall not access another customer's order information.

Availability
- The system should be available during normal service hours with minimal downtime.

Usability
- The application should provide a simple and user-friendly ordering process.
- Customers should be able to easily view order status.

---

10. Assumptions

- Customers have access to a valid mobile number or email.
- Restaurants maintain updated menu and availability information.
- Payment gateway services are available.
- Delivery partners are available in supported locations.
- Customers provide accurate delivery addresses.

---

11. Dependencies
- Payment Gateway
- Restaurant Management System
- Delivery Partner System
- Notification Service
- Location/Mapping Service
- Customer Database

---

12. Requirement Traceability

The functional requirements are derived from the business requirements, user stories and proposed process flow documented in this project.

Functional Requirement	Related Area
- FR-01	Customer Registration
- FR-02	Customer Login
- FR-03	Restaurant Search
- FR-04	Menu Browsing
- FR-05	Cart Management
- FR-06	Order Placement
- FR-07	Payment
- FR-08	Order Confirmation
- FR-09	Order Tracking
- FR-10	Order Cancellation
- FR-11	Notifications
