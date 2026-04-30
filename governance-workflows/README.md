# Risk Governance Workflows

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** NIST SP 800-39, FedRAMP Continuous Monitoring Strategy Guide
**Document ID:** FHX-RISK-GOV-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault FHX
**Review Cycle:** Annual (or upon significant organizational change)
**Classification:** Internal Use Only

---

## Purpose

This folder contains the workflows that govern how risk is identified, reviewed, escalated, accepted, and monitored at CloudVault FHX. A well-documented governance workflow is what separates a mature GRC program from a paper exercise. Without defined processes, risk decisions are inconsistent, escalation paths are unclear, and auditors cannot verify that governance actually occurred.

The workflows documented here align with NIST SP 800-39 and the three-tier risk management framework. They also satisfy FedRAMP continuous monitoring requirements for documented risk acceptance and AO engagement processes.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| FHX-RISK-GOV-001.md | This document (workflow overview) | NIST SP 800-39 | Current |
| risk-review-procedure.md | Monthly and quarterly risk register review procedure | NIST SP 800-39 Tier 2 | Current |
| risk-escalation-procedure.md | Escalation paths for Very High and High risks | NIST SP 800-39 Tier 1 | Current |
| risk-acceptance-procedure.md | AO risk acceptance process and documentation requirements | FedRAMP ConMon Guide | Current |
| risk-transfer-procedure.md | Third-party risk transfer process (vendor SLAs, cyber insurance) | NIST SP 800-39 | Current |
| risk-governance-charter.md | Charter defining roles, responsibilities, and authority for FHX risk governance | NIST SP 800-39 Tier 1 | Current |
| riskcomm-minutes-template.md | Template for risk governance committee meeting minutes | FHX Risk Governance Charter | Current |

---

## Risk Governance Committee

FHX risk governance is overseen by the Risk Governance Committee (RGC), which meets quarterly and on an ad hoc basis for escalated risks. The RGC is the primary governance body for risk decisions above the ISSO level.

| Role | Member | Responsibility |
|---|---|---|
| Chair | Angela Torres, CISO | Oversee risk governance program, escalate to AO |
| Authorizing Official | Deputy Director Henry Kline | Final risk acceptance authority, ATO maintenance |
| System Owner | Dr. Patricia Owens | Provide mission context for risk prioritization |
| ISSO / ISSM | Enechi P.C. Njeze | Present risk register, recommend treatment, track closures |
| Privacy Officer | Sandra Voss | Review PHI and PII risk implications |
| DevOps Lead | Trevor L. Abrams | Technical risk input, remediation feasibility |
| 3PAO Representative | ClearPath Security Assessors LLC | Annual assessment input, control effectiveness |

---

## Monthly Risk Register Review Workflow

The ISSO conducts a monthly risk register review as part of the FedRAMP continuous monitoring cycle. This review updates risk scores based on new threat intelligence, changes to controls, and new vulnerability data.

**Step 1: Gather Updated Inputs (Day 1-5 of month)**
- Pull latest vulnerability scan results from cloudvault-vuln-mgmt
- Review CISA Known Exploited Vulnerabilities (KEV) catalog for new entries affecting FHX
- Review FS-ISAC threat intelligence reports
- Check POA&M register for items past due or approaching due dates

**Step 2: Update Risk Scores (Day 5-8 of month)**
- For each open risk entry, assess whether likelihood or impact has changed based on new inputs
- Apply contextual adjustments per the scoring-model/ methodology
- Flag any risk that has increased by 1 or more tier for CISO notification

**Step 3: Identify New Risks (Day 8-10 of month)**
- Review recent system changes (DevOps change log) for new risk scenarios
- Review privacy officer's incident log for near-miss events
- Document any new risk entries with full scoring

**Step 4: Update Treatment Status (Day 10-12 of month)**
- Check corrective-actions/ register for completed treatments
- Close risk entries where treatment is verified complete
- Update scheduled completion dates for items where milestones have slipped

**Step 5: Draft Monthly Risk Summary (Day 12-15 of month)**
- Prepare monthly risk summary for inclusion in ConMon report
- Highlight any score changes, new risks, or closed risks
- Submit to CISO for review

---

## Quarterly Risk Governance Committee Review

The RGC meets quarterly to review the full risk register, approve risk acceptance decisions, and provide strategic direction on risk treatment priorities.

**Agenda Template:**

1. Risk Register Summary (ISSO, 15 minutes): Present current risk counts by tier, score changes since last quarter, and treatment progress
2. High and Very High Risk Review (ISSO, CISO, 20 minutes): Detailed discussion of each High or Very High risk, treatment plan status, and AO awareness items
3. New Risk Presentations (ISSO, 15 minutes): Present any new risks identified since last meeting
4. Risk Acceptance Decisions (AO, CISO, 15 minutes): AO reviews and approves or denies any pending risk acceptance requests
5. Treatment Priority Alignment (System Owner, DevOps Lead, 10 minutes): Prioritize remediation resources across competing treatment plans
6. Next Quarter Outlook (ISSO, 10 minutes): Upcoming risk activities, assessments, and expected changes

**Quorum Requirement:** ISSO, CISO, and AO (or AO designee) must be present. Decisions cannot be made without quorum.

---

## Risk Escalation Procedure

Not all risks follow the normal review cycle. The escalation procedure defines when and how risks are elevated above the ISSO for immediate attention.

**Trigger 1: New Very High Risk Identified**
- ISSO notifies CISO within 4 business hours of identification
- ISSO notifies System Owner within 24 hours
- AO notification within 24 hours if risk remains Very High after initial control assessment
- Emergency RGC meeting convened within 5 business days
- Out-of-cycle ConMon report may be required

**Trigger 2: Risk Score Increases to High or Very High**
- ISSO notifies CISO within 24 hours
- Updated risk entry prepared with new scoring rationale
- Risk escalated to next quarterly RGC meeting with priority agenda item
- If timeline to next RGC is more than 30 days: ad hoc notification to AO

**Trigger 3: Critical Vulnerability with No Available Patch**
- ISSO escalates to DevOps Lead and CISO immediately
- Compensating control options developed within 48 hours
- Risk scored under NIST SP 800-30 framework
- AO notified if compensating control does not reduce risk below High
- POA&M entry created within 5 business days

**Trigger 4: SLA Breach on High Risk Treatment**
- ISSO notifies CISO immediately upon breach
- Updated treatment plan with revised completion date submitted to AO within 5 business days
- Risk acceptance required from AO if treatment completion will exceed 30 days beyond original SLA

---

## Risk Acceptance Procedure

Risk acceptance is the formal process by which the AO agrees to operate the system despite a known residual risk. FedRAMP requires documented AO risk acceptance for any risk that cannot be fully remediated within the standard SLA window.

**Step 1: ISSO Prepares Risk Acceptance Package**
The package includes: risk entry from the risk register, inherent and residual risk scores, description of existing controls and why they are insufficient for full mitigation, proposed compensating controls (if any), business justification for acceptance, and recommended acceptance period (not to exceed 1 year without re-review).

**Step 2: CISO Reviews Package**
CISO reviews for completeness and reasonableness. CISO may return the package for additional analysis or forward to AO with CISO recommendation (accept, reject, or accept with conditions).

**Step 3: AO Decision**
AO reviews the package and CISO recommendation. AO may accept the risk, reject it (requiring continued treatment), or accept it with conditions (such as mandatory compensating controls or a shorter review period).

**Step 4: Documentation and Tracking**
Accepted risks are recorded in the risk-acceptance-log.md with AO signature date, acceptance period, conditions, and next review date. Accepted risks appear in the monthly ConMon report as accepted with the AO acceptance date.

**Step 5: Periodic Re-Review**
All accepted risks are reviewed at the quarterly RGC meeting. Acceptances approaching expiration are presented to the AO for renewal or closure.

---

## Risk Monitoring Workflow

Accepted and mitigated risks remain in active monitoring status until the underlying vulnerability is fully remediated or the AO determines that the risk is no longer relevant.

| Monitoring Activity | Frequency | Responsibility | Output |
|---|---|---|---|
| Threat intelligence review | Monthly | ISSO | Updated likelihood scores where applicable |
| Control effectiveness validation | Quarterly | ISSO, DevOps Lead | Updated residual risk scores |
| Risk acceptance expiration review | Quarterly | ISSO, AO | Renewed or closed acceptances |
| System change impact assessment | Per change | ISSO, Change Advisory Board | New or modified risk entries |
| Annual risk assessment | Annually | ISSO, 3PAO (ClearPath) | Updated Risk Assessment Report |

---

## Related Documents

- [Enterprise Risk Register](../risk-register/README.md)
- [Risk Scoring Model](../scoring-model/README.md)
- [Stakeholder Reporting](../stakeholder-reporting/README.md)
- [Corrective Actions](../corrective-actions/README.md)
- [FedRAMP ConMon](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/step6-monitor/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
