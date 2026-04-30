# Stakeholder Risk Reporting

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** NIST SP 800-39, FISMA Annual Reporting Requirements, FedRAMP ConMon Guide
**Document ID:** FHX-RISK-RPT-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Review Cycle:** Reports issued per schedule; templates reviewed annually
**Classification:** Internal Use Only

---

## Purpose

Risk reporting is the mechanism by which the ISSO translates technical risk data into strategic information that decision-makers can act on. A well-structured risk report answers three questions for the reader: Where do we stand today? What has changed since the last report? What decisions are needed?

Effective stakeholder risk reporting requires understanding the audience. The Authorizing Official needs to know whether the current risk posture supports maintaining the ATO. The CISO needs to know where to direct resources. The System Owner needs to understand operational impacts. The Privacy Officer needs to know about PHI and PII risk. Each audience receives reporting calibrated to their role and decision authority.

This folder contains the templates, completed reports, and distribution records for all risk-related reporting at CloudVault FHX.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| FHX-RISK-RPT-001.md | This document (reporting program overview) | NIST SP 800-39 | Current |
| executive-risk-dashboard-q2-2025.md | Q2 2025 executive risk dashboard (AO/CISO level) | NIST SP 800-39 Tier 1 | Current |
| executive-risk-dashboard-q1-2025.md | Q1 2025 executive risk dashboard | NIST SP 800-39 Tier 1 | Archived |
| ao-risk-briefing-template.md | Quarterly AO risk briefing template and format guide | FedRAMP ATO Process | Current |
| ao-risk-briefing-q2-2025.md | Q2 2025 AO risk briefing package | FedRAMP ConMon | Current |
| fisma-annual-risk-report-fy2025.md | FISMA annual risk reporting contribution for FY 2025 | FISMA / OMB Circular A-130 | Current |
| ciso-monthly-risk-summary-template.md | Monthly risk summary for CISO review | FHX Risk Governance Charter | Current |
| privacy-risk-report-q2-2025.md | Q2 2025 risk report for Privacy Officer (PHI/PII focus) | HIPAA, OMB M-17-12 | Current |
| risk-trend-analysis-fy2025.md | Full-year risk trend analysis for FY 2025 | NIST SP 800-137 | Current |

---

## Reporting Calendar

| Report | Audience | Frequency | Deadline | Owner |
|---|---|---|---|---|
| Monthly CISO Risk Summary | CISO Angela Torres | Monthly | 5th business day of following month | ISSO |
| Quarterly Executive Risk Dashboard | AO, CISO, System Owner | Quarterly | 15th of month following quarter close | ISSO |
| AO Risk Briefing Package | AO Henry Kline | Quarterly | Delivered with Executive Dashboard | ISSO |
| Privacy Risk Report | Privacy Officer Sandra Voss | Quarterly | 15th of month following quarter close | ISSO |
| FISMA Annual Risk Report | CIO, IG Office, OMB | Annually | February 1 | ISSO, CISO |
| FedRAMP Monthly ConMon | FedRAMP PMO, AO | Monthly | Last business day of month | ISSO |
| Ad Hoc Escalation Report | AO, CISO | As needed | Within 24 hours of trigger event | ISSO |

---

## Executive Risk Dashboard: Q2 2025

The following summarizes the Q2 2025 risk posture for CloudVault FHX at the executive level.

### Risk Posture Summary

| Metric | Q1 2025 | Q2 2025 | Change | Status |
|---|---|---|---|---|
| Total Open Risks | 13 | 12 | -1 | Improving |
| Very High Risks | 0 | 0 | No change | On Target |
| High Risks | 3 | 2 | -1 | Improving |
| Moderate Risks | 8 | 8 | No change | Stable |
| Low Risks | 2 | 2 | No change | Stable |
| AO Risk Acceptances Active | 2 | 1 | -1 | Improving |
| POA&M Items Open | 14 | 12 | -2 | Improving |
| POA&M Items Overdue | 1 | 0 | -1 | On Target |

### Q2 2025 Risk Highlights

**Risk Closed This Quarter:** FHX-RISK-013 (Excessive administrative access to legacy reporting module) was closed following completion of the IAM right-sizing project for legacy systems. DevOps Lead Trevor Abrams confirmed all legacy admin accounts were reviewed, right-sized, and re-documented with individual accountability.

**Risk Score Reduced:** FHX-RISK-002 (Ransomware) was reduced from High (score 16) to Moderate (score 12) following implementation of isolated backup vaulting in AWS GovCloud and completion of the Q2 disaster recovery exercise. Residual likelihood decreased from 4 to 3.

**Risk Acceptance Expired and Closed:** AO acceptance for FHX-RISK-016 (Minor configuration deviation in legacy network gateway) was allowed to expire following successful remediation. No renewal required.

**Ongoing Concerns:** FHX-RISK-001 (Privileged account compromise) and FHX-RISK-004 (API abuse) remain the two most significant open risks. Treatment plans are active. ISSO recommends continued prioritization of PAM maturity enhancement in Q3 2025 planning.

---

## AO Risk Briefing Package Structure

The quarterly AO risk briefing package follows a standardized structure to support consistent, efficient decision-making by AO Henry Kline.

**Section 1: ATO Status Confirmation**
Statement confirming that the system's risk posture remains within the AO's accepted risk threshold and that continuous authorization is maintained. If any risk has exceeded the threshold, this section flags it explicitly.

**Section 2: Risk Register Summary**
One-page summary of open risks by tier, with comparison to prior quarter. Highlights risks that have increased, decreased, or been newly identified since the last briefing.

**Section 3: POA&M Status**
Summary of open POA&M items, on-time closure rate, and any items requiring AO awareness (items at or near SLA limit, new High-risk entries, or items where original remediation plan has changed materially).

**Section 4: Risk Acceptance Actions Required**
Any risk acceptance requests pending AO decision, with CISO recommendation, business justification, and proposed acceptance period. AO signature block included.

**Section 5: Significant Changes Affecting Risk Posture**
Summary of system changes, new threat intelligence, or external events that have materially affected the FHX risk posture since the last briefing.

**Section 6: Upcoming Risk Activities**
Scheduled risk activities in the coming quarter: assessments, penetration tests, major system changes, vendor contract renewals, or FedRAMP reporting deadlines.

---

## FISMA Annual Risk Reporting

CloudVault FHX contributes to the agency FISMA annual report submitted to OMB each February. The ISSO prepares the FHX-specific risk inputs that feed the agency CIO's consolidated FISMA report.

| Input | Description | Deadline |
|---|---|---|
| System risk level and categorization | FIPS 199 categorization confirmation | January 10 |
| ATO status and expiration | Current authorization status and authorization date | January 10 |
| Significant deficiency summary | Count and description of significant deficiencies (High risks without accepted mitigations) | January 15 |
| POA&M summary | Total open items, on-time closure rate, items by severity | January 15 |
| Security incident summary | Incidents reported during the fiscal year with resolution status | January 15 |
| Privacy risk summary | PHI/PII risk events, HIPAA compliance status | January 20 |
| Continuous monitoring status | Scan coverage rate, ConMon reporting compliance | January 20 |

---

## Risk Communication Principles

The FHX risk reporting program follows these communication principles to ensure reports are useful and not merely compliance artifacts:

**Principle 1: Lead with the risk, not the process.** Executive reports begin with the risk picture, not with descriptions of what the ISSO did. Readers want to know: Is the system safe? What decisions do I need to make?

**Principle 2: Translate technical findings into business language.** FHX-RISK-001 is not simply "insufficient PAM controls." It means: there is a meaningful chance that an attacker who compromises a privileged account could access PHI for hundreds of thousands of patients. Frame it that way for executives.

**Principle 3: Recommend, don't just report.** Every report includes an ISSO recommendation section. Leadership should never have to ask "So what should we do?" The ISSO's job is to advise.

**Principle 4: Consistent format enables fast comparison.** Using the same report structure each quarter means readers can quickly spot what has changed. Consistency builds trust in the reporting program.

**Principle 5: Support the AO's authorization decision.** The AO must maintain an informed view of system risk at all times. The ISSO's reporting is the primary vehicle for that awareness. Every report should help the AO determine whether they would still grant the ATO today.

---

## Related Documents

- [Enterprise Risk Register](../risk-register/README.md)
- [Governance Workflows](../governance-workflows/README.md)
- [Corrective Actions](../corrective-actions/README.md)
- [Risk Scoring Model](../scoring-model/README.md)
- [FedRAMP ConMon](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/step6-monitor/README.md)
- [NIST RMF Step 5 Authorize](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/step5-authorize/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
