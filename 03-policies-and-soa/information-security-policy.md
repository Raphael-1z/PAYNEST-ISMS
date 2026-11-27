# PayNest Information Security Policy

**Document Version:** 1.0 | **Owner:** Information Security Officer | **Scope Reference:** PayNest ISMS Scope (v1.0) | **Framework Alignment:** ISO/IEC 27001

## 1. Purpose and Scope
This policy sets the overarching information security rules for **PayNest** across its credit, savings, deposit-taking, and wallet services delivered through its Tamale office, mobile app, website, USSD channel, and field agents. It applies to all 25 staff (office and remote in Ghana) and field agents, as well as the systems, data, connectivity/power support, and third-party dependencies within PayNest's ISMS scope.

In alignment with the PayNest ISMS Scope Statement, primary servers are hosted at **Onix Data Centre (Accra)**, an **encrypted backup server** operates at the **Tamale office**, connectivity and power rely on **MTN internet**, **Starlink backup**, **UPS**, and a **backup generator**, and **Microsoft 365** is restricted to *non-sensitive use only*. Customers' own phones and computers and suppliers' internal equipment and buildings are excluded from direct PayNest technical control, while PayNest's applications, data, and supplier risk management remain in scope.

## 2. Roles and Responsibilities
* **Information Security Officer:** Owns the ISMS, risk methodology, policy governance, Statement of Applicability, and assurance reporting.
* **Asset and Risk Owners (Engineering, Database/Infrastructure, Payments/Integrations, IT/Network, IT Support, Field Operations & QA, HR, Compliance & Credit, Facilities):** Enforce controls, maintain accurate inventories, remediate assigned risks, and report incidents within their operational domains.
* **All Staff (25 Office & Remote) and Field Agents:** Follow acceptable use, access, data classification, and incident reporting rules; protect PayNest devices and customer/transaction records.
* **Third-Party Suppliers & Independent Security Testers:** Comply with contractual security terms, SLAs, NDAs, and rules of engagement aligned with PayNest's TPRM policy.

## 3. Data Classification and Handling Rules
Information is classified into **Restricted**, **Confidential**, and **Internal** tiers based on sensitivity and impact to PayNest and its customers:
* **Restricted:** Customer personal data (PII), KYC/credit records, accounts, wallets, savings, deposits, transaction records, core databases/backups, and sensitive HR/staff records. Requires strict access control, encryption at rest and in transit, logging, and careful handling.
* **Confidential:** In-house software/APIs, mobile/web/USSD integration details, non-sensitive M365 operational records, security testing reports, and PayNest-managed endpoint configurations.
* **Internal:** Operational guidance, network/connectivity status, and support infrastructure details intended for internal use.

**Microsoft 365 Boundary:** Microsoft 365 is approved for *non-sensitive use only*. Storing or processing *Restricted* customer financial, credit, KYC, or sensitive staff records on Microsoft 365 is prohibited.

**Customer Devices & Field Agents:** PayNest does not control customers' personal phones or computers, so mobile/web/USSD channels and backend systems must enforce strong authentication, transport encryption, session integrity, and transaction validation. Field agent devices must use device locks, MDM/remote-wipe controls, minimal offline caching, and prompt reporting of loss or theft.

## 4. Core Security Controls and Continuity
* **Access & Authentication:** Apply least privilege, role-based access control (RBAC), privileged access oversight, strong authentication/MFA, and timely revocation upon role change or offboarding.
* **Hosting, Backups & Resilience:** Protect core systems and databases hosted at Onix Data Centre (Accra), maintain encrypted backups on the Tamale backup server with periodic restore testing, and maintain MTN internet, Starlink backup, UPS, and generator failover readiness in Tamale.
* **Secure Change & Vulnerability Management:** Embed security checks into software/API/USSD changes, address vulnerabilities promptly, and scope independent security testing under signed NDAs and rules of engagement.
* **Incident Management:** Report suspected security incidents, fraud/abuse anomalies, or lost/stolen devices immediately so containment, escalation, and recovery can occur without delay.

## 5. Policy Compliance and Review
Non-compliance with this policy may result in access restriction, disciplinary action, or contract termination where applicable. This policy is reviewed **annually** or when significant scope, infrastructure, supplier, or regulatory changes occur.
