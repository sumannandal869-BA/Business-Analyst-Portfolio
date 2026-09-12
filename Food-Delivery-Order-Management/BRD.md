# Business Requirements Document (BRD)

## 1. Document Information

| Item | Details |
|---|---|
| Project Name | Food Delivery & Order Management System |
| Document | Business Requirements Document |
| Role | Business Analyst |
| Project Type | Self-Initiated Portfolio Project |
| Methodology | Agile / Scrum |
| Status | Draft |

---

## 2. Business Problem

Customers may face difficulties when ordering food through traditional methods such as phone calls or direct restaurant visits. Restaurants may also manage orders manually, which can result in order errors, delays and limited visibility of order status.

The business needs a centralized digital platform that simplifies food ordering and provides better order management and tracking.

---

## 3. Business Objective

The objectives of the system are:

- Provide customers with a convenient digital food ordering platform.
- Allow customers to search and select restaurants.
- Allow customers to view menus and add food items to a cart.
- Enable customers to place orders and make online payments.
- Provide real-time visibility of order status.
- Help restaurants manage incoming orders efficiently.
- Reduce manual order processing and order-related errors.

---

## 4. Stakeholders

| Stakeholder | Responsibility / Interest |
|---|---|
| Customer | Search restaurants, place and track orders |
| Restaurant | Manage menu and process customer orders |
| Delivery Partner | Pick up and deliver orders |
| Admin | Manage users, restaurants and platform activities |
| Payment Service Provider | Process online payments |
| Business Analyst | Gather and document requirements |
| Developer | Develop the system |
| QA / Testing Team | Validate system functionality |

---

## 5. Scope

### 5.1 In Scope

- User registration and login
- Restaurant search
- Restaurant and menu browsing
- Cart management
- Checkout
- Online payment
- Order confirmation
- Order tracking
- Order cancellation
- Notifications
- Customer reviews and ratings

### 5.2 Out of Scope

- Grocery delivery
- Restaurant payroll management
- Restaurant accounting
- International payment processing

---

## 6. Business Requirements

### BR-01
The system shall allow customers to register and log in securely.

### BR-02
The system shall allow customers to search and browse available restaurants.

### BR-03
The system shall allow customers to view restaurant menus and item details.

### BR-04
The system shall allow customers to add, update and remove items from the cart.

### BR-05
The system shall allow customers to place an order after providing the required delivery information.

### BR-06
The system shall support online payment for orders.

### BR-07
The system shall provide customers with order confirmation and order status updates.

### BR-08
The system shall allow customers to cancel an order according to defined cancellation rules.

### BR-09
The system shall allow restaurants to receive and manage customer orders.

### BR-10
The system shall allow customers to provide ratings and reviews after order completion.

---

## 7. Business Rules

- A customer must be logged in before placing an order.
- A customer must provide a valid delivery address before checkout.
- An order can only be confirmed after successful payment.
- Restaurant acceptance is required before an order moves to food preparation.
- Cancellation and refund eligibility depends on the order status.
- Customers can submit a review only for a completed order.

---

## 8. Assumptions

- Customers have internet access.
- Restaurants maintain accurate menu and availability information.
- Delivery partners are available in supported locations.
- A third-party payment provider is available.
- Customers provide valid delivery information.

---

## 9. Constraints

- Payment processing depends on an external payment provider.
- Order tracking depends on delivery partner location data.
- System availability may depend on third-party services.
- Restaurant response time can affect overall delivery time.

---

## 10. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Payment failure | Order cannot be completed | Provide retry and payment status handling |
| Restaurant rejects order | Customer order is cancelled | Notify customer and provide refund process |
| Item becomes unavailable | Order modification may be required | Maintain real-time item availability |
| Delivery delay | Customer dissatisfaction | Provide order tracking and notifications |
| Duplicate payment | Financial/customer issue | Implement payment verification and transaction handling |

---

## 11. Success Criteria

The project will be considered successful when:

- Customers can successfully search and select restaurants.
- Customers can place orders successfully.
- Payments are processed correctly.
- Customers can track their orders.
- Restaurants can receive and manage orders.
- Customers receive appropriate notifications.
- Completed orders can be reviewed and rated.
