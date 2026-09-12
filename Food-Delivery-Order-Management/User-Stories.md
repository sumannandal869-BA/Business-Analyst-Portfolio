# User Stories & Acceptance Criteria

## Epic 1: Customer Ordering

### US-01: Search for Restaurants

**User Story**

As a customer, I want to search for restaurants so that I can find a suitable restaurant for my order.

**Acceptance Criteria**

- Customer can search by restaurant name.
- Customer can search by cuisine.
- System displays matching restaurants.
- System displays an appropriate message when no restaurants are found.
- Search results should show restaurant name, cuisine and availability status.

---

### US-02: View Restaurant Menu

**User Story**

As a customer, I want to view a restaurant's menu so that I can select food items to order.

**Acceptance Criteria**

- Customer can open a restaurant's menu.
- System displays available food items.
- Each item displays its name and price.
- Unavailable items cannot be added to the cart.
- Customer can view item details where available.

---

### US-03: Add Items to Cart

**User Story**

As a customer, I want to add food items to my cart so that I can place an order.

**Acceptance Criteria**

- Customer can add an available item to the cart.
- Customer can increase or decrease item quantity.
- Customer can remove an item from the cart.
- Cart displays item name, quantity and price.
- Cart displays the total order amount.

---

### US-04: Checkout

**User Story**

As a customer, I want to review my order and provide delivery details so that I can complete my purchase.

**Acceptance Criteria**

- Customer can review selected items before payment.
- System displays the total order amount.
- Customer must provide a valid delivery address.
- Customer can proceed to payment after providing required details.
- Customer can modify the cart before placing the order.

---

### US-05: Make Payment

**User Story**

As a customer, I want to make an online payment so that I can confirm my food order.

**Acceptance Criteria**

- Customer can select an available payment method.
- System sends the payment request to the payment provider.
- Successful payment confirms the payment status.
- Failed payment displays an appropriate error message.
- Customer can retry a failed payment.
- Customer should not be charged twice for the same order.

---

### US-06: Track Order

**User Story**

As a customer, I want to track my order so that I know its current status.

**Acceptance Criteria**

- Customer can view the current order status.
- System displays relevant status updates.
- Customer can see when the restaurant accepts the order.
- Customer can see when the order is picked up.
- Customer can see when the order is delivered.

---

## Epic 2: Restaurant Order Management

### US-07: Accept or Reject Order

**User Story**

As a restaurant, I want to accept or reject incoming orders so that I can manage order processing.

**Acceptance Criteria**

- Restaurant can view new orders.
- Restaurant can accept an order.
- Restaurant can reject an order.
- Customer receives a notification when the order is accepted or rejected.
- Rejected orders follow the defined cancellation/refund process.

---

### US-08: Update Order Status

**User Story**

As a restaurant, I want to update the order status so that customers can track their order.

**Acceptance Criteria**

- Restaurant can update an accepted order to "Preparing".
- Restaurant can update the order when it is ready.
- Relevant status updates are visible to the customer.
- Customer receives notifications for important status changes.

---

## Epic 3: Order Cancellation

### US-09: Cancel Order

**User Story**

As a customer, I want to cancel my order when cancellation is allowed so that I can stop an order I no longer need.

**Acceptance Criteria**

- Customer can request cancellation for an eligible order.
- System checks the order status before allowing cancellation.
- System displays an appropriate message when cancellation is not allowed.
- Customer receives cancellation confirmation.
- Refund is initiated when applicable according to the cancellation rules.

---

## Epic 4: Reviews

### US-10: Submit Review

**User Story**

As a customer, I want to rate and review a completed order so that I can provide feedback.

**Acceptance Criteria**

- Customer can review a completed order.
- Customer can provide a rating.
- Customer can optionally provide written feedback.
- Customer cannot review an incomplete or cancelled order.
- Review is saved after successful submission.

---

# Edge Cases

The following scenarios should also be considered during requirement analysis:

- Payment fails.
- Payment succeeds but order confirmation fails.
- Customer is charged twice.
- Restaurant rejects an order after payment.
- Food item becomes unavailable after it was added to the cart.
- Customer attempts to cancel after food preparation has started.
- Delivery address is invalid or outside the service area.
- Delivery partner is unavailable.
- Network connection is interrupted during payment.
