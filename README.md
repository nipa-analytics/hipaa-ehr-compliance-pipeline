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
