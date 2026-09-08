# Auditing Cloud Activity Using AWS CloudTrail
# Name: THARUN DP
# Register no:212225240172
## 📌 Objective
To audit and monitor cloud activity in AWS using AWS CloudTrail by viewing and analyzing recorded AWS management events. The primary goal is to extract essential audit trail metadata including user identity, event name, event time, AWS service source, target region, read-only status, and operation outcome.

---

## 🛠️ Environment & Prerequisites
* **Cloud Platform:** Amazon Web Services (AWS)
* **AWS Region:** `eu-north-1` (Europe - Stockholm)
* **Services Monitored:** AWS CloudTrail, Amazon S3, Amazon EC2
* **Access Level:** Root / IAM Administrative Rights

---

## 📄 Part A: CloudTrail Setup & Access
1. Navigated to the **AWS Management Console** and accessed **AWS CloudTrail**.
2. Opened the **Event history** dashboard to access log records from the past 90 days of management activity across all supported services.

<img width="1907" height="1016" alt="Screenshot 2026-09-02 205901" src="https://github.com/user-attachments/assets/1f3a5cb8-ebb8-4fea-bd02-d17df057498d" />

<img width="1907" height="1016" alt="Screenshot 2026-09-02 205901" src="https://github.com/user-attachments/assets/e12c3ace-d7ba-4bfa-b505-921716649e0b" />




## 🔬 Part B & C: Detailed Event Analysis

### Event 1: S3 Storage Activity (`CreateBucket`)

<img width="1917" height="1028" alt="Screenshot 2026-09-02 210221" src="https://github.com/user-attachments/assets/684ca5ce-de86-416f-8412-612e1d3c6784" />


---

### Event 2:  AutomatedDefaultVpcCreation
<img width="1917" height="1030" alt="Screenshot 2026-09-02 210601" src="https://github.com/user-attachments/assets/a3e3f84c-c4e0-4993-ba5a-1536325d986f" />

---




## 📋 Part D: Final Security Audit Summary


<img width="900" height="458" alt="Screenshot 2026-09-02 203925" src="https://github.com/user-attachments/assets/a1dbcd2b-9257-48ba-9778-f75dc8a46caa" />

---

## 🔒 Security Audit Findings & Forensic Value
1. **Accountability (Non-repudiation):** CloudTrail logs verify that both critical infrastructure mutations (`CreateBucket` and `AutomatedDefaultVpcCreation`) were performed directly by the `root` account credentials.
2. **Operational Scope:** Isolates the geographic impact (`ap-southeast-2`) and pinpoints exact resource identifiers for targeted incident investigation.
3. **Security Principle:** Identifying frequent `root` user management actions highlights a violation of the Least Privilege Principle; future actions should be performed via specific IAM roles.

---

## ✅ Result
Cloud activity within the AWS environment was audited using **AWS CloudTrail Event History**. Management events were categorized by identity, service source, region, read/write state, and operation status to form an immutable security audit trail.
