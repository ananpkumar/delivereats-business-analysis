# DeliverEats – Functional Requirements (v1.1, MVP)

> Simulated Business Analyst portfolio project (DeliverEats v1.1, MVP scope). Not a real production system.

Source: BRD v1.1 / FRD v1.1. Each FR traces to a business requirement (BR) and the use cases (UC) that realise it.

## Business requirements
| ID | Requirement | Priority |
|---|---|---|
| BR-01 | Customers must be able to register and log in to the DeliverEats app. Restaurants and delivery partners must be able to log in. | High |
| BR-02 | Customers must be able to browse restaurants and view digital menus. | High |
| BR-03 | Customers must be able to build a cart and place food orders through the app. | High |
| BR-04 | Customers must be able to pay securely online (Google Pay, Paytm). Payment must be returned automatically if an order is rejected or times out. | High |
| BR-05 | Restaurants must be able to receive, accept or reject incoming orders and update preparation progress. | High |
| BR-06 | Delivery partners must receive order assignments and update the delivery status. | Medium |
| BR-07 | Customers must be able to view the status of their orders in the app (status milestones). | Medium |
| BR-08 | The platform must inform users in-app of payment failures and order rejections. | Medium |

## Functional requirements
| FR ID | Description | Priority | Supports BR | Use cases |
|---|---|---|---|---|
| FR-01 | The system shall allow customers to register with mobile number and email, verified by an OTP sent through the OTP SMS gateway. | High | BR-01 | UC-01, UC-02 |
| FR-02 | The system shall allow secure login for customers, restaurants and delivery partners. | High | BR-01 | UC-03 |
| FR-03 | The system shall allow customers to browse restaurants and view their menus. | High | BR-02 | UC-04 |
| FR-04 | The system shall allow customers to add menu items to a cart and view or edit the cart. | High | BR-03 | UC-05, UC-06 |
| FR-05 | The system shall allow customers to submit an order from the cart with a delivery address and a payment method. | High | BR-03 | UC-07 |
| FR-06 | The system shall process payment through the payment gateway (Google Pay, Paytm). The order shall be sent to the restaurant only after payment succeeds. On failure the customer shall be able to retry or cancel. | High | BR-04 | UC-08, UC-09 |
| FR-07 | The system shall allow restaurants to view incoming orders, accept or reject them within 5 minutes (auto-reject on time-out) and update preparation status (Preparing, Ready for pickup). | High | BR-05 | UC-11, UC-12, UC-13 |
| FR-08 | The system shall assign accepted orders to an available delivery partner and allow the partner to accept, mark Picked up and mark Delivered. | Medium | BR-06 | UC-15, UC-16 |
| FR-09 | The system shall allow customers to view the current order status milestone (Placed, Accepted, Preparing, Ready for pickup, Picked up, Delivered). | Medium | BR-07 | UC-10 |
| FR-10 | The system shall show in-app messages to the user on payment failure and on order rejection. | Medium | BR-08, BR-07 | UC-08, UC-10 |
| FR-11 | The system shall automatically request a full payment reversal through the payment gateway when an order is rejected or times out. | High | BR-04, BR-05 | UC-12, UC-14 |

## Business rules
| Rule ID | Description |
|---|---|
| RULE-01 | Users must register with a valid mobile number and email, verified by OTP. |
| RULE-02 | Payment must be successfully processed before the order is sent to the restaurant. |
| RULE-03 | The system must immediately show an in-app message on payment failure or order rejection. |
| RULE-04 | Customers must be able to view the status milestone of their active orders in the app. |
| RULE-05 | A delivery partner must handle no more than one active delivery at a time. |
| RULE-06 | A restaurant must accept or reject an order within 5 minutes; otherwise the order is automatically rejected. |
| RULE-07 | When an order is rejected or times out, the full payment is automatically reversed to the original payment method. |
| RULE-08 | Only online payment methods (Google Pay, Paytm) are supported in the MVP. Cash on Delivery is not supported. |

## Use case narratives
| UC ID | Use case | Actors | Preconditions | Postconditions | Flow | FRs | BUC |
|---|---|---|---|---|---|---|---|
| UC-01 | Register | Customer | App installed, internet access | Account created | Enter details > request OTP > verify OTP > account created | FR-01 | BUC-01 |
| UC-02 | Verify OTP | Customer, OTP SMS Gateway | Registration started | OTP validated | System requests OTP send > user enters OTP > system validates | FR-01 | BUC-01 |
| UC-03 | Login | Customer, Restaurant, Delivery Partner | Registered account | Access granted | Enter credentials > authenticate > access granted | FR-02 | BUC-02 |
| UC-04 | Browse Restaurants and Menus | Customer | Logged in | Menu displayed | Browse list > select restaurant > view menu | FR-03 | BUC-03 |
| UC-05 | Add to Cart | Customer | Logged in, menu displayed | Items stored in cart | Select item > add to cart | FR-04 | BUC-04 |
| UC-06 | View Cart | Customer | Items in cart | Cart contents displayed | Open cart > view items, quantities, total > edit | FR-04 | BUC-04 |
| UC-07 | Place Order | Customer | Cart not empty | Order created (Pending Payment) | Review cart > enter address > choose payment method > place order | FR-05 | BUC-05 |
| UC-08 | Make Payment | Customer | Order created | Payment successful or failed | Pay via Google Pay/Paytm > await result > retry or cancel on failure | FR-06, FR-10 | BUC-06 |
| UC-09 | Process Payment | Payment Gateway | Payment requested | Payment result returned | Receive request > process > return result | FR-06 | BUC-06 |
| UC-10 | View Order Status | Customer | Order placed | Current milestone displayed | Open order > view status milestone | FR-09, FR-10 | BUC-07 |
| UC-11 | Receive Order | Restaurant | Payment successful | Order visible on dashboard | Order appears with items, customer, amount | FR-07 | BUC-08 |
| UC-12 | Accept / Reject Order | Restaurant | Order received | Order Accepted or Rejected | Open order > accept or reject (auto-reject after 5 min) | FR-07, FR-11 | BUC-08 |
| UC-13 | Update Preparation Status | Restaurant | Order accepted | Status Preparing / Ready for pickup | Select order > update status | FR-07 | BUC-08 |
| UC-14 | Reverse Payment | Payment Gateway | Order rejected or timed out | Payment status Refunded | System sends reversal request > gateway reverses > status updated | FR-11 | BUC-06, BUC-08 |
| UC-15 | Accept Delivery | Delivery Partner | Order assigned | Order picked up | View assignment > accept > confirm pickup | FR-08 | BUC-09 |
| UC-16 | Update Delivery Status | Delivery Partner | Order picked up | Status Delivered | After delivery > tap Delivered > system updates status | FR-08 | BUC-09 |
