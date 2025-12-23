# Windows 11 STIG Compliance – WN11-AU-000110
Sensitive Privilege Use – Failure Auditing (V-253328)

**Author:** Christopher Ham

---

## Overview
This repository documents the identification, remediation, and validation of **DISA STIG WN11-AU-000110 (V-253328)** on a Windows 11 system.

This STIG requires systems to audit **Sensitive Privilege Use – Failure** events to ensure attempted misuse of high-risk privileges is logged and detectable for security monitoring, incident response, and forensic analysis.

This project demonstrates a full STIG lifecycle:
- Initial validation and finding identification
- Correct remediation using DISA-approved tooling
- Post-remediation verification
- Evidence-based documentation suitable for audit review

---

## STIG Details
- **STIG ID:** WN11-AU-000110  
- **Vulnerability ID:** V-253328  
- **Severity:** CAT II (Medium)  
- **Control Family:** Auditing and Accountability  

---

## Why This Control Matters
Sensitive privileges include actions such as:
- Act as part of the operating system
- Debug programs

Failure to audit unsuccessful attempts to use these privileges reduces visibility into privilege abuse, misconfiguration, or malicious activity. Auditing failures is critical for detection and investigation.

---

## Environment
- **Operating System:** Windows 11  
- **Privileges:** Local Administrator  
- **Tools Used:** PowerShell, auditpol  

---

## Initial Validation (Finding)

Audit policy configuration was validated using:

auditpol /get /subcategory:"Sensitive Privilege Use"

---

## Result
The audit policy was successfully remediated and revalidated.

After enabling Sensitive Privilege Use failure auditing, the system returned the required configuration and now meets DISA STIG requirements.

**Final Status: NOT A FINDING**

---

## Evidence

### Initial Finding – Auditing Disabled
![Initial Finding – Auditing Disabled](auditpol-sensitive-privilege-use-finding.jpeg)This screenshot shows the system configured with **No Auditing** for Sensitive Privilege Use, resulting in a valid STIG finding.

---

### Post-Remediation Validation – Auditing Enabled
![Post-Remediation Validation](auditpol-sensitive-privilege-use-remediated.jpeg)This screenshot confirms **Sensitive Privilege Use – Failure** auditing is enabled following remediation.

---
