# CloudVault Risk Governance

![Framework](https://img.shields.io/badge/Framework-NIST%20RMF%20%7C%20ISO%2031000-blue)
![Standard](https://img.shields.io/badge/Standard-NIST%20SP%20800--30-green)
![FedRAMP](https://img.shields.io/badge/FedRAMP-High-red)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Cert](https://img.shields.io/badge/ISSO-CGRC%20%7C%20CISA%20%7C%20CISM-blue)

**Enterprise risk register and governance program for CloudVault Federal Health Exchange (FHX)**

---

## System Overview

**System Name:** CloudVault Federal Health Exchange (FHX)
**System Owner:** Dr. Patricia Owens, Deputy CIO for Health Information Technology
**ISSO / ISSM:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**CISO:** Angela Torres
**Authorizing Official (AO):** Deputy Director Henry Kline
**Privacy Officer:** Sandra Voss
**Cloud Provider:** AWS GovCloud (us-gov-west-1, us-gov-east-1) — FedRAMP High
**3PAO:** ClearPath Security Assessors LLC
**ATO Status:** Active Authorization — FedRAMP High, FISMA High, HIPAA, SOX, PCI-DSS Level 1

CloudVault FHX is a cloud-hosted federal health information exchange platform serving 47 federal agencies. It manages health enrollment, benefits administration, and clinical data exchange for 890,000 or more patients. The platform processes Protected Health Information (PHI), Personally Identifiable Information (PII), Controlled Unclassified Information (CUI), Federal Tax Information (FTI), and Payment Card Industry (PCI) data, operating under the highest tier of federal security and privacy requirements.

---

## Risk Governance Program Overview

Risk governance at CloudVault FHX is not a single activity: it is a continuous, structured discipline that identifies threats to the system, evaluates their likelihood and impact, prioritizes mitigation, and reports risk posture to decision-makers at every level of the organization.

The FHX risk governance program is built on NIST SP 800-30 (Guide for Conducting Risk Assessments), NIST SP 800-39 (Managing Information Security Risk), and ISO 31000 (Risk Management Principles and Guidelines). These frameworks are complementary: NIST provides the federal mandate and methodology, while ISO 31000 adds enterprise governance structure that supports reporting to the board and executive leadership.

The program operates at three tiers, consistent with NIST SP 800-39:

**Tier 1 (Organization):** Enterprise-wide risk governance, managed by the CISO and reported to the Authorizing Official and System Owner. Covers strategic risk, governance policy, and program-level risk appetite decisions.

**Tier 2 (Mission/Business Process):** Risk affecting FHX business processes: health data exchange, benefits enrollment, federal agency connectivity, and cross-agency interoperability. Managed by the ISSO with CISO oversight.

**Tier 3 (Information System):** Technical system risk: vulnerabilities, threats, configuration weaknesses, and access control gaps. Managed by the ISSO and DevOps Lead, tracked in the risk register and POA&M.

---

## Repository Structure

```
cloudvault-risk-governance/
├── README.md                     # This file: program overview and navigation
├── risk-register/                # Enterprise risk register with scoring and status
├── scoring-model/                # Risk scoring methodology (likelihood x impact)
├── governance-workflows/         # Risk review, escalation, and acceptance workflows
├── stakeholder-reporting/        # Executive risk reports and AO briefing materials
├── corrective-actions/           # Risk treatment plans and corrective action tracking
└── diagrams/                     # Risk governance process flow and architecture diagrams
```

---

## Deliverables

| Document | Folder | Framework Reference | Status |
|---|---|---|---|
| Enterprise Risk Register | risk-register/ | NIST SP 800-30, Table E-4 | Current |
| Risk Scoring Methodology | scoring-model/ | NIST SP 800-30, Appendix I | Current |
| Likelihood x Impact Matrix | scoring-model/ | NIST SP 800-30, Table G-2 | Current |
| Risk Review Workflow | governance-workflows/ | NIST SP 800-39 Tier 2 | Current |
| Risk Escalation Procedure | governance-workflows/ | NIST SP 800-39 Tier 1 | Current |
| Risk Acceptance Policy | governance-workflows/ | FedRAMP Continuous Monitoring | Current |
| Executive Risk Dashboard | stakeholder-reporting/ | NIST SP 800-39 Tier 1 | Current |
| AO Risk Briefing Template | stakeholder-reporting/ | FedRAMP ATO Process | Current |
| Quarterly Risk Report | stakeholder-reporting/ | FISMA Annual Reporting | Current |
| Risk Treatment Plan | corrective-actions/ | NIST SP 800-30 Section 3.3 | Current |
| Corrective Action Register | corrective-actions/ | FedRAMP POA&M Template | Current |
| Risk Governance Architecture | diagrams/ | NIST SP 800-39 | Current |

---

## Framework and Standards Coverage

| Framework | Applicable Requirements | Coverage |
|---|---|---|
| NIST SP 800-30 | Risk assessment methodology, likelihood and impact definitions, risk scoring | Full |
| NIST SP 800-39 | Three-tier risk management, risk framing, risk response, risk monitoring | Full |
| NIST SP 800-37 (RMF) | RMF Step 4 (Assess), Step 5 (Authorize), Step 6 (Monitor) risk activities | Full |
| NIST SP 800-137 | Continuous monitoring and ongoing risk determination | Full |
| ISO 31000:2018 | Risk management principles, framework, and process | Aligned |
| FedRAMP Continuous Monitoring | Monthly ConMon risk reporting, POA&M management, AO risk acceptance | Full |
| FISMA | Annual risk assessment, FISMA reporting, OMB Circular A-130 | Full |
| HIPAA Security Rule | Risk analysis (164.308(a)(1)), risk management (164.308(a)(1)(ii)(B)) | Full |
| SOX ITGC | IT risk controls, management risk assessment, audit committee reporting | Aligned |

---

## Laws, Regulations, and Standards

| Law / Regulation / Standard | Applicability | Implementation |
|---|---|---|
| Federal Information Security Modernization Act (FISMA) 2014 | Mandatory for federal systems | Annual risk assessment, ISSO oversight |
| NIST SP 800-30 Rev. 1 | Risk assessment methodology | Risk register scoring, threat identification |
| NIST SP 800-39 | Risk management at three tiers | Tier 1-3 governance structure |
| OMB Circular A-130 | Federal information security and privacy | Risk governance integration with privacy |
| HIPAA Security Rule (45 CFR 164) | PHI risk analysis and management | Risk register PHI entries, HIPAA controls |
| FedRAMP Authorization Requirements | Cloud system risk acceptance | ATO, continuous monitoring |
| ISO 31000:2018 | Enterprise risk governance | Executive reporting framework |
| NIST CSF v2.0 | Govern, Identify, Protect, Detect, Respond, Recover | Risk governance mapped to CSF Govern function |

---

## Key Risk Governance Controls

| Control | Control Name | Requirement | Implementation |
|---|---|---|---|
| RA-1 | Risk Assessment Policy and Procedures | Annual policy review | FHX Risk Governance Policy v2.3 |
| RA-2 | Security Categorization | FIPS 199 High | System categorized as High, all three security objectives |
| RA-3 | Risk Assessment | Conducted at authorization and continuously | Annual formal assessment, monthly ConMon updates |
| RA-5 | Vulnerability Monitoring and Scanning | Continuous authenticated scanning | Tenable, Inspector, Qualys — see cloudvault-vuln-mgmt |
| RA-7 | Risk Response | Defined risk treatment options | Risk Treatment Plan in corrective-actions/ |
| CA-6 | Authorization | AO-maintained authorization | Active FedRAMP High ATO |
| CA-7 | Continuous Monitoring | Monthly ConMon reporting | ConMon reports submitted monthly to FedRAMP PMO |
| PM-9 | Risk Management Strategy | Organization-level strategy | Documented in scoring-model/ and governance-workflows/ |
| PM-28 | Risk Framing | Enterprise risk context | Three-tier framework documented in this repository |
| SI-2 | Flaw Remediation | Risk-based remediation prioritization | Integration with cloudvault-vuln-mgmt POA&M |

---

## Risk Appetite Statement

CloudVault FHX operates with a Low risk appetite for any threat category that could result in unauthorized disclosure of PHI, PII, or CUI; disruption of health data exchange services for federal agency partners; or non-compliance with FedRAMP, HIPAA, or FISMA requirements.

A Moderate risk appetite is applied to operational efficiency risks and technology modernization initiatives, provided that security and privacy controls are maintained at FedRAMP High baseline.

The risk appetite is reviewed annually by the CISO, System Owner, and AO, and documented in the Risk Management Strategy for FHX.

---

## Certifications and Competencies

| Certification | Issuing Body | Relevance to This Repository |
|---|---|---|
| CGRC (Certified in Governance, Risk and Compliance) | ISC2 | Core qualification: GRC program management, risk governance |
| CISA (Certified Information Systems Auditor) | ISACA | Risk-based audit methodology, risk register validation |
| CISM (Certified Information Security Manager) | ISACA | Risk management strategy, enterprise security governance |
| PMP (Project Management Professional) | PMI | Risk governance program management, corrective action tracking |
| PMI-RMP (Risk Management Professional) | PMI | Direct certification in risk management methodology |
| CompTIA Security+ SY0-701 | CompTIA | Security risk foundations, threat identification |
| CHP (Certified HIPAA Professional) | AAPC | HIPAA risk analysis requirements |
| CSCS (Certified Security Compliance Specialist) | NCSA | Compliance risk and control validation |
| CISSP (in progress) | ISC2 | Advanced risk and security management |

---

## Related Repositories

| Repository | Relationship |
|---|---|
| [cloudvault-fedramp-ato](https://github.com/enechi-njeze/cloudvault-fedramp-ato) | FedRAMP ATO documentation, SSP, and POA&M |
| [cloudvault-nist-rmf](https://github.com/enechi-njeze/cloudvault-nist-rmf) | NIST RMF implementation, all six steps |
| [cloudvault-vuln-mgmt](https://github.com/enechi-njeze/cloudvault-vuln-mgmt) | Vulnerability management and technical risk |
| [cloudvault-hipaa](https://github.com/enechi-njeze/cloudvault-hipaa) | HIPAA risk analysis and security safeguards |
| [cloudvault-master-controls](https://github.com/enechi-njeze/cloudvault-master-controls) | Cross-framework controls matrix and portfolio capstone |

---

## Portfolio Status

| Repository | Framework | Status |
|---|---|---|
| cloudvault-fedramp-ato | FedRAMP High | Complete |
| cloudvault-nist-rmf | NIST RMF | Complete |
| cloudvault-iso27001 | ISO 27001:2022 | Complete |
| cloudvault-hipaa | HIPAA Security Rule | Complete |
| cloudvault-sox-itgc | SOX ITGC | Complete |
| cloudvault-pci-dss | PCI-DSS v4.0 | Complete |
| cloudvault-privacy | Privacy / CCPA / GDPR | Complete |
| cloudvault-vuln-mgmt | NIST SP 800-40 | Complete |
| **cloudvault-risk-governance** | **NIST SP 800-30 / ISO 31000** | **Active** |
| cloudvault-master-controls | Cross-Framework Capstone | In Progress |

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
