# PayNest — Information Security Management System (ISMS)

> **Portfolio Note:** PayNest is a fictional financial services company created for a Governance, Risk, and Compliance (GRC) portfolio project.

## Project Overview
This repository documents a practical ISMS design for **PayNest**, covering information used to deliver credit, savings, deposit-taking, and wallet services across its Tamale office, mobile app, website, USSD channel, and field agents. It is structured around **ISO/IEC 27001** principles alongside relevant fintech data protection and operational resilience considerations.

## ISMS Scope Statement
The ISMS of PayNest applies to the protection of information used to provide credit, savings, deposit-taking, and wallet services through its Tamale office, mobile app, website, USSD, and field agents.

### Included
* **People:** All 25 staff (office and remote, in Ghana) and field agents
* **Information:** Customer personal data, accounts, wallets, transaction records, credit records, and staff records
* **Systems:** In-house software, self-hosted core systems and databases, Microsoft 365, web front ends, office and mobile devices
* **Support:** MTN internet, Starlink backup, backup generator
* **Suppliers and Dependencies:** Microsoft, MTN, Starlink, USSD provider, web host (if used), independent security tester

### Exclusions
* **Customers' own devices:** Devices PayNest does not control are excluded *(the PayNest app and the customer/transaction data it processes remain in scope)*.
* **Suppliers' internal infrastructure:** Underlying supplier infrastructure is excluded *(vendor due diligence, contractual security requirements, and third-party risk management remain in scope)*.

## Planned / Current Repository Structure
* `01-scope-and-context/` — Scope boundaries, regulatory/compliance mapping, and asset/data classification
* `02-risk-management/` — Risk methodology, risk register, and treatment plans
* `03-policies-and-soa/` — Core ISMS policies, operational procedures, and Statement of Applicability (SoA)
* `04-third-party-risk/` — Supplier tiering and dependency controls (Microsoft, MTN, Starlink, USSD, hosting, security testing)
* `05-assurance-and-evidence/` — Sample audit checklists, access reviews, incident runbooks, and failover test logs
