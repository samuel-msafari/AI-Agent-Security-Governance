# AI Agent Risk Assessment Template

This folder contains the master Excel workbook used to mathematically score and evaluate third-party AI agents before onboarding. 

To review the logic instantly without downloading the spreadsheet, use the preview matrix below.

| Risk Domain | Audit Evaluation Checklist | Scoring Metric (1–5) | Minimum Passing Baseline | Compensating Control Required if Failed |
| :--- | :--- | :--- | :---: | :--- |
| **Data Retention & Training** | Does the vendor use corporate input data, prompts, or telemetry to retrain public or multi-tenant models? | 1 = Public training<br>5 = Zero retention | **4** | Contractual addendum signed by vendor legal counsel explicitly blocking model training or prompt logging. |
| **Tenant Isolation** | Is our organizational data cryptographically isolated at rest and in transit from other tenants using the platform? | 1 = Shared vector DB<br>5 = Dedicated VPC / Tenant | **5** | Platform rejection. Tenant isolation is a non-negotiable zero-trust requirement for corporate data. |
| **Identity & Auth** | Does the agent support SAML 2.0 / OIDC integration via Microsoft Entra ID with enforcement of Conditional Access and MFA? | 1 = Shared API Key<br>5 = Entra Identity Integration | **4** | Enforce API token rotation every 14 days inside Azure Key Vault; isolate agent traffic via dedicated network segment. |
| **Egress & Actions** | Does the agent possess autonomous write/delete privileges on core enterprise systems without human verification? | 1 = Fully autonomous<br>5 = Read-only / Strict HITL | **4** | Implement explicit API gateway routing blocks to intercept and pause all downstream POST/DELETE requests. |
| **Compliance Auditing** | Does the system generate structured, tamper-proof logs of all prompt inputs and model outputs to a centralized SIEM? | 1 = No logging export<br>5 = Native Sentinel / Syslog streaming | **3** | Build an interim automated web-scraper workflow or middleware API proxy to capture and stream egress requests manually. |

---
📊 **Download Asset:** [Agent-Risk-Assessment-v1.xlsx](./Agent-Risk-Assessment-v1.xlsx)
