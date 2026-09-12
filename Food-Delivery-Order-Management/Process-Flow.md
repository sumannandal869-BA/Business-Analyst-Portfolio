# Process Flow

## Customer Food Ordering Process

The following process represents the proposed TO-BE flow for placing and fulfilling a food delivery order.

```mermaid
flowchart TD
    A[Customer Login / Register] --> B[Search Restaurant]
    B --> C[View Menu]
    C --> D[Add Items to Cart]
    D --> E[Checkout]
    E --> F[Enter Delivery Address]
    F --> G[Make Payment]
    G --> H{Payment Successful?}

    H -->|No| I[Display Payment Failure]
    I --> G

    H -->|Yes| J[Order Confirmed]
    J --> K[Restaurant Receives Order]
    K --> L{Restaurant Accepts?}

    L -->|No| M[Cancel Order / Initiate Refund]
    L -->|Yes| N[Restaurant Prepares Food]

    N --> O[Order Ready]
    O --> P[Delivery Partner Picks Up]
    P --> Q[Customer Tracks Delivery]
    Q --> R[Order Delivered]
    R --> S[Customer Rates / Reviews Order]
