# Enterprise Risk Register

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** NIST SP 800-30 Rev. 1, NIST SP 800-39
**Document ID:** FHX-RISK-REG-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault FHX
**Review Cycle:** Monthly update, Quarterly formal review, Annual comprehensive assessment
**Classification:** Internal Use Only — Sensitive Security Information

---

## Purpose

The Enterprise Risk Register is the authoritative record of all identified risks to the CloudVault FHX mission, operations, data assets, and stakeholders. It is not a static checklist: it is a living document reviewed monthly by the ISSO and quarterly by the CISO, System Owner, and Authorizing Official.

Every entry in the risk register represents a scenario where a threat source could exploit a vulnerability to cause harm to the system or the 890,000-plus patients and 47 federal agencies that depend on it. Each risk entry includes the threat, vulnerability, impact, likelihood, risk score, current controls, residual risk, and treatment decision.

The risk register directly feeds the FedRAMP continuous monitoring process (CA-7), the POA&M register, and the executive risk reporting delivered to AO Henry Kline each quarter.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| FHX-RISK-REG-001.md | This document (risk register overview and governance) | NIST SP 800-30 | Current |
| risk-register-current.md | Active risk register with all open risk entries | NIST SP 800-30 Table E-4 | Current |
| risk-register-archive-2024.md | Closed and accepted risks from FY 2024 | NIST SP 800-30 | Archived |
| threat-source-catalog.md | Identified threat sources applicable to FHX | NIST SP 800-30 Appendix D | Current |
| vulnerability-catalog.md | Known vulnerability categories linked to risk entries | NIST SP 800-30 Appendix E | Current |
| risk-assessment-report-fy2025.md | Annual formal risk assessment report FY 2025 | NIST SP 800-30 | Current |
| risk-acceptance-log.md | AO-approved risk acceptances with justification | FedRAMP ConMon | Current |

---

## Risk Register: Active Entries

The following table represents the FHX Enterprise Risk Register as of Q2 2025. Risk scores are calculated using the Likelihood x Impact matrix documented in the scoring-model/ folder. Scores range from 1 (Very Low) to 25 (Very High).

| Risk ID | Risk Description | Threat Source | Vulnerability | Likelihood | Impact | Risk Score | Controls In Place | Residual Risk | Treatment | Status | Owner |
|---|---|---|---|---|---|---|---|---|---|---|---|
| FHX-RISK-001 | Unauthorized access to PHI via compromised privileged account | Advanced Persistent Threat (APT) | Insufficient PAM controls, shared credentials | 3 (Moderate) | 5 (Very High) | 15 (High) | MFA, PAM tooling, privileged access reviews | 2 (Low) | Mitigate: PAM maturity enhancement | Open | ISSO |
| FHX-RISK-002 | Ransomware attack encrypting EHR databases | Cybercriminal | Unpatched OS vulnerability, phishing susceptibility | 3 (Moderate) | 5 (Very High) | 15 (High) | EDR, backup isolation, patch management | 3 (Low-Moderate) | Mitigate: Enhanced backup testing, phishing simulation | Open | DevOps Lead |
| FHX-RISK-003 | Data exfiltration by malicious insider | Insider Threat | Insufficient DLP coverage on S3 bucket exports | 2 (Low) | 5 (Very High) | 10 (Moderate) | UEBA, access logging, DLP rules | 2 (Low) | Mitigate: Expand DLP rule set, quarterly access review | Open | CISO |
| FHX-RISK-004 | API abuse allowing mass enumeration of patient records | External Attacker | Insufficient API rate limiting, weak authentication | 3 (Moderate) | 4 (High) | 12 (Moderate-High) | API Gateway throttling, OAuth 2.0 | 2 (Low) | Mitigate: API security testing, rate limit tuning | Open | DevOps Lead |
| FHX-RISK-005 | Supply chain compromise via third-party software dependency | Nation-State / APT | Insufficient software composition analysis | 2 (Low) | 5 (Very High) | 10 (Moderate) | SCA scanning in CI/CD, vendor vetting | 2 (Low) | Mitigate: SBOM implementation, vendor risk program | Open | DevOps Lead |
| FHX-RISK-006 | Loss of availability due to DDoS targeting health exchange endpoints | Hacktivist / Competitor | Insufficient DDoS mitigation capacity | 2 (Low) | 4 (High) | 8 (Moderate) | AWS Shield Advanced, CloudFront WAF | 1 (Very Low) | Accept: Current controls adequate for risk level | Accepted | ISSO |
| FHX-RISK-007 | Regulatory non-compliance due to HIPAA breach notification failure | Compliance Risk | Manual breach detection process with gap potential | 2 (Low) | 5 (Very High) | 10 (Moderate) | Breach response plan, SIEM alerting | 2 (Low) | Mitigate: Automate breach detection, tabletop exercise | Open | Privacy Officer |
| FHX-RISK-008 | Configuration drift creating unauthorized access paths | Insider / Negligence | No continuous configuration baseline enforcement | 3 (Moderate) | 3 (Moderate) | 9 (Moderate) | AWS Config, SCPs, quarterly config reviews | 2 (Low) | Mitigate: Implement Config conformance packs | Open | DevOps Lead |
| FHX-RISK-009 | Privilege escalation via misconfigured IAM role | External Attacker | Over-permissioned IAM roles in legacy environments | 2 (Low) | 4 (High) | 8 (Moderate) | IAM Access Analyzer, least privilege review | 2 (Low) | Mitigate: IAM right-sizing project Q3 2025 | Open | DevOps Lead |
| FHX-RISK-010 | Loss of FedRAMP authorization due to continuous monitoring gaps | Compliance Risk | Insufficient ConMon documentation or scan coverage | 1 (Very Low) | 5 (Very High) | 5 (Low-Moderate) | Monthly ConMon reporting, scan coverage tracking | 1 (Very Low) | Monitor: Maintain current ConMon maturity | Monitoring | ISSO |
| FHX-RISK-011 | PHI disclosure through unencrypted data transfer between federal agencies | External Attacker / Error | Legacy agency connectivity without TLS enforcement | 2 (Low) | 5 (Very High) | 10 (Moderate) | TLS 1.3 enforcement on FHX endpoints | 2 (Low) | Mitigate: Enforce TLS on legacy agency APIs | Open | DevOps Lead |
| FHX-RISK-012 | Unauthorized modification of financial transactions (FTI data) | Insider / External | Insufficient integrity controls on FTI processing | 2 (Low) | 5 (Very High) | 10 (Moderate) | RBAC, audit logging, IRS FTI controls | 2 (Low) | Mitigate: Annual FTI audit, integrity verification | Open | ISSO |

---

## Risk Summary Statistics (Q2 2025)

| Risk Level | Count | Percentage |
|---|---|---|
| Very High (20-25) | 0 | 0% |
| High (15-19) | 2 | 17% |
| Moderate (8-14) | 8 | 67% |
| Low (3-7) | 2 | 17% |
| Very Low (1-2) | 0 | 0% |
| Total | 12 | 100% |

**Program Status:** The FHX risk posture is Moderate overall. No Very High risks are present. The two High risks (FHX-RISK-001 and FHX-RISK-002) have active treatment plans with scheduled completion dates. Residual risk across all entries is Low or Very Low, indicating that existing controls are effective in reducing inherent risk.

---

## Risk Treatment Categories

The FHX risk governance program uses four risk treatment options, consistent with NIST SP 800-39 and ISO 31000.

**Mitigate:** Implement or enhance controls to reduce likelihood or impact. This is the default treatment for High and Moderate risks. Mitigation actions are tracked in corrective-actions/ with assigned owners and due dates.

**Accept:** Accept the residual risk as within the organization's risk appetite. Requires written AO acceptance for any risk scored Moderate or above. Documented in the risk-acceptance-log.md.

**Transfer:** Shift risk to a third party through contractual means (e.g., cyber insurance, vendor SLAs). Limited applicability for federal systems due to FISMA accountability requirements.

**Avoid:** Eliminate the activity or condition that creates the risk. Applied when the risk cannot be adequately mitigated and the activity is discretionary.

---

## Risk Register Maintenance Schedule

| Activity | Frequency | Owner | Deliverable |
|---|---|---|---|
| New risk identification review | Monthly | ISSO | Updated risk register |
| Residual risk reassessment | Quarterly | ISSO, DevOps Lead | Updated risk scores |
| AO risk briefing | Quarterly | ISSO | Executive risk summary |
| Formal risk assessment | Annually | ISSO, 3PAO (ClearPath) | Risk Assessment Report |
| Risk appetite review | Annually | CISO, AO, System Owner | Updated Risk Management Strategy |
| Risk acceptance log review | Annually | AO Henry Kline | Renewed or closed acceptances |

---

## Related Documents

- [Risk Scoring Model](../scoring-model/README.md)
- [Governance Workflows](../governance-workflows/README.md)
- [Corrective Actions](../corrective-actions/README.md)
- [Stakeholder Reporting](../stakeholder-reporting/README.md)
- [Vulnerability Management](https://github.com/enechi-njeze/cloudvault-vuln-mgmt/blob/main/README.md)
- [FedRAMP ATO](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
