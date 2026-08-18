# RBAC Role Assignment — TechPay Solutions

## Overview
Role assignments in Microsoft Entra ID follow the principle 
of least privilege. Each user has only the permissions 
required for their specific job function.

## Role Assignments

| User | Role | Permissions | Justification |
|---|---|---|---|
| John Smith | Security Reader | Read security information and reports | SOC analyst needs visibility of security events |
| Maria Garcia | Global Reader | Read-only access to all admin features | Compliance Officer needs visibility without modification rights |
| Carlos Lopez | Directory Readers | Read basic directory data | Engineers need to look up users and groups |
| Ana Martinez | No admin role | Standard user only | HR manager needs no Azure admin access |

## Why These Roles?

### John Smith — Security Reader
SOC analysts need to read security alerts, logs and reports
but should never be able to modify security configurations.
Read-only access prevents accidental or malicious changes.

### Maria Garcia — Global Reader
The Compliance Officer and DPO needs visibility across all 
systems to verify compliance but must never modify settings.
Global Reader is the correct role for audit and oversight.

### Carlos Lopez — Directory Readers
Engineers need to look up user accounts and group memberships
when building applications but need no admin privileges.

### Ana Martinez — Standard User
HR managers work in HR systems, not Azure admin portals.
No admin role assigned — least privilege principle applied.

## Privileged Access Management

### Privileged Roles at TechPay
| Role | Assigned To | Justification |
|---|---|---|
| Global Administrator | IT Admin only | Full tenant control |
| Security Administrator | CISO only | Security configuration |
| User Administrator | IT Admin only | User lifecycle management |

### Privileged Access Rules
- Privileged roles reviewed monthly
- No standing privileged access — JIT (Just In Time) preferred
- All privileged actions logged to Sentinel
- MFA mandatory for all privileged roles

## Quarterly Access Review Process
| Step | Action | Responsible |
|---|---|---|
| 1 | Export all role assignments | IT Admin |
| 2 | Review with each manager | DPO + Managers |
| 3 | Remove unused access | IT Admin |
| 4 | Document changes | DPO |
| 5 | Report to CISO | Security team |

## GDPR Connection
| Article | RBAC Control |
|---|---|
| Art. 25 — Privacy by Design | Minimum access by default |
| Art. 32 — Security measures | Role-based access control |
| Art. 5(1)(f) — Integrity | Access logs in Sentinel |
| Art. 30 — Records | Role assignment audit trail |
