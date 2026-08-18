# entra-id-identity-management
Microsoft Entra ID identity and access management lab for a fictional fintech company — TechPay Solutions
# Microsoft Entra ID Identity Management Lab — TechPay Solutions

## Project Overview
This project implements Microsoft Entra ID for centralized 
identity and access management for a fictional fintech company — 
TechPay Solutions S.L. It covers user and group management, 
RBAC role assignments, identity lifecycle management, and 
GDPR compliance mapping.

## What This Project Covers
- 4 user accounts created with realistic fintech roles
- 4 security groups aligned with company departments
- RBAC role assignments following least privilege principle
- Identity lifecycle management (Joiner/Mover/Leaver)
- Privileged Access Management (PAM) policy
- Quarterly access review process
- GDPR compliance mapping (Art. 25, 32, 5(1)(f))

## Users and Groups

| User | Department | Entra ID Role |
|---|---|---|
| John Smith | Security | Security Reader |
| Maria Garcia | Compliance | Global Reader |
| Carlos Lopez | Engineering | Directory Readers |
| Ana Martinez | HR | Standard User |

## Security Groups
| Group | Purpose |
|---|---|
| TechPay-Security-Team | SOC and security operations |
| TechPay-Compliance-Team | Compliance and DPO functions |
| TechPay-Engineering-Team | Software development |
| TechPay-HR-Team | Human resources management |

## GDPR Compliance
| Article | Implementation |
|---|---|
| Art. 25 — Privacy by Design | Minimum access by default |
| Art. 32 — Security measures | RBAC + MFA + audit logs |
| Art. 5(1)(f) — Integrity | Access controls protect personal data |
| Art. 30 — Records | Identity audit trail as evidence |

## Tools & Technologies
- Microsoft Entra ID (Azure Active Directory)
- RBAC (Role-Based Access Control)
- Security Groups
- Audit Logs → Microsoft Sentinel

## Architecture
See [entra-id-architecture.md](docs/entra-id-architecture.md) 
for the full architecture diagram.

## Related Projects
- [Microsoft Sentinel Lab](https://github.com/Andrea1864/siem-microsoft-sentinel)
- [Azure Key Vault Lab](https://github.com/Andrea1864/azure-key-vault-secrets-management)
- [Azure Monitor Lab](https://github.com/Andrea1864/azure-monitor-observability)
- [Microsoft Purview Lab](https://github.com/Andrea1864/microsoft-purview-data-protection)
- [TechPay GDPR ROPA](https://github.com/Andrea1864/gdpr-ropa-fintech)

## Author
Andrea Castillo — Law Graduate | Cybersecurity & GRC Specialist  

