# Identity Design — TechPay Solutions

## Overview
TechPay uses Microsoft Entra ID as its Identity Provider (IdP)
for all employees. Every user has a unique identity with 
minimum necessary permissions following the principle of 
least privilege.

## User Inventory

| User | Username | Role | Department |
|---|---|---|---|
| John Smith | john.smith@techpay.onmicrosoft.com | Security Analyst | Security |
| Maria Garcia | maria.garcia@techpay.onmicrosoft.com | Compliance Officer | Compliance |
| Carlos Lopez | carlos.lopez@techpay.onmicrosoft.com | Software Engineer | Engineering |
| Ana Martinez | ana.martinez@techpay.onmicrosoft.com | HR Manager | HR |

## Security Groups

| Group | Members | Purpose |
|---|---|---|
| TechPay-Security-Team | John Smith | SOC and security operations |
| TechPay-Compliance-Team | Maria Garcia | Compliance and DPO functions |
| TechPay-Engineering-Team | Carlos Lopez | Software development |
| TechPay-HR-Team | Ana Martinez | Human resources management |

## Identity Lifecycle Management

### Joiner Process (New Employee)
HR notifies IT of new hire
↓
IT creates user account in Entra ID
↓
User added to relevant security group
↓
Minimum role assigned (least privilege)
↓
Welcome email with temporary password
↓
User sets permanent password on first login
↓
MFA enrollment within 24 hours


### Mover Process (Role Change)

Manager requests role change
↓
Old group membership removed
↓
New group membership added
↓
Access review confirms correct permissions
↓
Change documented in audit log


### Leaver Process (Employee Departure)

HR notifies IT of departure
↓
Account disabled immediately
↓
Active sessions revoked
↓
Data preserved per retention policy
↓
Account deleted after 30 days
↓
GDPR Art. 17 erasure request if applicable


## GDPR Connection
- **Art. 25** — Privacy by Design: minimum access by default
- **Art. 32** — Security: unique accounts, no shared credentials
- **Art. 5(1)(f)** — Integrity: access controls protect personal data
