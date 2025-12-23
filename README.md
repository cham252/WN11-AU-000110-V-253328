# Windows 11 STIG Compliance – WN11-AU-000110
Sensitive Privilege Use – Failure Auditing

## Overview
This repository documents the validation, remediation, and verification of **DISA STIG WN11-AU-000110 (V-253328)** on a Windows 11 system.

This STIG requires systems to audit **Sensitive Privilege Use – Failure** events to ensure attempted misuse of high-risk privileges is logged for detection and investigation.

The project demonstrates a full STIG lifecycle:
- Identification of a finding
- Correct remediation using authoritative tools
- Post-remediation validation
- Evidence-based documentation

---

## STIG Details
- STIG ID: WN11-AU-000110
- Vulnerability ID: V-253328
- Severity: CAT II (Medium)
- Control Family: Auditing and Accountability

---

## Why This Control Matters
Sensitive privileges include actions such as:
- Act as part of the operating system
- Debug programs

Failure to audit unsuccessful attempts to use these privileges reduces visibility into potential privilege abuse, misconfiguration, or malicious activity.

---

## Environment
- Operating System: Windows 11
- Privileges: Local Administrator
- Tooling: PowerShell, auditpol

---

## Validation (Initial State)

The following command was executed to validate the audit configuration:

```powershell
auditpol /get /subcategory:"Sensitive Privilege Use"
