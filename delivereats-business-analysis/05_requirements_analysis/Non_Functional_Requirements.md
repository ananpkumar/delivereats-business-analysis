# DeliverEats – Non-Functional Requirements (v1.1, MVP)

> Simulated Business Analyst portfolio project (DeliverEats v1.1, MVP scope). Not a real production system.

| NFR ID | Category | Requirement |
|---|---|---|
| NFR-01 | Performance | The system must respond to user actions within 2 seconds under normal load. |
| NFR-02 | Availability | The platform must achieve at least 99.5% availability per calendar month, excluding planned downtime (about 3.6 hours of unplanned downtime per 30-day month). |
| NFR-03 | Usability | The user interface must support intuitive navigation with a minimal learning curve for all user roles. |
| NFR-04 | Security | Sensitive data must be encrypted in transit (TLS) and at rest. Passwords must be stored as salted hashes, never in plain text. |
| NFR-05 | Maintainability | The platform must be modular so updates and fixes can be deployed with minimal disruption. |
| NFR-06 | Scalability | The system must be able to scale to a 5x increase in users with minimal performance degradation after the MVP. |
| NFR-07 | Compatibility | The app must support Android 10 and above. iOS (13+) may be considered in future releases. |
| NFR-08 | Backup & Recovery | Transactional data must be backed up every 24 hours and recoverable within 2 hours of a failure. |
| NFR-09 | Payment security | No card or UPI credentials are stored by DeliverEats; all payment data is handled by the third-party payment gateway. |

The availability target (NFR-02, 99.5% per month) is the same target used as a KPI in the BRD.
