# User Acceptance Testing (UAT) Document

## 1. Introduction

User Acceptance Testing (UAT) is performed to verify that the Food Delivery Order Management System meets the defined business requirements and is suitable for use by the intended users.

UAT focuses on validating the system from a business and end-user perspective rather than testing the technical implementation.

---

## 2. UAT Objective

The objectives of UAT are to:

- Verify that business requirements have been implemented correctly.
- Confirm that key business processes work as expected.
- Validate the system from the customer's perspective.
- Identify business-related issues before production release.
- Obtain business stakeholder acceptance before deployment.

---

## 3. UAT Scope

### In Scope

- Customer registration
- Customer login
- Restaurant search
- Menu browsing
- Cart management
- Order placement
- Payment processing
- Order confirmation
- Order tracking
- Order delivery
- Order cancellation
- Customer notifications

### Out of Scope

- Performance testing
- Security testing
- Database testing
- Code-level testing
- Infrastructure testing

---

## 4. UAT Participants

| Role | Responsibility |
|---|---|
| Business Analyst | Coordinates UAT and clarifies requirements |
| Business/User Representative | Performs business validation |
| QA Tester | Supports test execution and defect verification |
| Developer | Fixes identified defects |
| Product Owner | Reviews business acceptance |
| Project Manager | Coordinates UAT activities and release readiness |

---

## 5. UAT Entry Criteria

UAT can begin when:

- Development is completed for the agreed scope.
- QA testing has been completed.
- Critical and high-priority defects are resolved.
- UAT environment is available.
- UAT test data is available.
- UAT scenarios are reviewed and approved.
- Required users are available for testing.

---

## 6. UAT Exit Criteria

UAT can be considered complete when:

- All planned UAT scenarios have been executed.
- Critical business issues are resolved.
- No open blocker prevents business usage.
- Accepted defects have been documented.
- Business stakeholders provide approval/sign-off.

---

# 7. UAT Test Scenarios

## UAT-01: Customer Registration

**Requirement:** BR-01 / FR-01

**Objective:** Verify that a new customer can successfully register.

### Preconditions

- Customer does not already have an account.
- Valid registration details are available.

### Test Steps

1. Open the application.
2. Select **Register**.
3. Enter valid name, email/mobile number and password.
4. Submit the registration form.

### Expected Result

- System validates the entered information.
- Customer account is created successfully.
- Registration confirmation message is displayed.

**Expected Status:** Pass

---

## UAT-02: Customer Login

**Requirement:** BR-02 / FR-02

**Objective:** Verify that a registered customer can log in.

### Preconditions

- Customer has a valid registered account.

### Test Steps

1. Open the login page.
2. Enter valid email/mobile number.
3. Enter valid password.
4. Click **Login**.

### Expected Result

Customer is successfully authenticated and redirected to the application home page.

**Expected Status:** Pass

---

## UAT-03: Restaurant Search

**Requirement:** BR-03 / FR-03

**Objective:** Verify that customers can search for restaurants.

### Test Steps

1. Log in to the application.
2. Enter a restaurant name or keyword in the search field.
3. Submit the search.

### Expected Result

System displays relevant restaurants matching the search criteria.

**Expected Status:** Pass

---

## UAT-04: View Restaurant Menu

**Requirement:** BR-04 / FR-04

**Objective:** Verify that customers can view available menu items.

### Test Steps

1. Search for a restaurant.
2. Select a restaurant.
3. Open the menu.

### Expected Result

System displays available food items with their names, prices and availability.

**Expected Status:** Pass

---

## UAT-05: Manage Cart

**Requirement:** BR-05 / FR-05

**Objective:** Verify that customers can add, update and remove items from the cart.

### Test Steps

1. Select a food item.
2. Add the item to the cart.
3. Increase the item quantity.
4. Verify the total amount.
5. Remove the item.

### Expected Result

- Food item is added successfully.
- Quantity is updated correctly.
- Total amount is recalculated.
- Item can be removed from the cart.

**Expected Status:** Pass

---

## UAT-06: Place Order

**Requirement:** BR-06 / FR-06

**Objective:** Verify that a customer can successfully place an order.

### Preconditions

- Customer is logged in.
- Cart contains at least one available item.
- Valid delivery address is available.

### Test Steps

1. Open the cart.
2. Review selected items.
3. Select delivery address.
4. Select payment method.
5. Confirm the order.
6. Complete payment.

### Expected Result

- Order is successfully created.
- Unique order ID is generated.
- Restaurant receives the order.
- Customer receives order confirmation.

**Expected Status:** Pass

---

## UAT-07: Payment Processing

**Requirement:** BR-07 / FR-07

**Objective:** Verify that online payment is processed correctly.

### Test Steps

1. Place an order.
2. Select an online payment method.
3. Complete the payment process.

### Expected Result

- Payment is successfully processed.
- Payment status is recorded.
- Order is confirmed after successful payment.

### Negative Scenario

If payment fails:

- System displays a payment failure message.
- Order is not incorrectly confirmed.
- Customer can retry the payment.

**Expected Status:** Pass

---

## UAT-08: Restaurant Order Processing

**Requirement:** BR-08 / FR-08

**Objective:** Verify that the restaurant can receive and process an order.

### Test Steps

1. Customer places an order.
2. Restaurant receives the order notification.
3. Restaurant accepts the order.
4. Restaurant starts preparing the food.
5. Restaurant marks the order as ready for pickup.

### Expected Result

Order status changes correctly as the restaurant processes the order.

**Expected Status:** Pass

---

## UAT-09: Order Tracking

**Requirement:** BR-09 / FR-09

**Objective:** Verify that customers can track their order.

### Test Steps

1. Place an order.
2. Open the active order.
3. View the current order status.
4. Monitor status updates.

### Expected Result

Customer can view the latest order status.

Example:

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
Expected Status: Pass

UAT-10: Order Delivery

Requirement: BR-10 / FR-09

Objective: Verify that a delivery partner can complete an order delivery.

Test Steps
Restaurant marks the order as ready.
Delivery partner accepts the delivery.
Delivery partner picks up the order.
Delivery partner delivers the order.
Delivery partner updates the order as delivered.
Expected Result
Order status changes to Out for Delivery.
Order status changes to Delivered after successful delivery.
Customer receives delivery confirmation.

Expected Status: Pass

UAT-11: Order Cancellation

Requirement: BR-11 / FR-10

Objective: Verify that an eligible order can be cancelled.

Test Steps
Open an active order.
Select Cancel Order.
System checks whether cancellation is allowed.
Confirm cancellation.
Expected Result
Order is cancelled if cancellation is permitted.
Customer receives cancellation confirmation.
Restaurant receives cancellation notification.
Refund process is initiated if applicable.
Negative Scenario

If cancellation is not permitted:

System does not cancel the order.
Customer receives an appropriate message explaining that cancellation is unavailable.

Expected Status: Pass

UAT-12: Order Notifications

Requirement: BR-12 / FR-11

Objective: Verify that customers receive important order notifications.

Test Steps
Place an order.
Monitor order status changes.
Check notifications after each applicable event.
Expected Result

Customer receives appropriate notifications for events such as:

Order placed
Restaurant accepted order
Food preparation started
Order ready for pickup
Order out for delivery
Order delivered
Order cancelled
Payment failed

Expected Status: Pass

8. UAT Execution Summary
UAT ID	Scenario	Expected Result	Status
UAT-01	Customer Registration	Account created successfully	Pass
UAT-02	Customer Login	Customer successfully logged in	Pass
UAT-03	Restaurant Search	Relevant restaurants displayed	Pass
UAT-04	View Menu	Available menu displayed	Pass
UAT-05	Manage Cart	Cart updated correctly	Pass
UAT-06	Place Order	Order successfully created	Pass
UAT-07	Payment Processing	Payment processed correctly	Pass
UAT-08	Restaurant Order Processing	Restaurant processes order correctly	Pass
UAT-09	Order Tracking	Latest order status displayed	Pass
UAT-10	Order Delivery	Order delivered successfully	Pass
UAT-11	Order Cancellation	Eligible order cancelled successfully	Pass
UAT-12	Notifications	Appropriate notifications received	Pass
9. Defect Handling Process

If a UAT issue is identified:

UAT Execution
      ↓
Issue Identified
      ↓
Defect Logged
      ↓
BA / QA Analysis
      ↓
Developer Fix
      ↓
QA Verification
      ↓
UAT Retesting
      ↓
Accepted / Reopened
Defect Priority
Priority	Description
Critical	Prevents the business process from continuing
High	Major business functionality is affected
Medium	Functionality is affected but workaround exists
Low	Minor issue with limited business impact
10. UAT Sign-Off

After successful completion of UAT, the authorized business stakeholder should provide approval for production deployment.

Sign-Off Details
Role	Name	Status	Date
Business Representative	TBD	Pending	TBD
Business Analyst	TBD	Pending	TBD
Product Owner	TBD	Pending	TBD

Note: This portfolio document is a sample project created for demonstrating Business Analyst skills. The sign-off section is therefore marked as pending.

11. Conclusion

UAT confirms that the Food Delivery Order Management System meets the defined business requirements and supports the expected business processes.

The Business Analyst coordinates with business users, QA, developers and stakeholders during UAT to clarify requirements, manage issues, support retesting and obtain business acceptance.
