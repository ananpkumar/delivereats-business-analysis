# DeliverEats – Definition of Done and Definition of Ready

> Simulated Business Analyst portfolio project. These are working agreements for the simulated team.

## Definition of Ready (a story can enter a sprint when)

- It is written as "As a … I want … so that …".
- It has acceptance criteria in Given/When/Then form.
- It is traced to a BR, FR and use case through labels.
- It has a priority and a story point estimate.
- It is small enough to finish within one sprint.
- Dependencies (for example the payment gateway or OTP SMS provider) are identified.

## Definition of Done (a story is Done when)

1. All acceptance criteria are met.
2. The linked UAT scenario (for example UAT-06 for DE-18) passes.
3. Business rules named on the story (for example RULE-02) are respected.
4. Non-functional requirements below are met where they apply.
5. No open defects remain on the story.
6. The Product Owner has reviewed and accepted it.
7. Traceability labels and status in Jira are up to date.

## How the non-functional requirements apply

| NFR | Requirement | Where it is checked |
|---|---|---|
| NFR-01 | Respond to user actions within 2 seconds under normal load | Every story with a user-facing action |
| NFR-02 | At least 99.5% availability per calendar month | Release readiness, not per story |
| NFR-03 | Intuitive navigation for all user roles | UI stories, reviewed against the wireframes |
| NFR-04 | Encrypted in transit and at rest; salted password hashes | DE-11, DE-13 and any story handling sensitive data |
| NFR-05 | Modular, deployable with minimal disruption | Release readiness |
| NFR-06 | Scales to 5x users after the MVP | Release readiness |
| NFR-07 | Supports Android 10 and above | All app stories |
| NFR-08 | Daily backup; recovery within 2 hours | Release readiness |
| NFR-09 | No card or UPI credentials stored by DeliverEats | DE-16, DE-17, DE-18, DE-19 |

NFRs are kept here, not as separate stories, so each story stays focused on one user outcome.
