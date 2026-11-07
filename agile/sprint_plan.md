# DeliverEats – Sprint Plan (Simulated)

> Simulated planning only. No sprint was actually executed; statuses in Jira were set to Done for portfolio purposes. Dates are planned dates.

Six two-week sprints (12 weeks) match the 3-month MVP target in BRD v1.1, Objective 1. Jira sprint names are "DE Sprint 1" to "DE Sprint 6".

## Summary

| Sprint | Planned dates | Goal | Points |
|---|---|---|---|
| Sprint 1 | 9 Nov – 20 Nov 2026 | Customers can register with OTP and log in, and restaurants and delivery partners can log in. | 11 |
| Sprint 2 | 23 Nov – 4 Dec 2026 | Customers can browse restaurant menus, build a cart and place an order with a delivery address and online payment method. | 13 |
| Sprint 3 | 7 Dec – 18 Dec 2026 | Customers can pay with Google Pay or Paytm, retry or cancel after a failed payment, and see a payment-failed message. | 13 |
| Sprint 4 | 21 Dec 2026 – 1 Jan 2027 | Restaurants can view incoming paid orders, accept or reject them within 5 minutes, and update preparation status. | 14 |
| Sprint 5 | 4 Jan – 15 Jan 2027 | Rejected or timed-out orders are refunded automatically, and delivery partners can accept, pick up and deliver orders. | 18 |
| Sprint 6 | 18 Jan – 29 Jan 2027 | Customers can track order status milestones and see an in-app message when an order is rejected. | 7 |
| **Total** | | | **76** |

## Sprint 1 – Register and log in (11 points)

| Key | Story | Epic | Priority | Points |
|---|---|---|---|---|
| DE-11 | Register with mobile number and email | Account & Access | High | 5 |
| DE-12 | Verify OTP to complete registration | Account & Access | High | 3 |
| DE-13 | Log in as customer, restaurant or delivery partner | Account & Access | High | 3 |

## Sprint 2 – Browse, cart, place order (13 points)

| Key | Story | Epic | Priority | Points |
|---|---|---|---|---|
| DE-14 | Browse restaurants and view menus | Ordering | High | 5 |
| DE-15 | Add items to cart and view or edit the cart | Ordering | High | 5 |
| DE-16 | Place order with delivery address and payment method | Ordering | High | 3 |

## Sprint 3 – Pay online and handle failure (13 points)

| Key | Story | Epic | Priority | Points |
|---|---|---|---|---|
| DE-17 | Pay online with Google Pay or Paytm | Payment & Reversal | High | 8 |
| DE-18 | Retry or cancel after failed payment | Payment & Reversal | High | 3 |
| DE-28 | See in-app message when payment fails | Order Status & Messages | Medium | 2 |

DE-28 belongs to the messages epic but is scheduled with the payment-failure flow so the failure screen is complete at the end of the sprint (see `decision_log.md`, D-04).

## Sprint 4 – Restaurant order handling (14 points)

| Key | Story | Epic | Priority | Points |
|---|---|---|---|---|
| DE-20 | Restaurant views incoming orders | Restaurant & Delivery Fulfilment | High | 3 |
| DE-21 | Restaurant accepts or rejects an order within 5 minutes | Restaurant & Delivery Fulfilment | High | 5 |
| DE-22 | Auto-reject order when the restaurant does not respond in 5 minutes | Restaurant & Delivery Fulfilment | High | 3 |
| DE-23 | Restaurant updates preparation status | Restaurant & Delivery Fulfilment | High | 3 |

## Sprint 5 – Refunds and delivery (18 points)

| Key | Story | Epic | Priority | Points |
|---|---|---|---|---|
| DE-19 | Automatically reverse payment for rejected or timed-out orders | Payment & Reversal | High | 8 |
| DE-24 | Assign ready orders to an available delivery partner | Restaurant & Delivery Fulfilment | Medium | 5 |
| DE-25 | Delivery partner accepts and picks up an order | Restaurant & Delivery Fulfilment | Medium | 3 |
| DE-26 | Delivery partner marks order as delivered | Restaurant & Delivery Fulfilment | Medium | 2 |

Payment reversal (DE-19) is built after the restaurant reject and auto-reject stories (DE-21, DE-22) because it is triggered by them.

## Sprint 6 – Order tracking and messages (7 points)

| Key | Story | Epic | Priority | Points |
|---|---|---|---|---|
| DE-27 | View order status milestones | Order Status & Messages | Medium | 5 |
| DE-29 | See in-app message when an order is rejected | Order Status & Messages | Medium | 2 |

Sprint 6 is the lightest, leaving capacity for Definition of Done checks and non-functional verification.

## Out of the sprints

Future enhancements FE-01 to FE-06 (live GPS tracking, push notifications, admin dashboard, complaints and manual refunds, ratings, Cash on Delivery) are not in any sprint. They are documented in BRD v1.1 section 5.2.
