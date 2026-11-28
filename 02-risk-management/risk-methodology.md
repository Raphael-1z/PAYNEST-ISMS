# PayNest Risk Assessment Methodology

**Document Version:** 1.0 | **Owner:** Information Security Officer | **Scope Reference:** PayNest ISMS Scope (v1.0) | **Framework Alignment:** ISO/IEC 27001

## 1. Purpose and Context
This methodology defines how **PayNest** identifies, analyzes, evaluates, and treats information security risks across its credit, savings, deposit-taking, and wallet services. It operates across PayNest's Tamale office, mobile app, website, USSD channel, and field agents, covering all 25 staff (office and remote in Ghana) and field agents.

In alignment with the PayNest ISMS Scope Statement, primary servers reside at **Onix Data Centre (Accra)**, an encrypted backup server resides at the **Tamale office**, connectivity and power rely on **MTN internet**, **Starlink backup**, **UPS**, and a **backup generator**, and **Microsoft 365** is restricted to *non-sensitive use only*. Customer-owned phones/computers and suppliers' own equipment/buildings are excluded from direct technical control, while PayNest's applications, data, and supplier risk management remain in scope.

## 2. Risk Identification Approach
Risks are identified systematically from the **PayNest Asset and Data Classification Register** (`AST-001` through `AST-017`), threat scenarios relevant to mobile/USSD/wallet/credit/deposit operations, operational resilience failure modes, regulatory/compliance obligations, and supplier dependencies (Onix, Microsoft, MTN, Starlink, USSD provider, and independent security tester). Scored entries are recorded in `02-risk-management/risk-register.csv`.

* **Asset-Driven Scenarios:** Each risk links to one or more registered assets and considers Confidentiality, Integrity, and Availability (CIA) impacts.
* **Channel & Operational Scenarios:** Evaluates risks around mobile/web/USSD transactions, field agent handling, power/internet failover in Tamale, Onix hosting dependencies, and M365 non-sensitive boundary enforcement.

## 3. Scoring Scales (Likelihood and Impact)
Both Likelihood and Impact are scored on a **1 to 5 scale** to establish consistent, auditable ratings.

### 3.1 Likelihood Scale (1–5)
| Score | Rating | Definition & Indicative Frequency |
| :--- | :--- | :--- |
| **1** | Rare | Unlikely to occur under normal circumstances; may happen only in exceptional situations (< once every 3–5 years). |
| **2** | Unlikely | Could occur occasionally; limited historical precedent or strong existing deterrents (roughly once every 1–3 years). |
| **3** | Possible | Might occur at some point; realistic threat vector or recurring environmental/operational factor (several times a year to annually). |
| **4** | Likely | Will probably occur in many circumstances; observed vulnerabilities, high exposure, or frequent operational stress (monthly to quarterly). |
| **5** | Almost Certain | Expected to occur frequently or continuously unless actively controlled (weekly or more often). |

### 3.2 Impact Scale (1–5)
| Score | Rating | Financial, Operational, Legal/Regulatory & Reputational Criteria |
| :--- | :--- | :--- |
| **1** | Negligible | Minimal financial loss; minor local inconvenience handled within normal routines; no regulatory breach or material reputational impact. |
| **2** | Minor | Low financial impact; brief single-channel or single-user disruption with quick workaround; minor internal policy deviation. |
| **3** | Moderate | Noticeable financial loss or delayed collections/settlements; temporary service degradation across a channel or team; potential data protection/compliance scrutiny or localized customer complaints. |
| **4** | Major | Substantial financial loss, ledger/transaction discrepancies, or prolonged outage affecting core/wallet/credit/deposit services; regulatory investigation, contractual breach, or significant reputational harm. |
| **5** | Severe / Catastrophic | Severe financial loss or solvency/liquidity shock; widespread compromise of Restricted customer PII, wallet/deposit/credit records, or core systems; severe regulatory enforcement/license risk or lasting loss of customer trust. |

## 4. Risk Calculation, Risk Matrix, and Risk Appetite
**Inherent Risk Score** is `Likelihood × Impact` before controls (range **1** to **25**). **Current Risk Score** reflects only controls operating today: risks whose treatment is *Planned* keep their inherent score, and partially treated (*In Progress*) risks may be credited only for what is already in place. **Target Risk Score** is the level expected once all planned controls are implemented and verified. Risk acceptance and sign-off decisions use the current score.

| Risk Score Range | Risk Level | Governance Action & Approval Requirement |
| :--- | :--- | :--- |
| **1 – 4** | Low | Acceptable within routine operations; monitor periodically via standard controls. |
| **5 – 9** | Medium | Manage through defined controls and regular monitoring; review quarterly by asset/risk owner. |
| **10 – 14** | High | Requires prioritized treatment plan and targeted controls; requires Information Security Officer and operational lead sign-off. |
| **15 – 25** | Critical | Immediate executive escalation and mandatory treatment action; requires formal management acceptance if any current score remains elevated. |

**PayNest Risk Appetite:** PayNest maintains a **low risk appetite** for unauthorized access, alteration, or loss of *Restricted* data (customer PII, credit/KYC records, accounts, wallets, deposits, savings, transactions, and HR records) and for prolonged unavailability of core/USSD/wallet services. Current risks scoring **10 or above** require documented justification and executive/Information Security Officer approval.

## 5. Risk Treatment Options
1. **Mitigate:** Implement technical, physical, or procedural controls to reduce Likelihood, Impact, or both.
2. **Transfer:** Shift or share financial/operational risk through contracts, SLAs, insurance, or vetted third-party arrangements (recognizing that accountability and TPRM oversight remain with PayNest).
3. **Avoid:** Eliminate the risk by discontinuing, restricting, or not initiating the activity or data handling practice (for example, enforcing *Microsoft 365 non-sensitive use only*).
4. **Accept:** Consciously retain a low or justified current risk where further treatment is disproportionate, subject to formal approval and periodic review.

## 6. Review Cadence and Governance
The Risk Register (`02-risk-management/risk-register.csv`) is reviewed **quarterly** and whenever major architectural, supplier, channel, or regulatory changes occur (such as changes to Onix hosting, USSD integration, field agent workflows, or connectivity/power setups in Tamale).
