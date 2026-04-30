# Risk Governance Diagrams and Architecture

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** NIST SP 800-39, NIST SP 800-30, ISO 31000:2018
**Document ID:** FHX-RISK-DIAG-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault FHX
**Review Cycle:** Annual (or upon significant change to risk governance structure)
**Classification:** Internal Use Only

---

## Purpose

This folder contains the process flow diagrams, governance architecture maps, and visual reference materials that support the CloudVault FHX risk governance program. Visual documentation complements the procedural documents in other folders by making complex governance relationships and workflows immediately understandable to diverse audiences.

During a FedRAMP assessment or FISMA audit, these diagrams help the 3PAO (ClearPath Security Assessors LLC) and IG auditors understand how risk governance functions in practice. They also support executive briefings where the AO and CISO need a high-level view of the program without reading through every procedure document.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| FHX-RISK-DIAG-001.md | This document (diagrams index and descriptions) | NIST SP 800-39 | Current |
| risk-governance-architecture.md | Three-tier risk governance structure: Tier 1 (Org), Tier 2 (Mission), Tier 3 (System) | NIST SP 800-39 | Current |
| risk-lifecycle-flow.md | End-to-end risk lifecycle: identification through treatment to closure | NIST SP 800-30 | Current |
| riskcomm-structure.md | Risk Governance Committee membership, authority, and reporting lines | FHX Risk Governance Charter | Current |
| risk-reporting-flow.md | Risk report production and distribution workflow | NIST SP 800-39 Tier 1 | Current |
| risk-escalation-flow.md | Visual escalation path for Very High and High risk triggers | FHX Risk Governance Charter | Current |
| risk-treatment-decision-tree.md | Decision tree for selecting risk treatment option (mitigate, accept, transfer, avoid) | NIST SP 800-30 Sec. 3.3 | Current |

---

## Risk Governance Architecture: Three-Tier Framework

NIST SP 800-39 defines risk management across three tiers. The FHX risk governance architecture implements all three tiers with clear ownership and integration.

**Tier 1: Organization Level**
At the organization tier, risk governance is led by the CISO (Angela Torres) with AO (Deputy Director Henry Kline) as the final risk decision authority. The Risk Governance Committee (RGC) operates at this tier. Decisions made here include: risk appetite, risk acceptance above Moderate, FedRAMP authorization maintenance, and FISMA annual reporting. The System Owner (Dr. Patricia Owens) participates at this tier to ensure mission context informs governance decisions.

**Tier 2: Mission/Business Process Level**
At the mission tier, risk governance focuses on the FHX business processes: health data exchange, enrollment services, agency connectivity, and privacy management. The ISSO (Enechi P.C. Njeze) and Privacy Officer (Sandra Voss) operate primarily at this tier. Decisions here include: risk prioritization by business impact, privacy risk assessment, and cross-process risk integration. Monthly risk register updates and quarterly executive dashboards are produced at this tier.

**Tier 3: Information System Level**
At the system tier, technical risk is identified, scored, and tracked by the ISSO and DevOps Lead (Trevor L. Abrams). Vulnerability scan results, configuration findings, penetration test outcomes, and security incident analysis all feed risk identification at this tier. Corrective actions and POA&M entries are managed here and escalated upward when warranted.

**Integration Points:**
- Tier 3 findings flow up to Tier 2 via the monthly risk register update
- Tier 2 priorities flow up to Tier 1 via the quarterly AO risk briefing package
- Tier 1 risk appetite decisions flow down to Tier 2 and 3 via the Risk Management Strategy document
- Tier 1 AO acceptance decisions flow down to Tier 3 via POA&M entries

---

## Risk Lifecycle: Identification to Closure

Every risk in the FHX enterprise risk register follows a defined lifecycle. This lifecycle ensures no risk is indefinitely open without a deliberate governance decision.

**Phase 1: Identification**
Risk sources include: vulnerability scan results, threat intelligence feeds (CISA KEV, FS-ISAC), penetration test findings, security incident analysis, system change assessments, and ISSO-initiated risk reviews. Any team member may identify a potential risk and submit it to the ISSO for evaluation.

**Phase 2: Analysis and Scoring**
The ISSO applies the FHX risk scoring methodology (documented in scoring-model/) to calculate the inherent and residual risk scores. Contextual adjustments are applied for regulatory multipliers and threat intelligence modifiers. The scored risk entry is added to the risk register.

**Phase 3: Treatment Decision**
The ISSO recommends a treatment option (mitigate, accept, transfer, avoid). For risks scored High or Very High, the CISO and AO are notified. The Risk Governance Committee approves treatment decisions for High and Very High risks.

**Phase 4: Treatment Execution**
Corrective action plans are developed and tracked in corrective-actions/. For accepted risks, the AO risk acceptance package is prepared and submitted. Treatment progress is reported monthly to the CISO and quarterly to the AO.

**Phase 5: Verification**
Upon completion of corrective actions, the ISSO independently verifies that the treatment has reduced the residual risk score as expected. Verification evidence is documented in the closure record.

**Phase 6: Closure**
Verified treatments result in risk closure. The risk entry is moved to the closed register with the closure date, verifying evidence, and final residual score. Closed risks are reviewed annually to confirm they have not recurred.

---

## Risk Governance Committee Structure

| Role | Member | Authority Level | Decision Types |
|---|---|---|---|
| Authorizing Official (Chair) | Deputy Director Henry Kline | Final authority | Risk acceptance, ATO decisions, Very High risk disposition |
| CISO (Vice Chair) | Angela Torres | Program authority | High risk treatment approval, resource allocation |
| System Owner | Dr. Patricia Owens | Mission authority | Business impact prioritization, mission risk tolerance |
| ISSO / ISSM (Secretary) | Enechi P.C. Njeze | Operational authority | Risk identification, scoring, treatment recommendations |
| Privacy Officer | Sandra Voss | Privacy authority | PHI/PII risk disposition, HIPAA compliance risk |
| DevOps Lead | Trevor L. Abrams | Technical authority | Technical feasibility of treatments, remediation timelines |
| 3PAO (Advisory) | ClearPath Security Assessors LLC | Assessment authority | Control effectiveness opinion, assessment risk input |

**Reporting Structure:**
- RGC reports to AO on risk posture at each quarterly meeting
- ISSO reports to CISO monthly on risk register updates
- CISO reports to CIO and Deputy Director on program-level risk annually

---

## Risk Reporting Flow

The risk reporting flow describes how information moves from technical risk identification through executive decision-making.

**Monthly Flow:**
- ISSO compiles monthly risk register update from vuln scan data, incident logs, and system changes
- ISSO submits monthly risk summary to CISO (5th business day of following month)
- Risk summary data incorporated into FedRAMP monthly ConMon report (last business day of month)

**Quarterly Flow:**
- ISSO prepares Executive Risk Dashboard from monthly data (due 15th of month after quarter close)
- ISSO prepares AO Risk Briefing Package (delivered with Executive Dashboard)
- Privacy Officer receives PHI/PII-focused risk report (same deadline)
- RGC meets to review full risk register and make treatment decisions
- AO reviews and signs risk acceptance decisions

**Annual Flow:**
- ISSO prepares FHX inputs for FISMA annual report (January)
- Full risk assessment conducted with 3PAO participation (Q1 of each FY)
- Risk appetite statement reviewed and reaffirmed by CISO and AO
- Risk Management Strategy updated if material changes required

---

## Risk Escalation Decision Flow

The escalation decision flow defines the branch conditions that determine when a risk requires elevation above the standard monthly review cycle.

**Condition 1: Risk scored Very High at identification**
Path: ISSO immediately to CISO (within 4 hours) to AO (within 24 hours) to emergency RGC (within 5 days)

**Condition 2: Existing risk score increases to High or Very High**
Path: ISSO to CISO within 24 hours, priority item at next RGC; if RGC is more than 30 days away, direct notification to AO

**Condition 3: Active exploitation detected for a risk scenario in the register**
Path: ISSO to CISO immediately, incident response protocol activated, risk register updated same day, AO notification within 24 hours

**Condition 4: SLA breach on High risk corrective action**
Path: ISSO to CISO immediately, revised treatment plan to AO within 5 business days, risk acceptance if revised timeline exceeds 30 days beyond original SLA

**Condition 5: ConMon finding requires out-of-cycle report**
Path: ISSO prepares out-of-cycle ConMon report, CISO reviews and approves, submitted to FedRAMP PMO and AO within 72 hours of trigger event

---

## Related Documents

- [Enterprise Risk Register](../risk-register/README.md)
- [Risk Scoring Model](../scoring-model/README.md)
- [Governance Workflows](../governance-workflows/README.md)
- [Stakeholder Reporting](../stakeholder-reporting/README.md)
- [Corrective Actions](../corrective-actions/README.md)
- [NIST RMF](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/README.md)
- [FedRAMP ATO](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
