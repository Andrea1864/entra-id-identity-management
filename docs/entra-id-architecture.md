# Microsoft Entra ID Architecture — TechPay Solutions

## Architecture Overview

TechPay Employees
│
├── John Smith (Security)
├── Maria Garcia (Compliance)
├── Carlos Lopez (Engineering)
└── Ana Martinez (HR)
│
▼
Microsoft Entra ID
(Default Directory)
│
├── Security Groups
│ ├── TechPay-Security-Team
│ ├── TechPay-Compliance-Team
│ ├── TechPay-Engineering-Team
│ └── TechPay-HR-Team
│
├── Role Assignments
│ ├── Security Reader → John Smith
│ ├── Global Reader → Maria Garcia
│ ├── Directory Readers → Carlos Lopez
│ └── Standard User → Ana Martinez
│
└── Audit Logs
│
▼
Microsoft Sentinel
(law-sentinel-techpay)
│
▼
SOC Investigation


## Identity Lifecycle

New Employee Role Change Departure
│ │ │
Create account Update groups Disable account
Add to group Review access Revoke sessions
Assign role Document change Delete after 30d
Enroll MFA Notify DPO GDPR Art.17 check


## Security Controls
| Control | Implementation |
|---|---|
| Authentication | Username + Password + MFA |
| Authorization | RBAC — least privilege |
| Audit trail | Entra ID logs → Sentinel |
| Access review | Quarterly by DPO + managers |
| Privileged access | Global Admin — IT Admin only |

## Integration with Other Projects
| Project | Integration |
|---|---|
| Microsoft Sentinel | Sign-in logs → KQL detection rules |
| Azure Key Vault | RBAC roles for secrets access |
| Azure Monitor | Activity log monitoring |
| Microsoft Purview | Identity-based DLP policies |

## GDPR Compliance
| Article | Entra ID Control |
|---|---|
| Art. 25 | Minimum access by default |
| Art. 32 | MFA + RBAC + audit logs |
| Art. 5(1)(f) | Access controls protect personal data |
| Art. 30 | Identity audit trail as evidence |
