\-------------------------------------------

UAT TEST CASES

Project: Intelligent Fraud Detection & Risk Scoring System

\-------------------------------------------

**UAT-01: Real-Time Transaction Evaluation**

**Objective:** Ensure transactions are evaluated within 1 second.  
**Precondition:** Valid customer transaction.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Initiate a transaction | System receives request |
| 2 | System performs evaluation | Evaluation completed in < 1 sec |
| 3 | View logs | Processing time displayed |

**UAT-02: Medium Risk Alert Notification**

**Objective:** Verify alerts for score 60–79.  
**Precondition:** Simulated transaction with risk score 65.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Perform transaction | System marks it medium-risk |
| 2 | Wait for alert | SMS/Email/Push sent |
| 3 | Open alert | Shows amount, device, location |

**UAT-03: High Risk OTP Authentication:**

**Objective:** Validate OTP trigger for score 80–89.  
**Precondition:** Simulated high-risk transaction.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Trigger high-risk transaction | System holds it |
| 2 | System requests OTP | OTP generated |
| 3 | Enter correct OTP | Transaction approved |

**UAT-04: OTP Failure Blocks Transaction:**

**Objective:** Ensure 3 wrong OTPs cause blocking.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Trigger high-risk transaction | OTP requested |
| 2 | Enter wrong OTP 3 times | System blocks transaction |
| 3 | Check logs | OTP failures recorded |

**UAT-05: Very High-Risk Transaction Block:**

**Objective:** Validate automatic block for score ≥ 90.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Perform very high-risk txn | System blocks instantly |
| 2 | System sends alert | “Suspicious Transaction Blocked” |
| 3 | Fraud Queue | Transaction appears in queue |

**UAT-06: Customer Clicks ‘Not Me’:**

**Objective:** Ensure card is blocked immediately.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Open alert | “Not Me” visible |
| 2 | Click “Not Me” | Card is blocked |
| 3 | Complaint system | Auto-ticket created |

**UAT-07: Fraud Queue Verification:**

**Objective:** Ensure flagged transactions appear correctly.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Open Fraud Queue | Transaction visible |
| 2 | View details | Location, device, score shown |

**UAT-08: Dashboard Metrics Display:**

**Objective:** Verify fraud dashboard shows correct counts.

| Step | Action | Expected Result |
| --- | --- | --- |
| 1 | Load dashboard | Total alerts, blocks displayed |
| 2 | Apply filters | Data updates correctly |
