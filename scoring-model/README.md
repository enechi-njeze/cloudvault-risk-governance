# Risk Scoring Methodology

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** NIST SP 800-30 Rev. 1, Appendices G, H, and I
**Document ID:** FHX-RISK-SCORE-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault FHX
**Review Cycle:** Annual (or upon significant change to threat landscape or system impact categorization)
**Classification:** Internal Use Only

---

## Purpose

This folder documents the risk scoring methodology used to evaluate and prioritize risks in the CloudVault FHX Enterprise Risk Register. A consistent, documented scoring approach is essential for three reasons:

First, it ensures that risk scores are reproducible: two analysts reviewing the same threat scenario should arrive at the same or comparable score using this framework. Consistency is critical when presenting risk posture to the AO, CISO, and executive stakeholders.

Second, it provides audit traceability. When ClearPath Security Assessors LLC reviews the risk register during a FedRAMP assessment, they need to understand how scores were derived. This document provides that basis.

Third, it aligns FHX risk scoring with federal standards. NIST SP 800-30 Appendix I provides the semi-quantitative risk methodology that underpins this model. FHX has adapted NIST's framework to reflect the specific mission context of a federal health data exchange serving 47 agencies.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| FHX-RISK-SCORE-001.md | This document (methodology overview) | NIST SP 800-30 App. I | Current |
| likelihood-definitions.md | Detailed likelihood level definitions with examples | NIST SP 800-30 App. G | Current |
| impact-definitions.md | Detailed impact level definitions for CIA triad | NIST SP 800-30 App. H | Current |
| risk-matrix.md | Full 5x5 Likelihood x Impact risk matrix | NIST SP 800-30 App. I | Current |
| contextual-adjustments.md | FHX-specific contextual factors for risk scoring | FHX Risk Management Strategy | Current |
| scoring-examples.md | Worked examples of risk scoring for common FHX scenarios | NIST SP 800-30 | Current |

---

## Scoring Framework Overview

FHX uses a semi-quantitative risk scoring approach based on NIST SP 800-30. Semi-quantitative scoring uses defined numerical scales for likelihood and impact, then combines them using a matrix to produce an overall risk score. This approach is more rigorous than qualitative-only approaches (High/Medium/Low without numeric basis) and more practical than fully quantitative approaches (which require actuarial data often unavailable in federal environments).

**Risk Score = Likelihood Level x Impact Level**

Both likelihood and impact are scored on a 1-5 scale. The product yields a risk score between 1 and 25. Risk scores are then mapped to a five-tier risk rating.

---

## Likelihood Scale

Likelihood reflects the probability that a threat source will successfully exploit a vulnerability in the FHX environment, given existing controls. Likelihood is assessed at the residual level after accounting for implemented controls.

| Level | Value | Definition | Representative Frequency |
|---|---|---|---|
| Very Low | 1 | The threat source lacks capability or motivation; no known instances in similar environments | Less than once per 10 years |
| Low | 2 | The threat source has limited capability; exploitation would require unusual circumstances | Once per 3-10 years |
| Moderate | 3 | The threat source has demonstrated capability; exploitation is plausible given current controls | Once per 1-3 years |
| High | 4 | The threat source has demonstrated capability and motivation; exploitation has occurred in similar environments | Once per 6-12 months |
| Very High | 5 | The threat source actively targets this type of system; exploitation is expected without additional controls | More than once per 6 months |

**FHX Contextual Note:** Given that CloudVault FHX handles PHI for 890,000-plus patients and processes FTI data, it represents a high-value target for APT groups, cybercriminals, and nation-state actors. The baseline likelihood for threat sources targeting health sector federal systems is Moderate, and specific scenarios involving known APT TTPs are scored at High.

---

## Impact Scale

Impact reflects the consequence of a successful exploitation of a vulnerability, measured across all three dimensions of the CIA triad: Confidentiality, Integrity, and Availability. For FHX, impact scoring also incorporates mission/business impact to the 47 federal agencies and 890,000-plus patients served.

| Level | Value | Confidentiality Impact | Integrity Impact | Availability Impact | Mission/Business Impact |
|---|---|---|---|---|---|
| Very Low | 1 | Disclosure of non-sensitive internal information | Negligible modification; easily detected and corrected | Brief outage, less than 1 hour, no user impact | Minimal mission degradation |
| Low | 2 | Disclosure of sensitive but non-personal information | Minor data modification; detectable through routine review | Short outage, 1-4 hours, limited user impact | Minor mission degradation |
| Moderate | 3 | Disclosure of PII or business-sensitive data for limited population | Moderate data modification; may require manual reconciliation | Extended outage, 4-24 hours, significant user impact | Moderate mission degradation across some agencies |
| High | 4 | Disclosure of PHI, CUI, or FTI for significant population | Significant data modification; difficult to reconcile | Major outage, 1-7 days, widespread user impact | Major mission degradation; regulatory violation likely |
| Very High | 5 | Mass disclosure of PHI, CUI, or FTI; breach notification required | Widespread data corruption; integrity cannot be assured | Extended outage, more than 7 days, or permanent data loss | Catastrophic mission failure; federal health exchange unavailable |

**FHX Contextual Note:** Because FHX handles federally regulated data (PHI, FTI, PII, CUI), the regulatory impact of a significant data event scales the impact level upward. Any scenario involving reportable HIPAA breach to 500-plus individuals is scored at Impact 4 (High) at minimum. Mass PHI disclosure affecting thousands of patients is scored at Impact 5 (Very High).

---

## Risk Matrix (Likelihood x Impact)

The following matrix maps the combination of likelihood and impact values to an overall risk rating. Scores of 15 and above are rated High. Scores of 8-14 are Moderate. Scores of 4-7 are Low. Scores of 1-3 are Very Low.

|  | **Impact 1** | **Impact 2** | **Impact 3** | **Impact 4** | **Impact 5** |
|---|---|---|---|---|---|
| **Likelihood 5** | 5 (Low) | 10 (Moderate) | 15 (High) | 20 (Very High) | 25 (Very High) |
| **Likelihood 4** | 4 (Low) | 8 (Moderate) | 12 (Moderate) | 16 (High) | 20 (Very High) |
| **Likelihood 3** | 3 (Very Low) | 6 (Low) | 9 (Moderate) | 12 (Moderate) | 15 (High) |
| **Likelihood 2** | 2 (Very Low) | 4 (Low) | 6 (Low) | 8 (Moderate) | 10 (Moderate) |
| **Likelihood 1** | 1 (Very Low) | 2 (Very Low) | 3 (Very Low) | 4 (Low) | 5 (Low) |

---

## Risk Rating Definitions

| Rating | Score Range | Required Response | Reporting |
|---|---|---|---|
| Very High | 20-25 | Immediate escalation to AO and CISO; treatment plan required within 5 business days | AO notification within 24 hours; monthly ConMon update |
| High | 15-19 | Active treatment plan required; CISO and System Owner notified; POA&M entry within 15 days | Quarterly AO briefing; monthly ConMon update |
| Moderate | 8-14 | Treatment plan developed; ISSO tracks to closure; POA&M if SLA-constrained | Quarterly risk register review; ConMon update when score changes |
| Low | 4-7 | Monitor; accept or schedule remediation at next opportunity | Annual risk register review |
| Very Low | 1-3 | Accept with documentation; no active treatment required | Annual risk register review |

---

## Residual Risk Calculation

Inherent risk is the risk score before controls are applied. Residual risk is the score after existing controls reduce likelihood or impact. The residual risk score is the primary basis for risk treatment decisions.

**Example: FHX-RISK-001 (Unauthorized PHI Access via Compromised Privileged Account)**

- Inherent Likelihood: 4 (High) — APT capability and motivation against federal health targets is well documented
- Inherent Impact: 5 (Very High) — Mass PHI disclosure would require HIPAA breach notification
- Inherent Risk Score: 20 (Very High)
- Existing Controls: MFA on all privileged accounts, PAM tooling, 90-day access reviews, UEBA alerting
- Control Effectiveness: Controls reduce likelihood from 4 to 3 (Moderate)
- Residual Likelihood: 3 (Moderate)
- Residual Impact: 5 (unchanged — controls reduce likelihood, not consequence)
- Residual Risk Score: 15 (High)
- Treatment: Mitigate further through PAM maturity enhancement program

---

## Contextual Scoring Adjustments

FHX applies three contextual adjustments that may modify raw likelihood or impact scores:

**Adjustment 1: Regulatory Multiplier**
If exploitation would trigger mandatory federal reporting (HIPAA breach, FTI incident, FISMA major incident), the impact score is increased by 1 tier if not already at Very High.

**Adjustment 2: Threat Intelligence Modifier**
If current threat intelligence (CISA advisories, FS-ISAC alerts, FBI flash notifications) specifically identifies active exploitation of the relevant vulnerability in the health sector, the likelihood score is increased by 1 tier.

**Adjustment 3: Data Sensitivity Modifier**
If the affected data includes FTI (subject to IRS Publication 1075), the impact score is increased by 1 tier if not already at Very High, due to the heightened legal and operational consequences of FTI compromise.

---

## Related Documents

- [Enterprise Risk Register](../risk-register/README.md)
- [Governance Workflows](../governance-workflows/README.md)
- [Corrective Actions](../corrective-actions/README.md)
- [NIST RMF Step 4 Assess](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/step4-assess/README.md)
- [FedRAMP ATO](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
