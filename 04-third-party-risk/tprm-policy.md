# PayNest Third-Party Risk Management (TPRM) Policy

**Document Version:** 1.0 | **Owner:** Information Security Officer | **Scope Reference:** PayNest ISMS Scope (v1.0) | **Framework Alignment:** ISO/IEC 27001 (Controls A.5.19, A.5.20, A.5.23)

## 1. Purpose and Scope
This policy establishes how **PayNest** identifies, assesses, contracts, monitors, and manages information security and operational resilience risks arising from external suppliers and dependencies across its credit, savings, deposit-taking, and wallet services.

In accordance with the PayNest ISMS Scope Statement, PayNest's core suppliers and dependencies include **Onix Data Centre (Accra)** (primary server hosting), **Microsoft** (Microsoft 365, governed strictly under *non-sensitive use only*), **MTN** (primary internet), **Starlink** (backup internet), PayNest's **USSD provider**, and any **independent security tester**. Suppliers' internal infrastructure, equipment, and buildings are excluded from direct PayNest technical control, whereas supplier risk governance, data protection obligations, integration/connectivity boundaries, and assurance rules remain strictly in scope.

## 2. Supplier Tiering Criteria
Suppliers are assigned a risk tier based on data sensitivity (*Restricted*, *Confidential*, or *Internal*), operational criticality to core ledgers, wallets, deposits, savings, credit, or Tamale office continuity, and access/integration exposure.

| Tier | Characteristics & Exposure | Required Governance & Review Cadence |
| :--- | :--- | :--- |
| **Tier 1 (Critical)** | Hosts or processes core banking/ledger/database systems, handles customer financial/transaction/USSD flows, or underpins core availability (e.g., Onix Data Centre, USSD provider). | Enhanced due diligence, formal SLA and incident notification terms, continuity/failover alignment, and semi-annual or event-driven review. |
| **Tier 2 (High)** | Provides vital connectivity/failover links for Tamale operations, hosts collaboration services subject to strict data boundaries, or accesses sensitive security/vulnerability artifacts (e.g., MTN, Starlink, Microsoft, independent security tester). | Targeted security and boundary verification (such as M365 non-sensitive use enforcement, link failover monitoring, or pentest NDA/rules of engagement) and annual review. |
| **Tier 3 (Standard / Conditional)** | Lower-impact or conditional dependencies with bounded data exposure and clear contingency options. | Standard onboarding checks, contractual confidentiality clauses, and annual review. |

## 3. Onboarding, Contracting, and Shared Responsibility
* **Due Diligence Before Onboarding:** Verify security posture, operational reliability, and compliance alignment commensurate with tier before granting access or routing production/connectivity traffic.
* **Contractual & NDA Controls:** Require confidentiality/NDA obligations, security responsibilities, incident notification expectations, and clear scope definitions prior to service start.
* **Shared Responsibility & Data Boundaries:** Document what PayNest controls (configurations, access/MFA, data classification, M365 non-sensitive use only, Tamale encrypted backup and failover testing) versus what the supplier manages internally.

## 4. Specific Controls for Independent Security Testers
Any independent security tester engaged by PayNest must operate under strict assurance guardrails:
1. **Signed NDA & Written Rules of Engagement (RoE):** Explicitly define authorized targets, permitted testing windows, prohibited actions (such as denial-of-service or unauthorized lateral movement), and escalation contacts before testing begins.
2. **Data Minimization & Sanitization:** Avoid exposing live customer PII or real financial ledger records unless strictly authorized in an isolated test environment with appropriate safeguards.
3. **Secure Handling & Post-Test Deletion:** Transmit vulnerability reports and architecture details over encrypted channels and require verified deletion or secure return of any test data/artifacts upon engagement completion.
4. **Remediation Tracking:** Log validated findings and track remediation through PayNest's risk and vulnerability management process.

## 5. Ongoing Monitoring, Incident Escalation, and Offboarding
* **Ongoing Oversight:** Monitor service availability, failover behavior (MTN to Starlink and power/backup dependencies), security advisories, and policy adherence (including M365 non-sensitive use).
* **Incident & Disruption Escalation:** Require timely reporting of supplier security incidents or service disruptions that could affect PayNest's Confidentiality, Integrity, or Availability, and trigger PayNest's incident response and continuity runbooks.
* **Offboarding & Access Revocation:** Revoke supplier/tester accounts, API keys, VPN/console access, and shared workspace permissions promptly upon contract end or engagement closeout, and confirm data return/destruction.

## 6. Policy Review
This policy is owned by the **Information Security Officer** and reviewed **annually** or whenever a critical supplier, hosting/backup arrangement, or channel integration changes.
