# DeliverEats – Future Enhancements (not in MVP)

> Simulated Business Analyst portfolio project (DeliverEats v1.1, MVP scope). Not a real production system.

These features were in the v1.0 BRD/FRD scope but are excluded from the MVP so that all documents, diagrams and wireframes agree on a focused first release.

| ID | Enhancement | Description | Origin in v1.0 |
|---|---|---|---|
| FE-01 | Live GPS order tracking | Map-based live location of the delivery partner (replaces status milestones). | Formerly BR-07 / FR-09 'real-time tracking' |
| FE-02 | Push notifications | Push alerts to customers, restaurants and delivery partners (MVP uses in-app messages and OTP SMS only). | Formerly BR-09 / FR-11 |
| FE-03 | Central admin dashboard | Admin UI for user management, platform monitoring, complaint handling and reports (MVP uses back-end tools run by the technical team). | Formerly BR-08 / FR-10, UC-16, UC-17 |
| FE-04 | Complaint handling and manual refunds | Customer complaints, admin review and manually issued refunds. | Formerly UC-18, UC-19 |
| FE-05 | Ratings and reviews | Customers rate restaurants and delivery. | Formerly UC-10 'Rate Delivery' |
| FE-06 | Cash on Delivery | Cash payment at the door. Excluded because RULE-02 requires successful payment before the order reaches the restaurant. | Appeared in v1.0 checkout wireframe only |

## What the MVP does instead
- Live GPS tracking: order status milestones (Placed, Accepted, Preparing, Ready for pickup, Picked up, Delivered).
- Push notifications: in-app messages plus OTP by SMS.
- Admin dashboard: back-end tools used by the technical team.
- Complaints and manual refunds: automatic payment reversal when an order is rejected or times out.
