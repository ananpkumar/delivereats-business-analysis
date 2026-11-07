# DeliverEats – Traceability: Waterfall to Agile

> Simulated Business Analyst portfolio project. Keys and labels come from the Jira export in `exports/DeliverEats_Backlog_Export.csv`.

## 1. Story-level traceability

| Story | Title | Epic | Sprint | BR | FR | Use cases | Rules | UAT | Wireframe |
|---|---|---|---|---|---|---|---|---|---|
| DE-11 | Register with mobile number and email | DE-6 Account & Access | Sprint 1 | BR-01 | FR-01 | UC-01 | RULE-01 | UAT-01 | A1 |
| DE-12 | Verify OTP to complete registration | DE-6 Account & Access | Sprint 1 | BR-01 | FR-01 | UC-02 | RULE-01 | UAT-01 | A1 |
| DE-13 | Log in as customer, restaurant or delivery partner | DE-6 Account & Access | Sprint 1 | BR-01 | FR-02 | UC-03 | – | UAT-02 | A1 |
| DE-14 | Browse restaurants and view menus | DE-7 Ordering | Sprint 2 | BR-02 | FR-03 | UC-04 | – | UAT-03 | A2 |
| DE-15 | Add items to cart and view or edit the cart | DE-7 Ordering | Sprint 2 | BR-03 | FR-04 | UC-05, UC-06 | – | UAT-04 | A3 |
| DE-16 | Place order with delivery address and payment method | DE-7 Ordering | Sprint 2 | BR-03 | FR-05 | UC-07 | RULE-08 | UAT-05 | A3 |
| DE-17 | Pay online with Google Pay or Paytm | DE-8 Payment & Reversal | Sprint 3 | BR-04 | FR-06 | UC-08, UC-09 | RULE-02 | UAT-05 | A4 |
| DE-18 | Retry or cancel after failed payment | DE-8 Payment & Reversal | Sprint 3 | BR-04 | FR-06 | UC-08 | RULE-02 | UAT-06 | A4 |
| DE-19 | Automatically reverse payment for rejected or timed-out orders | DE-8 Payment & Reversal | Sprint 5 | BR-04 | FR-11 | UC-14 | RULE-07 | UAT-08 | A5 |
| DE-20 | Restaurant views incoming orders | DE-9 Restaurant & Delivery Fulfilment | Sprint 4 | BR-05 | FR-07 | UC-11 | – | UAT-07 | A6 |
| DE-21 | Restaurant accepts or rejects an order within 5 minutes | DE-9 Restaurant & Delivery Fulfilment | Sprint 4 | BR-05 | FR-07 | UC-12 | RULE-06 | UAT-07, UAT-08 | A6 |
| DE-22 | Auto-reject order when the restaurant does not respond in 5 minutes | DE-9 Restaurant & Delivery Fulfilment | Sprint 4 | BR-05 | FR-07 | UC-12 | RULE-06 | UAT-08 | A6 |
| DE-23 | Restaurant updates preparation status | DE-9 Restaurant & Delivery Fulfilment | Sprint 4 | BR-05 | FR-07 | UC-13 | – | UAT-07 | A6 |
| DE-24 | Assign ready orders to an available delivery partner | DE-9 Restaurant & Delivery Fulfilment | Sprint 5 | BR-06 | FR-08 | UC-15 | RULE-05 | UAT-09 | A7 |
| DE-25 | Delivery partner accepts and picks up an order | DE-9 Restaurant & Delivery Fulfilment | Sprint 5 | BR-06 | FR-08 | UC-15 | RULE-05 | UAT-09 | A7 |
| DE-26 | Delivery partner marks order as delivered | DE-9 Restaurant & Delivery Fulfilment | Sprint 5 | BR-06 | FR-08 | UC-16 | – | UAT-09 | A7 |
| DE-27 | View order status milestones | DE-10 Order Status & Messages | Sprint 6 | BR-07 | FR-09 | UC-10 | RULE-04 | UAT-10 | A5 |
| DE-28 | See in-app message when payment fails | DE-10 Order Status & Messages | Sprint 3 | BR-08 | FR-10 | UC-08 | RULE-03 | UAT-06 | A4 |
| DE-29 | See in-app message when an order is rejected | DE-10 Order Status & Messages | Sprint 6 | BR-08 | FR-10 | UC-10 | RULE-03 | UAT-08 | A5 |

## 2. Business requirement → epic → stories

| BR | Business requirement | Epic(s) | Stories |
|---|---|---|---|
| BR-01 | Register and log in | DE-6 Account & Access | DE-11, DE-12, DE-13 |
| BR-02 | Browse restaurants and menus | DE-7 Ordering | DE-14 |
| BR-03 | Cart and place orders | DE-7 Ordering | DE-15, DE-16 |
| BR-04 | Pay online; automatic payment return | DE-8 Payment & Reversal | DE-17, DE-18, DE-19 |
| BR-05 | Restaurant accepts/rejects and updates preparation | DE-9 Restaurant & Delivery Fulfilment | DE-20, DE-21, DE-22, DE-23 |
| BR-06 | Delivery assignment and status | DE-9 Restaurant & Delivery Fulfilment | DE-24, DE-25, DE-26 |
| BR-07 | Order status milestones | DE-10 Order Status & Messages | DE-27 |
| BR-08 | In-app messages for payment failure and rejection | DE-10 Order Status & Messages | DE-28, DE-29 |

## Functional requirement → stories

| ID | Stories |
|---|---|
| FR-01 | DE-11, DE-12 |
| FR-02 | DE-13 |
| FR-03 | DE-14 |
| FR-04 | DE-15 |
| FR-05 | DE-16 |
| FR-06 | DE-17, DE-18 |
| FR-07 | DE-20, DE-21, DE-22, DE-23 |
| FR-08 | DE-24, DE-25, DE-26 |
| FR-09 | DE-27 |
| FR-10 | DE-28, DE-29 |
| FR-11 | DE-19 |

## Use case → stories

| ID | Stories |
|---|---|
| UC-01 | DE-11 |
| UC-02 | DE-12 |
| UC-03 | DE-13 |
| UC-04 | DE-14 |
| UC-05 | DE-15 |
| UC-06 | DE-15 |
| UC-07 | DE-16 |
| UC-08 | DE-17, DE-18, DE-28 |
| UC-09 | DE-17 |
| UC-10 | DE-27, DE-29 |
| UC-11 | DE-20 |
| UC-12 | DE-21, DE-22 |
| UC-13 | DE-23 |
| UC-14 | DE-19 |
| UC-15 | DE-24, DE-25 |
| UC-16 | DE-26 |

## Business rule → stories

| ID | Stories |
|---|---|
| RULE-01 | DE-11, DE-12 |
| RULE-02 | DE-17, DE-18 |
| RULE-03 | DE-28, DE-29 |
| RULE-04 | DE-27 |
| RULE-05 | DE-24, DE-25 |
| RULE-06 | DE-21, DE-22 |
| RULE-07 | DE-19 |
| RULE-08 | DE-16 |

## UAT scenario → stories (acceptance criteria source)

| ID | Stories |
|---|---|
| UAT-01 | DE-11, DE-12 |
| UAT-02 | DE-13 |
| UAT-03 | DE-14 |
| UAT-04 | DE-15 |
| UAT-05 | DE-16, DE-17 |
| UAT-06 | DE-18, DE-28 |
| UAT-07 | DE-20, DE-21, DE-23 |
| UAT-08 | DE-19, DE-21, DE-22, DE-29 |
| UAT-09 | DE-24, DE-25, DE-26 |
| UAT-10 | DE-27 |

## Coverage

All 8 business requirements, 11 functional requirements, 16 use cases, 8 business rules and 10 UAT scenarios map to at least one story. NFR-01 to NFR-09 are handled in `definition_of_done.md`. Future enhancements FE-01 to FE-06 are intentionally not traced.
