# HIPAA EHR Compliance Pipeline

A healthcare data engineering and compliance analytics project demonstrating how Electronic Health Record information can be processed through HIPAA-aligned privacy, security, audit, access-control, and breach-detection workflows.

This project uses synthetic FHIR-style EHR data and simulates key HIPAA Technical Safeguards including:

- PHI de-identification using the HIPAA Safe Harbor method
- Role-Based Access Control
- Audit logging and tamper-evident activity tracking
- Breach detection and notification workflow
- Compliance dashboard and reporting outputs

> This project is for educational and portfolio purposes only. It does not process real patient data.

---

## Project Objective

The goal of this project is to demonstrate how healthcare organizations can build responsible data pipelines that protect electronic Protected Health Information while still supporting analytics, monitoring, and operational reporting.

The pipeline focuses on four major HIPAA Technical Safeguard areas:

| HIPAA Area | Standard |
|---|---|
| Access Controls | 45 CFR §164.312(a) |
| Audit Controls | 45 CFR §164.312(b) |
| Integrity Controls | 45 CFR §164.312(c) |
| Transmission Security | 45 CFR §164.312(e) |

The project also includes PHI de-identification using the Safe Harbor method under 45 CFR §164.514(b).

---

## Key Features

### 1. FHIR EHR Data Loading

The pipeline loads synthetic FHIR patient bundles and extracts patient-level demographic and clinical fields for compliance processing.

### 2. PHI De-identification

Implements HIPAA Safe Harbor-style de-identification by handling sensitive identifiers such as:

- Names
- Dates
- Geographic identifiers
- Phone numbers
- Email addresses
- Medical record identifiers
- Unique patient identifiers

The output is saved as:

```text
output/reports/deidentified_patients.csv


### HIPAA Safeguards Mapping

This document maps the HIPAA EHR Compliance Pipeline project components to selected HIPAA Privacy and Security Rule concepts.

This project is for educational and portfolio demonstration purposes only. It does not represent legal, compliance, or security advice.

---

## 1. Project Scope

The HIPAA EHR Compliance Pipeline demonstrates how synthetic Electronic Health Record data can be processed through privacy, access-control, audit, and breach-detection workflows.

The project focuses on simulated technical safeguards commonly associated with electronic Protected Health Information.

The pipeline includes:

* Synthetic FHIR-style EHR data loading
* PHI de-identification
* Role-Based Access Control
* Audit logging
* Breach detection
* Notification workflow simulation
* Compliance dashboard reporting

---

## 2. HIPAA Concepts Covered

| HIPAA Concept         | Project Implementation                                    |
| --------------------- | --------------------------------------------------------- |
| PHI De-identification | Safe Harbor-style removal or masking of identifiers       |
| Access Controls       | Role-Based Access Control simulation                      |
| Audit Controls        | User activity logging and audit report generation         |
| Integrity Controls    | Structured event tracking and controlled access decisions |
| Transmission Security | Conceptual placeholder for secure data movement           |
| Breach Notification   | Simulated incident detection and notification workflow    |

---

## 3. PHI De-identification Mapping

### HIPAA Reference

HIPAA Privacy Rule de-identification concepts under 45 CFR §164.514(b).

### Project Implementation

The project applies Safe Harbor-style de-identification logic to synthetic patient data.

Sensitive fields may include:

* Patient name
* Date of birth
* Address
* Phone number
* Email address
* Medical record number
* Patient identifier
* Geographic information
* Date-related identifiers

### Project Output

```text
output/reports/deidentified_patients.csv
```

### Portfolio Value

This demonstrates understanding of healthcare privacy, PHI handling, and responsible analytics preparation before downstream data use.

---

## 4. Access Controls Mapping

### HIPAA Reference

HIPAA Security Rule Technical Safeguards: Access Control
45 CFR §164.312(a)

### Project Implementation

The project simulates Role-Based Access Control for healthcare users.

Example roles may include:

* Physician
* Nurse
* Billing staff
* Data analyst
* Administrator
* External vendor

Access decisions are based on:

* User role
* Clearance level
* Resource sensitivity
* Requested action
* Session validity

### Example Access Logic

| Role            | Example Allowed Access                  |
| --------------- | --------------------------------------- |
| Physician       | View clinical patient records           |
| Nurse           | View limited clinical records           |
| Billing Staff   | View billing-related information        |
| Data Analyst    | View de-identified data only            |
| External Vendor | Restricted access                       |
| Administrator   | System-level access depending on policy |

### Project Output

```text
output/reports/rbac_access_report.csv
```

### Portfolio Value

This shows practical awareness of least-privilege access, role separation, and healthcare data governance.

---

## 5. Audit Controls Mapping

### HIPAA Reference

HIPAA Security Rule Technical Safeguards: Audit Controls
45 CFR §164.312(b)

### Project Implementation

The project generates simulated audit events for user interactions with EHR data.

Audit events may include:

* User ID
* User role
* Action performed
* Resource accessed
* Access timestamp
* Access decision
* Risk level
* Event outcome

### Project Outputs

```text
output/logs/hipaa_audit.jsonl
output/reports/audit_report.csv
```

### Portfolio Value

This demonstrates how healthcare systems can support accountability, traceability, monitoring, and investigation of access to electronic health information.

---

## 6. Integrity Controls Mapping

### HIPAA Reference

HIPAA Security Rule Technical Safeguards: Integrity
45 CFR §164.312(c)

### Project Implementation

The project supports integrity concepts by creating structured event records and access decisions.

Integrity-related practices include:

* Consistent logging format
* Structured audit records
* Controlled access decisions
* Detection of unusual or unauthorized actions
* Separation between identified and de-identified data outputs

### Project Output

```text
output/reports/audit_report.csv
```

### Portfolio Value

This shows how data pipelines can be designed to preserve trust, accountability, and consistency in healthcare data workflows.

---

## 7. Transmission Security Mapping

### HIPAA Reference

HIPAA Security Rule Technical Safeguards: Transmission Security
45 CFR §164.312(e)

### Project Implementation

This project does not implement a real encrypted transmission layer. However, it includes a conceptual placeholder for secure transmission design.

In a production system, this area would require:

* HTTPS/TLS
* Secure APIs
* SFTP where appropriate
* Encrypted data transfer
* Authentication and authorization
* Key management
* Secure cloud storage policies

### Portfolio Value

This demonstrates awareness that healthcare compliance requires security across both stored data and data in motion.

---

## 8. Breach Detection Mapping

### HIPAA Concept

HIPAA requires covered entities and business associates to identify, assess, and respond to potential breaches involving unsecured PHI.

### Project Implementation

The project simulates breach detection by identifying suspicious access patterns.

Example incident categories:

* Unauthorized PHI access
* Bulk export of patient records
* Access beyond clearance level
* External user accessing restricted clinical records
* PHI deletion attempt
* Suspicious repeated access attempts

### Project Outputs

```text
output/reports/breach_incidents.csv
output/reports/notification_workflow.csv
```

### Portfolio Value

This demonstrates applied knowledge of monitoring, incident classification, and compliance reporting workflows.

---

## 9. Compliance Dashboard Mapping

### Project Implementation

The project generates a dashboard summarizing compliance-related metrics.

Example dashboard metrics:

* Total access events
* Approved access events
* Denied access events
* Breach incidents detected
* High-risk events
* De-identification status
* Role-based access summary

### Project Output

```text
output/charts/hipaa_compliance_dashboard.png
```

### Portfolio Value

This demonstrates the ability to translate compliance activity into understandable analytics for business, security, and healthcare stakeholders.

---

## 10. Summary Mapping Table

| Project Component         | HIPAA-Relevant Area              | Output                                  |
| ------------------------- | -------------------------------- | --------------------------------------- |
| FHIR data loading         | EHR data processing              | Notebook pipeline                       |
| PHI de-identification     | Privacy Rule / De-identification | `deidentified_patients.csv`             |
| Role-Based Access Control | Access Controls                  | `rbac_access_report.csv`                |
| Audit logging             | Audit Controls                   | `hipaa_audit.jsonl`, `audit_report.csv` |
| Breach detection          | Incident monitoring              | `breach_incidents.csv`                  |
| Notification workflow     | Breach response simulation       | `notification_workflow.csv`             |
| Dashboard                 | Compliance reporting             | `hipaa_compliance_dashboard.png`        |

---

## 11. Limitations

This project is a simulation and does not provide full HIPAA compliance.

A real HIPAA-compliant system would require:

* Formal risk assessment
* Administrative safeguards
* Physical safeguards
* Technical safeguards
* Encryption
* Authentication
* Authorization
* Secure infrastructure
* Policies and procedures
* Workforce training
* Legal review
* Business Associate Agreements where required
* Incident response plans
* Continuous monitoring

---


