# Corrective Actions and Risk Treatment Plans

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** NIST SP 800-30 Section 3.3, FedRAMP POA&M Template, NIST SP 800-53 CA-5
**Document ID:** FHX-RISK-CAP-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault FHX
**Review Cycle:** Monthly tracking update, Quarterly formal review
**Classification:** Internal Use Only

---

## Purpose

Identifying risks is only the beginning. The value of a risk management program lies in what happens after a risk is identified: the systematic, accountable, and documented process of treating that risk. This folder contains the corrective action register, risk treatment plans, and supporting documentation for all active risk mitigation efforts at CloudVault FHX.

A corrective action, in the context of federal GRC practice, is any planned activity intended to reduce a known risk to within the organization's risk appetite. Corrective actions range from patching a specific vulnerability to implementing a new program-wide control. Each action is assigned an owner, a completion date, milestones, and an expected residual risk score upon completion.

This folder integrates with the FedRAMP POA&M register. Any risk that cannot be fully remediated within its standard timeline becomes a POA&M item. The corrective action register serves as the planning document that informs each POA&M entry.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| FHX-RISK-CAP-001.md | This document (corrective action program overview) | NIST SP 800-30 | Current |
| corrective-action-register.md | Active corrective action register with all open items | FedRAMP POA&M Template | Current |
| risk-treatment-plan-risk001.md | Risk treatment plan for FHX-RISK-001 (PAM enhancement) | NIST SP 800-30 Sec. 3.3 | Active |
| risk-treatment-plan-risk002.md | Risk treatment plan for FHX-RISK-002 (Ransomware) | NIST SP 800-30 Sec. 3.3 | Active |
| risk-treatment-plan-risk004.md | Risk treatment plan for FHX-RISK-004 (API abuse) | NIST SP 800-30 Sec. 3.3 | Active |
| risk-treatment-plan-risk005.md | Risk treatment plan for FHX-RISK-005 (Supply chain) | NIST SP 800-30 Sec. 3.3 | Active |
| corrective-action-closure-log.md | Closed corrective actions with evidence of completion | NIST SP 800-30 | Current |
| poam-linkage-map.md | Mapping of corrective action items to FedRAMP POA&M entries | FedRAMP POA&M Template | Current |

---

## Corrective Action Register: Active Items

| CA ID | Linked Risk | Description | Treatment Type | Owner | Start Date | Target Completion | Milestones | Expected Residual Score | Status |
|---|---|---|---|---|---|---|---|---|---|
| CA-2025-001 | FHX-RISK-001 | PAM maturity enhancement: deploy CyberArk for all privileged access, implement session recording, eliminate shared credentials | Mitigate | DevOps Lead (T. Abrams) | Jan 15, 2025 | Sep 30, 2025 | M1: Requirements complete (Feb 28) M2: Vendor selection (Apr 15) M3: Pilot deployment (Jun 30) M4: Full rollout (Sep 30) | 8 (Moderate) | On Track |
| CA-2025-002 | FHX-RISK-002 | Enhanced backup and recovery: implement immutable backup vaulting in isolated S3 bucket, quarterly recovery testing | Mitigate | DevOps Lead (T. Abrams) | Feb 1, 2025 | Jun 30, 2025 | M1: Architecture design (Feb 28) M2: Implementation (Apr 15) M3: Testing complete (Jun 30) | 9 (Moderate) | Completed Q2 |
| CA-2025-003 | FHX-RISK-002 | Phishing simulation program: quarterly phishing campaigns, targeted training for high-risk roles | Mitigate | CISO (A. Torres) | Mar 1, 2025 | Dec 31, 2025 | Quarterly campaigns: Apr, Jul, Oct, Jan | 9 (Moderate) | On Track |
| CA-2025-004 | FHX-RISK-004 | API security enhancement: implement adaptive rate limiting, add API behavioral monitoring via Amazon API Gateway | Mitigate | DevOps Lead (T. Abrams) | Apr 1, 2025 | Aug 31, 2025 | M1: Rate limit tuning (May 31) M2: Behavioral monitoring (Aug 31) | 8 (Moderate) | On Track |
| CA-2025-005 | FHX-RISK-005 | SBOM implementation: integrate SBOM generation into CI/CD pipeline, establish vendor dependency review process | Mitigate | DevOps Lead (T. Abrams) | May 1, 2025 | Oct 31, 2025 | M1: Tool selection (Jun 30) M2: Pipeline integration (Aug 31) M3: Process documentation (Oct 31) | 8 (Moderate) | On Track |
| CA-2025-006 | FHX-RISK-007 | Breach detection automation: integrate SIEM rule set for breach indicators, automate HHS notification workflow | Mitigate | Privacy Officer (S. Voss) | Mar 15, 2025 | Sep 30, 2025 | M1: SIEM rules (May 31) M2: Workflow automation (Jul 31) M3: Tabletop exercise (Sep 30) | 8 (Moderate) | On Track |
| CA-2025-007 | FHX-RISK-008 | AWS Config conformance packs: implement FedRAMP-aligned conformance pack across all accounts | Mitigate | DevOps Lead (T. Abrams) | Jun 1, 2025 | Nov 30, 2025 | M1: Conformance pack design (Jul 31) M2: Pilot (Sep 30) M3: Full deployment (Nov 30) | 6 (Low) | On Track |
| CA-2025-008 | FHX-RISK-009 | IAM right-sizing project: review all IAM roles, apply least privilege, document individual accountability | Mitigate | DevOps Lead (T. Abrams) | Apr 15, 2025 | Sep 30, 2025 | M1: Role inventory (May 31) M2: Analysis and redesign (Jul 31) M3: Implementation (Sep 30) | 6 (Low) | On Track |
| CA-2025-009 | FHX-RISK-011 | Legacy agency API TLS enforcement: audit all agency-facing API endpoints, enforce TLS 1.3 minimum | Mitigate | DevOps Lead (T. Abrams) | May 15, 2025 | Aug 31, 2025 | M1: Endpoint inventory (Jun 15) M2: Enforcement implementation (Aug 31) | 8 (Moderate) | On Track |
| CA-2025-010 | FHX-RISK-012 | FTI integrity controls: annual FTI audit, implement hash-based integrity verification on FTI processing | Mitigate | ISSO (E. Njeze) | Jun 1, 2025 | Dec 31, 2025 | M1: FTI audit (Aug 31) M2: Integrity verification implementation (Dec 31) | 8 (Moderate) | On Track |

---

## Corrective Action Completion Summary

| Quarter | Actions Targeted | Actions Completed | Completion Rate | Notes |
|---|---|---|---|---|
| Q1 2025 | 3 | 2 | 67% | CA-2025-002 M1 delayed due to architecture review |
| Q2 2025 | 4 | 5 | 125% | CA-2025-002 completed ahead of Q3 schedule |
| Q3 2025 (projected) | 6 | TBD | TBD | CA-2025-001, 004, 006 have major milestones |
| Q4 2025 (projected) | 5 | TBD | TBD | CA-2025-005, 007, 010 targeting Q4 closure |

---

## Risk Treatment Plan: FHX-RISK-001 (PAM Enhancement)

**Linked Risk:** FHX-RISK-001 (Unauthorized PHI Access via Compromised Privileged Account)
**Current Risk Score:** 15 (High) — Likelihood 3, Impact 5
**Target Residual Score:** 8 (Moderate) — Likelihood 2, Impact 4 (regulatory multiplier reduced with controls in place)
**Treatment Type:** Mitigate

**Problem Statement:** FHX currently manages privileged access through a combination of AWS IAM roles, Active Directory groups, and manual access reviews. While MFA is enforced, the absence of a dedicated Privileged Access Management (PAM) solution creates gaps: there is no continuous session monitoring, shared service accounts exist in legacy subsystems, and access reviews are manual rather than automated.

**Treatment Approach:**
1. Deploy CyberArk Privileged Access Security to manage all privileged accounts across AWS GovCloud, Windows Server, and database tiers
2. Implement session recording for all privileged sessions with SIEM integration
3. Eliminate all shared service account credentials, replacing with individual accountability or machine identity tokens
4. Automate quarterly privileged access certification through the PAM tool

**Expected Control Improvements:**
- Likelihood reduced from 3 (Moderate) to 2 (Low): PAM tool detects and alerts on anomalous privileged activity; session recording provides forensic deterrence
- Residual risk score reduced from 15 (High) to 8 (Moderate)

**Owner:** DevOps Lead Trevor L. Abrams
**ISSO Oversight:** Enechi P.C. Njeze reviews milestone deliverables and updates risk register upon verified completion

---

## POA&M Linkage

Corrective actions that cannot be completed within the standard SLA are elevated to formal FedRAMP POA&M entries. The following table maps active corrective actions to POA&M entries where applicable.

| CA ID | POA&M ID | POA&M Title | Scheduled Completion | AO Acceptance |
|---|---|---|---|---|
| CA-2025-001 | FHX-POAM-2025-001 | PAM solution deployment | Sep 30, 2025 | Granted Jan 2025 |
| CA-2025-005 | FHX-POAM-2025-008 | SBOM implementation | Oct 31, 2025 | Granted May 2025 |
| CA-2025-010 | FHX-POAM-2025-015 | FTI integrity verification | Dec 31, 2025 | Pending AO review |

---

## Related Documents

- [Enterprise Risk Register](../risk-register/README.md)
- [Risk Scoring Model](../scoring-model/README.md)
- [Governance Workflows](../governance-workflows/README.md)
- [Stakeholder Reporting](../stakeholder-reporting/README.md)
- [Vulnerability Remediation](https://github.com/enechi-njeze/cloudvault-vuln-mgmt/blob/main/remediation-tracking/README.md)
- [FedRAMP POA&M](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/ssp-attachments/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
