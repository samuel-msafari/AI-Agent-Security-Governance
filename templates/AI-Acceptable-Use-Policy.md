# Corporate Policy: Acceptable Use of Generative AI & Autonomous Agents

**Document Reference:** SEC-POL-AI-2026-V1  
**Effective Date:** April 2026  
**Classification:** Internal Corporate Use Only  
**Target Audience:** All Employees, Contractors, and Third-Party Vendors  

---

## 1. Purpose & Scope
This policy defines the permissible deployment, interaction, and data-sharing boundaries for Generative Artificial Intelligence (GenAI) platforms and autonomous AI Agents within the enterprise. This policy covers all corporate-issued assets, networks, and cloud tenancies.

## 2. Classification of AI Tools

### 🟢 Class A: Sanctioned & Managed Systems
* **Definition:** Tools fully vetted by IT Operations, legally cleared for corporate data retention, and integrated behind corporate Identity Providers (IdP).
* **Examples:** Microsoft Copilot (with Enterprise Data Protection enabled), Sanctioned internal RAG instances.
* **Data Permissibility:** Authorized for Corporate Internal and Restrictive Customer Data, provided it aligns with Role-Based Access Control (RBAC).

### 🟡 Class B: Evaluated / Project-Specific Tools
* **Definition:** Specialized API integrations or specialized developer agents undergoing active Vendor Risk Assessment.
* **Data Permissibility:** Restricted to anonymized test data. No production data or customer PII may be introduced.

### 🔴 Class C: Unsanctioned / Shadow AI Tools
* **Definition:** Publicly available consumer-grade LLMs, browser extensions, or automated web agents lacking enterprise data isolation agreements.
* **Examples:** Consumer-grade web interfaces, unvetted AI coding assistants.
* **Data Permissibility:** **STRICTLY PROHIBITED** for any corporate data. Introduction of proprietary source code, legal text, or operational logs to these platforms constitutes an immediate security breach.

## 3. Mandatory Operational Guardrails

* **Human-in-the-Loop (HITL) Requirement:** No autonomous agent may execute system-level operational modifications, external data transmissions, or programmatic purchases without an explicit, cryptographically signed approval from a designated human supervisor.
* **Source Code & IP Protection:** Proprietary software code, internal system flowcharts, and architectural blueprints must never be pasted into unmanaged or consumer-tier AI systems.
* **Identity Isolation:** AI Agents acting as automated workflows must utilize unique, monitored service accounts (Service Principals) with explicit, least-privilege scoping. Sharing human user credentials with an automated agent is strictly forbidden.

## 4. Compliance & Enforcement
Violations of this policy will result in immediate termination of system access privileges and may be subject to disciplinary action up to and including termination, in accordance with local corporate governance guidelines.
