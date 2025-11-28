
**USE CASE DIAGRAM – DESCRIPTION**

**Intelligent Fraud Detection & Risk Scoring System**


**1\. Text Description of Use Case Diagram**

**Actors**

1.  **Customer** – Initiates transactions, receives alerts, reports fraud
2.  **Fraud Analyst** – Reviews flagged transactions
3.  **System (Risk Engine)** – Evaluates transactions, assigns risk score
4.  **SMS/Email Gateway** – Sends notifications
5.  **Authentication Service (OTP/FaceID)** – Validates user identity
6.  **Complaint System** – Stores fraud complaint tickets

**Use Cases**

**1\. Perform Transaction (Customer)**

*   Customer initiates a transaction
*   System receives and evaluates it

**2\. Evaluate Transaction (System)**

*   System collects data (amount, device, IP, GPS)
*   Applies fraud rules
*   Calculates risk score

**3\. Trigger Alert (System → SMS/Email Gateway)**

*   System sends a warning or block alert to the customer

**4\. OTP/FaceID Verification (Authentication Service)**

*   System requests OTP
*   Customer enters OTP
*   Service validates the OTP

**5\. Block Transaction (System)**

*   If risk score is 90 or above, the system blocks the transaction immediately

**6\. Report Fraud ("Not Me") – Customer**

*   Customer reports suspicious activity
*   System blocks card
*   System generates fraud complaint

**7\. Add to Fraud Queue (System → Fraud Analyst)**

*   High-risk or blocked transactions appear in the Fraud Queue

**8\. Review Transaction (Fraud Analyst)**

*   Analyst reviews details
*   Approves or rejects the transaction

**9\. Create Complaint (System → Complaint System)**

*   Auto-generated complaint with a unique complaint ID

**3\. Use Case Relationships**

| Relationship | Explanation |
| --- | --- |
| Customer → Perform Transaction | Primary interaction |
| System → Evaluate Transaction | Core fraud logic |
| System → Authentication Service | Handles OTP/FaceID verification |
| System → SMS/Email Gateway | Sends alerts and notifications |
| System → Fraud Queue | Routes high-risk transactions |
| Fraud Analyst → Review Transaction | Manual investigation workflow |
| System → Complaint System | Auto complaint creation |
