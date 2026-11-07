# DeliverEats – Data Requirements (v1.1, MVP)

> Simulated Business Analyst portfolio project (DeliverEats v1.1, MVP scope). Not a real production system.

## Data elements
| Field | Description | Type | Validation | Mandatory |
|---|---|---|---|---|
| Full Name | Customer's full name | Text | Letters and spaces only, max 50 characters | Y |
| Email Address | Unique email address | Email | Valid email format, no duplicates | Y |
| Mobile Number | Contact number used for OTP | Numeric (10 digits) | Exactly 10 digits, numerals only | Y |
| Password | Login password (stored as salted hash) | Hashed text | Min 8 characters with at least 1 uppercase letter, 1 number and 1 symbol | Y |
| Delivery Address | Delivery location entered by customer | Text | Max 200 characters | Y |
| Order ID | Unique identifier for each order | Alphanumeric (UUID) | System-generated | Y |
| Order Total | Total amount payable (INR) | Decimal | Greater than 0, 2 decimal places | Y |
| Payment Method | Method selected for payment | Enum | Google Pay, Paytm | Y |
| Payment Status | Status of the payment transaction | Enum | Pending, Successful, Failed, Refunded | Y |
| Order Status | Current lifecycle status of the order | Enum | Pending Payment, Placed, Accepted, Preparing, Ready for Pickup, Picked Up, Delivered, Rejected, Cancelled | Y |
| Restaurant ID | Restaurant fulfilling the order | Alphanumeric | System-generated | Y |
| Menu Item ID | Unique identifier for each menu item | Alphanumeric | System-generated | Y |
| User Role | Role of the logged-in user | Enum | Customer, Restaurant, Delivery Partner | Y |

## Payment status vs order status
Payment Status: **Pending, Successful, Failed, Refunded**.

Order Status and its normal Payment Status:

| Order status | Payment status | Meaning |
|---|---|---|
| Pending Payment | Pending | Order created; awaiting payment result. Restaurant cannot see it yet. |
| Placed | Successful | Payment succeeded; order sent to the restaurant. |
| Accepted | Successful | Restaurant accepted within 5 minutes. |
| Preparing | Successful | Restaurant is preparing the food. |
| Ready for Pickup | Successful | Food is ready; delivery partner assigned. |
| Picked Up | Successful | Delivery partner has collected the order. |
| Delivered | Successful | Delivery partner marked the order delivered. |
| Rejected | Refunded | Restaurant rejected the order or 5 minutes elapsed; payment reversed automatically (FR-11). |
| Cancelled | Failed | Customer cancelled after a failed payment; no money taken. |

Key transitions:
- Pending Payment to Placed: payment succeeds (RULE-02).
- Pending Payment to Cancelled: payment fails and the customer cancels; no money taken.
- Placed to Rejected: restaurant rejects, or 5 minutes pass without a response (RULE-06); payment becomes Refunded automatically (RULE-07, FR-11).
- Placed to Accepted to Preparing to Ready for Pickup to Picked Up to Delivered.
