# PAYNEST-ISMS

> **Note:** PayNest is a fictional company created for a portfolio project. All test results and evidence records are simulated examples.

Information Security Management System (ISMS) documentation and governance artifacts for **PayNest** (credit, savings, deposit-taking, and wallet services), aligned with **ISO/IEC 27001**.

## Scope & Operational Boundaries
* **Channels & People:** Covers PayNest's Tamale office, mobile app, website, USSD channel, and field agents, including all 25 staff (office and remote in Ghana) and field agents.
* **Infrastructure & Data Boundaries:** Primary servers reside at **Onix Data Centre (Accra)**, an encrypted backup server operates at the **Tamale office**, connectivity and power rely on **MTN internet**, **Starlink backup**, **UPS**, and a **backup generator**, and **Microsoft 365** is restricted to *non-sensitive use only*.
* **Exclusions:** Customers' personal phones/computers and suppliers' internal facilities/equipment are excluded from direct PayNest technical control, while PayNest's applications, data, and supplier risk governance remain in scope.

## Repository Structure

| Folder | Phase / Focus | Key Artifacts |
| :--- | :--- | :--- |
| `01-context-and-scope/` | Context, Scope & Asset Inventory | Scope statement (`scope.md`) and asset/data classification register |
| `02-risk-management/` | Risk Methodology & Risk Register | Risk assessment methodology (`risk-methodology.md`) and risk register (`risk-register.csv`) |
| `03-policies-and-soa/` | Policies & Statement of Applicability | Information security policy and Statement of Applicability (`statement-of-applicability.csv`) |
| `04-third-party-risk/` | Third-Party Risk Management | TPRM policy (`tprm-policy.md`) and supplier risk & tiering register |
| `05-assurance-and-evidence/` | Incident Response, Continuity & Evidence | Incident response & continuity runbook (`incident-continuity-runbook.md`) and assurance/evidence log (`Assurance and Evidence Log.csv`) |

## Governance & Review Cadence
* **Risk Register & SoA:** Reviewed quarterly and upon major architectural, channel, supplier, or regulatory changes.
* **Policies & TPRM:** Reviewed annually (with semi-annual/engagement-level oversight for critical suppliers and independent security testers).
* **Assurance & Continuity:** Periodic backup restore drills, MTN-to-Starlink and power failover tests, access/DLP reviews, and incident post-reviews tracked in `05-assurance-and-evidence/`.
