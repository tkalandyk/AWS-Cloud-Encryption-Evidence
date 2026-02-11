
<img width="1536" height="1024" alt="ChatGPT Image Feb 10, 2026, 09_54_19 PM" src="https://github.com/user-attachments/assets/8facd8e6-8cf1-48a7-b7a4-b90611a9e9da" />

# AWS Cloud Encryption Evidence

---

## Business Problem

Most organizations cannot instantly prove their data is encrypted at rest.

During audits, teams scramble to gather screenshots and find the right people. This process is manual, slow, and prone to human error.

This project demonstrates how encryption evidence collection can be automated, scalable, and audit-ready on demand.

---

## What This Tool Does

This Python-based tool automatically validates encryption across key AWS storage services and generates audit-ready evidence.

### Services Validated

| AWS Service | Business Meaning |
| --- | --- |
| S3 | File storage |
| EBS | Server hard drives |
| KMS | Encryption key management |

---

## Compliance Coverage

### SOC 2

- CC6.1 — Logical Access Controls  
- CC6.x — Data Protection and Security Monitoring  

### NIST 800-53

- SC-28 — Protection of Data At Rest  
- SC-12 — Cryptographic Key Establishment  

---

## Business Value

### Time Savings

Manual Evidence Collection → Hours or Days  
Automated Evidence Collection → Seconds  

### Cost Savings

Built using:

- Python  
- boto3 (Official AWS SDK)  

No additional SaaS tooling required.

### Operational Value

- Reduces manual workload  
- Improves audit readiness  
- Enables continuous compliance validation  
- Allows teams to focus on real risk instead of manual verification  

---

## Organizational Impact (Who Benefits)

### Security Teams

- Reduces manual encryption verification workload  
- Enables continuous monitoring  
- Allows focus on high-risk threats instead of configuration checks  

---

### Compliance and Audit Teams

- Provides structured, timestamped evidence  
- Eliminates screenshot-based audit evidence  
- Improves audit repeatability and consistency  

---

### Cloud and DevOps Engineering

- Provides clear remediation guidance  
- Accelerates encryption gap remediation  
- Supports future CI/CD security enforcement  

---

### Application and Product Engineering

- Helps ensure secure infrastructure is deployed from the start  
- Reduces risk of releasing non-compliant resources  

---

### Finance and Leadership

- Reduces audit preparation labor cost  
- Reduces dependency on third-party compliance tools  
- Lowers financial exposure from security incidents  

---

### IT Operations

- Reduces audit season workload spikes  
- Improves visibility into encryption posture  
- Standardizes security checks across environments  

---

## Technical Overview

This project uses **boto3**, the official AWS SDK for Python, to securely query AWS resources via API instead of manual console review.

### Core Logic

#### Discovery

- `s3.list_buckets()` → Find all storage containers  
- `ec2.describe_volumes()` → Find all server disk volumes  

#### Validation

- Checks S3 encryption configuration  
- Checks EBS encryption status  
- Validates KMS usage  

#### Evidence Generation

- JSON → Machine-readable  
- CSV → Audit and Excel-friendly  

---

## Why Build This Instead Of Only Using Native AWS Tools?

### Native AWS Options

- AWS Config  
- Security Hub  
- Trusted Advisor  

### Custom Build Benefits

- Demonstrates AWS API-level security knowledge  
- Produces custom audit evidence outputs  
- Portable across environments  
- No per-rule cost scaling  
- Strengthens automation engineering capability  

---

## Demo Output

Generates:

<img width="923" height="411" alt="image" src="https://github.com/user-attachments/assets/e3e13dbe-fb9e-4fb1-a553-0e1b2c971f07" />


- Encryption Compliance JSON Report

<img width="819" height="742" alt="image" src="https://github.com/user-attachments/assets/1243e36b-c2b4-4293-8fff-f02b4ad74b4a" />

- Encryption Compliance CSV Summary  

<img width="1398" height="148" alt="image" src="https://github.com/user-attachments/assets/7054edc4-82cd-4308-ad29-38e1fb8ad34f" />

Includes:

- Resource Name  
- Region  
- Encryption Status  
- Risk Level  
- Remediation Guidance  

---

## Current Scope

### Current

- Detection  
- Compliance Evidence Generation  

### Future Potential

- Automated Remediation  
- Multi-Region Coverage  
- ChatOps Integration  
- AI Risk Prioritization  

---

## Why This Matters

Encryption at rest is a foundational cloud security control.  
Auditors, regulators, and customers expect organizations to prove encryption is consistently enforced.

This project demonstrates:

- Automated encryption validation  
- Continuous compliance evidence generation  
- Reduced manual compliance workload  
- Improved security posture through automation  

---

## Portfolio Value

Demonstrates capability in:

- AWS Security Automation  
- GRC Engineering  
- Compliance Evidence Generation  
- Python Cloud Automation  
- Security Control Validation  
