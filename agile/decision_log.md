# DeliverEats – Agile Decision Log

> Simulated Business Analyst portfolio project.

| ID | Decision | Reason | Status |
|---|---|---|---|
| D-01 | Create the agile version by re-slicing the waterfall BRD/FRD, not by writing new requirements | Keeps both versions consistent and traceable | Accepted |
| D-02 | Use 5 epics instead of 7 (one per BR) | The scope is small (8 BRs, 16 use cases). Seven epics would hold only 2–3 stories each. Epics should span more than one sprint. | Accepted |
| D-03 | Cash on Delivery is excluded from the MVP and has no story | RULE-08 and FE-06: COD conflicts with RULE-02 (payment must succeed before the restaurant sees the order). Deferred, not rejected. | Accepted |
| D-04 | DE-28 (payment-failed message) is scheduled in Sprint 3 although it belongs to the messages epic | The failure flow (DE-18) is incomplete without its message. Sprints are planned by deliverable value, not by epic. | Accepted |
| D-05 | The user story sentence is written at the top of the Description field; the Summary is a short title | Common Jira practice; Summary has a 255-character limit | Accepted |
| D-06 | NFRs are in the Definition of Done, not separate stories or an epic | Keeps stories focused on user outcomes | Accepted |
| D-07 | Sprints and statuses are simulated | No application is built; velocity and burndown must not be read as real | Accepted |
| D-08 | Future enhancements FE-01 to FE-06 are not created in Jira | They are documented in BRD v1.1 section 5.2 and excluded from the MVP | Accepted |
| D-09 | Evidence is kept as screenshots, a CSV export and dashboard PDFs | Jira has no single export that preserves the project's appearance | Accepted |
| D-10 | Four Confluence pages (Product Overview, Sprint Plan, Definition of Ready and Done, Decision Log) are linked to the Jira epics and stories | Shows documentation connected to the backlog; the PDF exports are kept in `confluence/` because Confluence is private | Accepted |
