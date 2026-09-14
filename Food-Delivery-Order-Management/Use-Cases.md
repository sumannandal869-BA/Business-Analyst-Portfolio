# Use Case Document

## 1. Introduction

This document describes the major use cases of the Food Delivery Order Management System.

The purpose is to define how different actors interact with the system to complete business activities such as searching for restaurants, placing orders, making payments, tracking orders, and cancelling orders.

---

## 2. Actors

| Actor | Description |
|---|---|
| Customer | Searches restaurants, selects food, places and tracks orders |
| Restaurant | Receives, accepts and prepares customer orders |
| Delivery Partner | Picks up and delivers customer orders |
| Payment Gateway | Processes online payments |
| System | Validates requests, manages orders and sends notifications |

---

## 3. Use Case Diagram

The major interactions between actors and the system are represented below:

```text
                    FOOD DELIVERY ORDER MANAGEMENT SYSTEM
                 +------------------------------------------+
                 |                                          |
 Customer ------>| Register / Login                         |
 Customer ------>| Search Restaurant                        |
 Customer ------>| View Menu                                |
 Customer ------>| Manage Cart                              |
 Customer ------>| Place Order                              |
 Customer ------>| Make Payment                             |
 Customer ------>| Track Order                              |
 Customer ------>| Cancel Order                             |
                 |                                          |
 Restaurant ---->| Accept / Reject Order                     |
 Restaurant ---->| Prepare Order                             |
 Restaurant ---->| Update Order Status                       |
                 |                                          |
 Delivery ------>| Accept Delivery                           |
 Partner         | Update Delivery Status                    |
                 |                                          |
 Payment ------->| Process Payment                            |
 Gateway         |                                          |
                 +------------------------------------------+
```

UC-01: Customer Registration

Actor: Customer

Goal: Create a new customer account.

Preconditions
- Customer is not already registered.
- Customer has a valid email or mobile number.

Main Flow
- Customer opens the application.
- Customer selects Register.
- Customer enters the required details.
- System validates the information.
- System checks whether the customer already exists.
- System creates the customer account.
- System displays a registration success message.

Alternate Flow
- If the email/mobile number already exists, the system displays an appropriate error message.
- If required information is missing, the system asks the customer to provide it.

Postcondition
- Customer account is successfully created.


UC-02: Customer Login

Actor: Customer

Goal: Access the food delivery application.

Preconditions
- Customer has a registered account.

Main Flow
- Customer enters email/mobile number.
- Customer enters password.
- System validates the credentials.
- System authenticates the customer.
- System displays the home page.

Alternate Flow
- If credentials are incorrect, the system displays an error message.
- Customer can use the password recovery option if available.

Postcondition
- Customer is successfully logged in.


UC-03: Search Restaurant

Actor: Customer

Goal: Find a suitable restaurant.

Preconditions
- Customer has opened the application.

Main Flow
- Customer enters a restaurant name or search keyword.
- System processes the search request.
- System displays matching restaurants.
- Customer selects a restaurant.

Alternate Flow
- If no matching restaurant is found, the system displays a No restaurants found message.

Postcondition
- Customer can view the selected restaurant.

UC-04: View Menu

Actor: Customer

Goal: View available food items.

Preconditions
- Customer has selected a restaurant.

Main Flow
- Customer selects a restaurant.
- System displays the restaurant menu.
- Customer views food item names and prices.
- System displays item availability.
- Customer selects required food items.

Alternate Flow
- If a food item is unavailable, the system prevents the customer from adding it to the cart.

Postcondition
- Customer can add available food items to the cart.

UC-05: Manage Cart

Actor: Customer

Goal: Review and modify selected food items.

Preconditions
- Customer has selected at least one food item.

Main Flow
- Customer opens the cart.
- System displays selected food items.
- Customer changes item quantities if required.
- Customer can remove items.
- System recalculates the total amount.
- Customer proceeds to checkout.

Alternate Flow
- If the cart is empty, the system displays an appropriate message.
- If an item becomes unavailable, the system informs the customer and asks them to remove or replace the item.

Postcondition
- Cart contains the customer's final food selection.

UC-06: Place Order

Actor: Customer

Goal: Place a food delivery order.

Preconditions
- Customer is logged in.
- Cart contains at least one item.
- Valid delivery address is available.
- Main Flow
- Customer reviews the cart items.
- Customer selects or enters a delivery address.
- System calculates the final order amount.
- Customer selects a payment method.
- Customer confirms the order.
- System sends the payment request.
- Payment is successfully processed.
- System creates the order.
- System generates a unique order ID.
- Restaurant receives the new order notification.
- Customer receives order confirmation.

Alternate Flow
- If payment fails, the order is not confirmed.
- If a selected food item becomes unavailable, the system asks the customer to modify the order.
- If the restaurant is unavailable, the customer is informed and cannot proceed with the order.

Postcondition
- Order is successfully placed and sent to the restaurant.

UC-07: Process Payment

Actors: Customer, Payment Gateway

Goal: Complete payment for the order.

Preconditions
Customer has reached the payment stage.
Order contains valid items and amount.
Main Flow
Customer selects a payment method.
System sends the payment request to the payment gateway.
Payment gateway processes the transaction.
Payment gateway returns the payment status.
System records the payment result.
System confirms the order if payment is successful.
Alternate Flow
If payment fails, the system displays a payment failure message.
Customer can retry using an available payment method.
If the payment gateway is unavailable, the system informs the customer and does not confirm the order.
Postcondition

Payment status is recorded as successful or failed.

UC-08: Accept and Prepare Order

Actor: Restaurant

Goal: Process a customer order.

Preconditions
Restaurant has received a new order.
Main Flow
Restaurant receives the order notification.
Restaurant reviews the order.
Restaurant accepts the order.
System updates the order status to Restaurant Accepted.
Restaurant prepares the food.
Restaurant updates the order status to Food Being Prepared.
Restaurant marks the order as Ready for Pickup.
Alternate Flow
Restaurant can reject the order if it cannot fulfil the order.
System notifies the customer if the restaurant rejects the order.
Postcondition

Order is ready for pickup by the delivery partner.

UC-09: Track Order

Actor: Customer

Goal: Track the current status of an order.

Preconditions
Customer has placed an order.
Order is not yet delivered or cancelled.
Main Flow
Customer opens the order history.
Customer selects an active order.
System displays the current order status.
System updates the status as the order progresses.
Customer can view the latest available status.
Order Status
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
Postcondition

Customer can view the latest available order status.

UC-10: Deliver Order

Actor: Delivery Partner

Goal: Deliver the order to the customer.

Preconditions
Order is ready for pickup.
Delivery partner is available.
Main Flow
Delivery partner receives an available delivery request.
Delivery partner accepts the delivery.
Delivery partner picks up the order from the restaurant.
System updates the status to Out for Delivery.
Delivery partner travels to the customer location.
Delivery partner delivers the order.
Delivery partner marks the order as Delivered.
System notifies the customer.
Alternate Flow
If delivery cannot be completed, the delivery partner updates the delivery status and the system follows the applicable exception process.
Postcondition

Order is successfully delivered or moved to an exception state.

UC-11: Cancel Order

Actor: Customer

Goal: Cancel an order when cancellation is permitted.

Preconditions
Customer has an active order.
Order has not reached a stage where cancellation is prohibited.
Main Flow
Customer selects the active order.
Customer selects Cancel Order.
System checks the current order status.
System determines whether cancellation is allowed.
System cancels the order.
System notifies the restaurant.
If applicable, system initiates the refund process.
Customer receives cancellation confirmation.
Alternate Flow
If cancellation is not allowed, the system displays an appropriate message.
If a refund is applicable, the refund is processed according to the payment and cancellation rules.
Postcondition

Order is cancelled successfully or the customer is informed that cancellation is not permitted.

5. Use Case Summary
Use Case ID	Use Case	Primary Actor
UC-01	Customer Registration	Customer
UC-02	Customer Login	Customer
UC-03	Search Restaurant	Customer
UC-04	View Menu	Customer
UC-05	Manage Cart	Customer
UC-06	Place Order	Customer
UC-07	Process Payment	Customer / Payment Gateway
UC-08	Accept and Prepare Order	Restaurant
UC-09	Track Order	Customer
UC-10	Deliver Order	Delivery Partner
UC-11	Cancel Order	Customer
6. Business Rules
Customer must be registered and logged in to place an order.
Only available food items can be ordered.
An order must contain at least one food item.
A valid delivery address is required.
Payment must be successfully completed before confirming an online-paid order.
Order cancellation depends on the current order status.
Refund eligibility depends on the applicable cancellation rules.
Restaurant must accept an order before preparation begins.
Delivery status must be updated as the order progresses.
7. Assumptions
Customers have access to a valid email or mobile number.
Restaurants maintain updated menu and availability information.
Payment gateway services are available.
Delivery partners are available in supported locations.
Customers provide a valid delivery address.
The system has access to required notification services.
8. Dependencies
Payment Gateway
Restaurant Management System
Delivery Partner System
Notification Service
Location/Mapping Service
Customer Database
Order Management System
9. Requirement Mapping
Use Case	Related Functional Requirement
UC-01 Customer Registration	FR-01
UC-02 Customer Login	FR-02
UC-03 Search Restaurant	FR-03
UC-04 View Menu	FR-04
UC-05 Manage Cart	FR-05
UC-06 Place Order	FR-06
UC-07 Process Payment	FR-07
UC-08 Accept and Prepare Order	FR-08
UC-09 Track Order	FR-09
UC-10 Deliver Order	FR-09
UC-11 Cancel Order	FR-10
