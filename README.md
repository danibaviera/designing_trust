# Designing Trust
## Service Design for Risk & Fraud

### Central question
How can a digital service become safer without creating unnecessary friction for legitimate users?

---

## 1. Context
Digital financial services must balance two needs that often come into tension:

- protecting the platform against fraud;
- delivering a simple and reliable experience for legitimate users.

Additional controls can reduce risk, but they can also increase friction, trigger false positives, and create more operational burden. This project examines the service not only from the interface perspective, but as an ecosystem made up of users, channels, operations, decision rules, data, and systems.

---

## 2. Challenge
Conceptual scenario:

A fintech observes a rise in friction during a critical journey. Legitimate users are increasingly pushed into additional verification or have transactions blocked by fraud prevention mechanisms.

This scenario impacts:

- Users: frustration, insecurity, abandonment;
- Business: lower conversion and approval rates;
- Operations: more contacts and manual reviews;
- Risk: the need to maintain appropriate protection levels.

The central issue is the relationship between:

Fraud Prevention × Customer Experience × Operational Efficiency

---

## 3. Research and foundations
### Key concepts
The project considers themes such as:

- common types of fraud;
- identity fraud;
- account takeover;
- onboarding fraud;
- false positives;
- KYC;
- authentication;
- biometrics;
- recovery mechanisms;
- communication best practices;
- friction impact;
- fraud prevention versus conversion.

The investigation is based on the idea that security should not be seen only as a technical layer, but as part of the service experience.

---

## 4. Personas and actors
The main actors and relevant behaviors for the service are:

### Legitimate user
Wants to complete the operation safely and with minimal friction.

### Fraudster / Malicious actor
Attempts to exploit vulnerabilities in the service to gain an unfair advantage.

### Fraud / Risk analyst
Investigates cases and decisions flagged by the platform.

### Customer support agent
Assists affected users and needs to understand what happened.

### Product / Risk team
Defines rules, policies, and service improvements.

This set of actors reinforces a multi-actor service design perspective.

---

## 5. Current journey
The journey of a legitimate user can be represented as follows:

Need
↓
Attempt
↓
Verification
↓
Risk evaluation
↓
Additional verification
↓
Blocked
↓
Confusion
↓
Support
↓
Manual review
↓
Resolution

---

## 6. Service blueprint
The service structure is organized in layers.

### User journey
Attempt
↓
Verification
↓
Blocked
↓
Understand
↓
Contest
↓
Wait
↓
Resolution

### Line of interaction
- App
- Notification
- Verification
- Support
- Status
- Result

### Frontstage
- App
- Notifications
- Verification
- Support
- Operation status
- Outcome

### Backstage / Operations
- Customer Support
- Fraud Operations
- Manual Review
- Escalation
- Decision Review

### Decision layer
- Risk signals
- Rules
- Score
- Decision engine
- Approval / Review / Block

### Data
- Account
- Transaction
- Device
- Identity
- History
- Behavior
- Risk signals

### Technical backstage
- APIs
- Identity provider
- Fraud engine
- Payment infrastructure
- CRM
- Case management
- Logs
- Databases

---

## 7. Service Failure Map
A useful way to analyze the problem is to map service failures, root causes, user impact, and operational impact.

Example:

- Legitimate user blocked → overly restrictive rule → frustration → support contact
- Generic error message → limited decision context → confusion → repeated contacts
- Support cannot explain → disconnected systems → distrust → escalation
- Manual review takes too long → fragmented process → abandonment → operational cost
- Reversal isn't propagated → integration failure → repeated block → rework

### Suggested structure
Service Failure → Root Cause → User Impact → Operational Impact

---

## 8. Design perspective
I approached fraud prevention not only as a security problem, but as a service design challenge.

A risk decision made in the technical backstage can trigger an entire customer journey, from additional verification or transaction blocking to customer support, manual analysis, and case resolution.

By connecting the customer experience to operations, decision rules, data, and systems, this project explores how Service Design can help identify where security mechanisms create unwanted friction and where the service can better support legitimate users without compromising risk controls.

The goal is not to eliminate friction completely, but to make it proportional, understandable, and reversible.

A good fraud prevention strategy should block malicious actors without designing every journey as if every customer were a threat.

---

## 9. Conclusion
The project aims to understand how security and user experience can coexist in a more balanced way. The main idea is that fraud prevention must be designed as a service, not just as a set of technical rules.

From this perspective, it is possible to reduce unnecessary friction, improve the clarity of decisions, and strengthen user trust in the service.

---

## 10. Suggested next steps
- map journeys by user segment;
- define indicators of friction and false positives;
- identify service breakpoints;
- propose communication and experience improvements;
- test hypotheses with a focus on balancing security and conversion.
