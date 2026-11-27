# PayNest Incident Response and Continuity Runbook

**Document Version:** 1.0 | **Owner:** Information Security Officer | **Scope Reference:** PayNest ISMS Scope (v1.0) | **Framework Alignment:** ISO/IEC 27001 (Controls A.5.24, A.5.29, A.5.30, A.8.13, A.8.15)

## 1. Purpose and Scope
This runbook defines operational response, escalation, and continuity procedures for **PayNest** across its credit, savings, deposit-taking, and wallet services. It supports PayNest's Tamale office, mobile app, website, USSD channel, and field agents, covering all 25 staff (office and remote in Ghana) and field agents.

In line with PayNest's ISMS scope, primary servers reside at **Onix Data Centre (Accra)**, an **encrypted backup server** operates at the **Tamale office**, connectivity and power rely on **MTN internet**, **Starlink backup**, **UPS**, and a **backup generator**, and **Microsoft 365** is restricted to *non-sensitive use only*. Customers' personal devices and suppliers' internal facilities/equipment remain outside direct PayNest technical control, while PayNest's applications, data, and supplier risk oversight remain in scope.

## 2. Incident Severity and Escalation Matrix
| Severity | Trigger Examples | Primary Owners & Escalation | Target Response & Cadence |
| :--- | :--- | :--- | :--- |
| **SEV-1 (Critical)** | Suspected unauthorized access/privilege abuse on Onix core/ledger/databases; wallet/deposit/credit data integrity compromise or major outage; active USSD/API exploit or critical supplier disruption. | Information Security Officer, Head of Core Systems / Engineering Lead, Payments & Integrations Lead, Executive Management | Immediate containment and escalation; continuous status updates until stabilized. |
| **SEV-2 (High)** | Extended MTN internet or Tamale power/UPS/generator disruption; USSD session/transaction mismatch; lost/stolen field agent device with KYC/session risk; accidental Restricted data exposure in M365. | Information Security Officer, IT & Network Lead, IT Support Lead, Field Operations & QA Lead | Prompt triage and containment; updates at defined operational intervals until resolved. |
| **SEV-3 (Medium / Low)** | Isolated endpoint alert or policy/clear-desk anomaly with no confirmed breach; minor non-critical utility/connectivity hiccup absorbed by failover. | IT Support Lead or relevant Asset/Risk Owner (reported to Information Security Officer) | Standard operational handling and logging; reviewed in periodic assurance checks. |

## 3. Core Operational Runbooks

### 3.1 Core Systems, Database & Application Incident (Onix / Mobile / Web / USSD)
1. **Detect & Triage:** Validate alerts, audit/transaction logs, and USSD/API error or reconciliation anomalies across Onix-hosted services and customer channels.
2. **Contain:** Isolate affected accounts, tokens, API keys, or USSD/channel routing; coordinate with Onix Data Centre or the USSD provider where supplier action is needed.
3. **Eradicate & Recover:** Patch or roll back faulty changes, verify ledger/transaction reconciliation (including idempotency and duplicate/failed prompt checks), and restore clean state.
4. **Post-Incident Review:** Record root cause, affected assets/risks, and corrective actions; update the Risk Register and Statement of Applicability where needed.

### 3.2 Tamale Connectivity, Power & Encrypted Backup Recovery
1. **Connectivity & Power Failover:** When MTN primary internet degrades/drops or grid power fails in Tamale, verify Starlink failover cutover and UPS/generator status and fuel readiness.
2. **Encrypted Backup Restoration:** When restoring from the Tamale encrypted backup server (or validating recovery readiness), verify backup integrity, decrypt/restore into a controlled target, and confirm data completeness.
3. **Test Cadence & Logging:** Run periodic Tamale backup restore drills and MTN-to-Starlink / UPS / generator failover tests, logging test dates, outcomes, and follow-up actions.

### 3.3 Field Agent Device Loss/Theft & M365 Non-Sensitive Boundary Breach
1. **Lost/Stolen Field Device:** Immediately lock/remote-wipe the device via MDM, revoke active sessions/credentials, monitor associated agent/KYC activity, and log the incident.
2. **Restricted Data in M365:** Promptly remove or quarantine misplaced Restricted data (customer PII, credit/KYC, financial/HR records) from Microsoft 365, revoke unintended sharing links, assess exposure, and reinforce DLP/training controls.

## 4. Assurance & Evidence Maintenance
Maintain dated evidence artifacts in `05-assurance-and-evidence/`—including periodic user/privileged access review logs, Tamale backup restore test logs, MTN-to-Starlink and UPS/generator failover test logs, and incident/assurance review records—to support ongoing ISMS verification.
