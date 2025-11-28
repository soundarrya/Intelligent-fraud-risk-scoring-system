\-------------------------------------------

USER STORIES (Agile - Jira Ready)

Project: Intelligent Fraud Detection & Risk Scoring System

\-------------------------------------------

**1\. Transaction Evaluation User Stories:**

**US-01: Real-Time Transaction Evaluation**

**As a** Customer,  
**I want** my transaction to be evaluated in real time,  
**so that** fraud can be detected before money leaves my account.

**Acceptance Criteria (Gherkin):**

- Given a customer initiates a transaction
- When the transaction is sent to the system
- Then the system must evaluate it in under 1 second

**US-02: Transaction Data Collection**

**As a** Fraud Analyst,  
**I want** the system to capture all relevant data,  
**so that** risk scoring is accurate.

**Acceptance Criteria (Gherkin):**

- Given a new transaction is received
- When the system processes it
- Then device ID, IP, GPS/ATM location, amount, and time must be captured

**2\. Risk Scoring Engine User Stories:**

**US-03: Apply Risk Rules**

**As a** System,  
**I want** to apply fraud rules to each transaction,  
**so that** risk score is calculated correctly.

**Acceptance Criteria (Gherkin):**

- Given a transaction is processed
- When any fraud rule matches
- Then the corresponding risk score must be added

**US-04: Calculate Final Risk Score**

**As a** System,  
**I want** to compute a total risk value (0-100),  
**so that** I can classify the risk level.

**Acceptance Criteria (Gherkin):**

- Given all applicable rules are matched
- When the rule engine executes
- Then the final score must be between 0 and 100

**3\. Authentication (OTP / Face ID):**

**US-05: OTP Requirement for High Risk**

**As a** Customer,  
**I want** OTP verification for high-risk transactions,  
**so that** unauthorized users cannot complete the transaction.

**Acceptance Criteria (Gherkin):**

- Given risk score is between 80 and 89
- When the customer tries to proceed
- Then OTP or FaceID must be requested

**US-06: OTP Failure Should Block Transaction**

**As a** Fraud Prevention System,  
**I want** to block transaction after failed OTP attempts,  
**so that** fraud is prevented.

**Acceptance Criteria (Gherkin):**

- Given the customer receives OTP
- When the customer enters wrong OTP 3 times
- Then the transaction must be blocked

**4\. Customer Notifications:**

**US-07: Alert for Medium & High Risk**

**As a** Customer,  
**I want** to receive fraud alerts instantly,  
**so that** I know if suspicious activity happens.

**Acceptance Criteria (Gherkin):**

- Given risk score is 60 or above
- When the transaction is processed
- Then customer must receive SMS/Email/Push within 5 seconds

**US-08: Not Me Button**

**As a** Customer,  
**I want** an option to report a suspicious transaction,  
**so that** I can block my card instantly.

**Acceptance Criteria (Gherkin):**

- Given user receives alert
- When user clicks "Not Me"
- Then card must be blocked immediately
- And complaint must be created

**5\. Fraud Queue User Stories:**

**US-09: Send High-Risk Transactions to Queue**

**As a** Fraud Analyst,  
**I want** to see all blocked/high-risk transactions in a queue,  
**so that** I can review them quickly.

**Acceptance Criteria (Gherkin):**

- Given a transaction is blocked or flagged
- When the risk score >= 90
- Then it must appear in the Fraud Queue with reason code

**US-10: Detailed Transaction View**

**As a** Fraud Analyst,  
**I want** to view complete details of flagged transactions,  
**so that** I can make decisions.

**Acceptance Criteria (Gherkin):**

- Given a flagged transaction is selected
- When the analyst opens it
- Then location, device, score, and amount must be shown

**6\. Complaint Handling User Stories:**

**US-11: Auto Complaint Ticket**

**As a** System,  
**I want** to create a fraud complaint automatically,  
**so that** the fraud team can take action immediately.

**Acceptance Criteria (Gherkin):**

- Given user clicks "Not Me"
- When transaction is identified as fraud
- Then a complaint ID must be generated automatically

**7\. Dashboard User Stories:**

**US-12: Fraud Metrics Dashboard**

**As a** Fraud Analyst,  
**I want** a dashboard,  
**so that** I can track fraud patterns and counts.

**Acceptance Criteria (Gherkin):**

- Given the dashboard is opened
- When the system loads data
- Then total fraud cases, alerts, and risk distribution must be displayed

**8\. Error Handling User Stories:**

**US-13: Log All Errors:**

**As a** System,  
**I want** to log all exceptions,  
**so that** investigations can happen easily.

**Acceptance Criteria (Gherkin):**

- Given an error occurs
- When the system catches exception
- Then timestamp, transaction ID, and error message must be logged

**US-14: System Error Alert to Fraud Team:**

**As a** Fraud Analyst,  
**I want** to be notified when errors occur during risky transactions,  
**so that** I can manually verify them.

**Acceptance Criteria (Gherkin):**

- Given an error occurs during a high-risk transaction
- When the transaction fails
- Then fraud team must receive an error alert notification
