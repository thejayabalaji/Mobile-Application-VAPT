# Android Mobile Application VAPT

## Project Overview

This project documents a security assessment of a deliberately vulnerable
Android application. The assessment was performed in a controlled lab
environment to identify, validate, and document mobile application security
vulnerabilities.

The assessment follows the OWASP Mobile Top 10 methodology.

---

## Objectives

- Perform static and dynamic analysis of the Android application
- Assess authentication and authorization controls
- Identify insecure data storage and communication issues
- Test application components and attack surfaces
- Validate vulnerabilities and assess their impact
- Provide remediation recommendations

---

## Lab Environment

| Component | Details |
|---|---|
| Testing OS | Kali Linux |
| Target | Android Emulator |
| Application | Androgoat |
| Device Interaction | ADB |

### Lab Architecture

![Lab Architecture](01-Lab-Setup/architecture.png)

---

## Tools & Technologies

- Kali Linux
- MobSF
- Burp Suite
- ADB
- APKTool
- Android Emulator
- OWASP Mobile Top 10

---

## Methodology

```text
Reconnaissance
      ↓
Static Analysis
      ↓
Dynamic Analysis
      ↓
Network Testing
      ↓
Authentication & Authorization Testing
      ↓
Data Storage Testing
      ↓
Vulnerability Validation
      ↓
Risk Assessment
      ↓
Remediation
      ↓
Retesting
