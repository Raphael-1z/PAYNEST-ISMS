# PayNest — Information Security Management System (ISMS)

> **Portfolio Note:** PayNest is a fictional financial services company created for a Governance, Risk, and Compliance (GRC) portfolio project.

## Project Overview
This repository documents a practical ISMS design for **PayNest** (v1.0, owned by the Information Security Officer), covering information used to deliver credit, savings, deposit-taking, and wallet services across its Tamale office, mobile app, website, USSD channel, and field agents. It is structured around **ISO/IEC 27001** principles alongside relevant fintech data protection and operational resilience considerations.

## ISMS Scope Statement
The ISMS of PayNest applies to the protection of information used to provide credit, savings, deposit-taking, and wallet services through its Tamale office, mobile app, website, USSD, and field agents.

### Included
* **People:** All 25 staff (office and remote, in Ghana) and field agents
* **Information:** Customer personal data, accounts, wallets, transaction records, credit records, and staff records
* **Systems:** In-house software, core systems, databases, Microsoft 365 *(non-sensitive use only)*, office and mobile devices
* **Connectivity and Power:** MTN internet, Starlink backup, UPS, and backup generator
* **Hosting and Backup:** Primary servers at **Onix Data Centre, Accra**; encrypted backup server at the **Tamale office**
* **Suppliers and Dependencies:** Onix, Microsoft, MTN, Starlink, USSD provider, and independent security tester

### Exclusions
* **Customers' own phones and computers:** Devices PayNest does not control are excluded *(the security of PayNest's app, website, USSD service, and customer data remains in scope)*.
* **Suppliers' own equipment and buildings:** Underlying supplier infrastructure and facilities are excluded *(PayNest's management of supplier risks remains in scope)*.

## Repository Structure
* `01-context-and-scope/` — Scope statement (`scope.md`), asset and data classification register, and context/compliance notes
* `02-risk-management/` — Risk methodology, risk register, and treatment plans
* `03-policies-and-soa/` — Core ISMS policies, operational procedures, and Statement of Applicability (SoA)
* `04-third-party-risk/` — Supplier tiering and dependency controls (Onix, Microsoft, MTN, Starlink, USSD provider, security tester)
* `05-assurance-and-evidence/` — Sample audit checklists, access reviews, incident runbooks, and failover/backup test logs
