# 🛡️ Control Verification

> 6 controls verified against the vendor's SOC 2 report and PCI DSS attestation evidence.

| # | Control | Framework | Reference | Effectiveness | Frequency |
|---|---|---|---|---|---|
| 1 | Encryption of Cardholder Data (Transit & At Rest) | PCI DSS | `3.4` | ![Effective](https://img.shields.io/badge/status-Effective-28a745) | Continuous |
| 2 | CDE Network Segmentation | PCI DSS | `1.3` | ![Effective](https://img.shields.io/badge/status-Effective-28a745) | Quarterly |
| 3 | Access Control & Multi-Factor Authentication | PCI DSS | `8.3` | ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) | Continuous |
| 4 | Vulnerability Management & Penetration Testing | PCI DSS | `11.3` | ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) | Annual |
| 5 | Incident Response & Breach Notification | PCI DSS | `12.10` | ![Effective](https://img.shields.io/badge/status-Effective-28a745) | Continuous |
| 6 | Sub-Processor / Fourth-Party Risk Management | SOC 2 | `CC9.2` | ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) | Annual |

## 1. Encryption of Cardholder Data (Transit & At Rest)

**Framework:** PCI DSS `3.4` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Effective](https://img.shields.io/badge/status-Effective-28a745) &nbsp;·&nbsp; **Owner:** Augustine Ozor

**Description**  
Works by encrypting cardholder data with TLS in transit and strong encryption with managed keys at rest. Implemented across PaySecure's processing and storage systems per their documented encryption standard. Tested via review of the vendor's SOC 2 report control testing and their encryption standard summary provided during due diligence.

**Decision Rationale**  
Rated Effective because SOC 2 Type II testing showed no exceptions for encryption controls, and the vendor's documented encryption standard aligns with PCI DSS Requirement 3/4 expectations for cardholder data protection.

---

## 2. CDE Network Segmentation

**Framework:** PCI DSS `1.3` &nbsp;·&nbsp; **Frequency:** Quarterly  
**Effectiveness:** ![Effective](https://img.shields.io/badge/status-Effective-28a745) &nbsp;·&nbsp; **Owner:** Augustine Ozor

**Description**  
Works by isolating the cardholder data environment from the vendor's broader corporate network through firewalls and access control lists, limiting the systems that can reach cardholder data. Implemented as part of PaySecure's PCI DSS-scoped network architecture. Tested through the vendor's periodic segmentation testing, reviewed via their PCI DSS Attestation of Compliance (AOC).

**Decision Rationale**  
Rated Effective because the AOC confirms segmentation testing was performed within the last 12 months with no material findings, indicating the CDE boundary is being actively validated rather than assumed.

---

## 3. Access Control & Multi-Factor Authentication

**Framework:** PCI DSS `8.3` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) &nbsp;·&nbsp; **Owner:** Augustine Ozor

**Description**  
Works by restricting cardholder data access to authorized personnel on a least-privilege basis and requiring MFA for access to CDE systems. Implemented through the vendor's identity and access management platform. Tested via SOC 2 report testing of access provisioning, deprovisioning, and periodic access reviews.

**Decision Rationale**  
Rated Partially Effective because while MFA enforcement tested with no exceptions, the SOC 2 report noted exceptions in periodic user access review testing, meaning stale or excessive access may not be reliably caught, which is a related open issue for this vendor.

---

## 4. Vulnerability Management & Penetration Testing

**Framework:** PCI DSS `11.3` &nbsp;·&nbsp; **Frequency:** Annual  
**Effectiveness:** ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) &nbsp;·&nbsp; **Owner:** Augustine Ozor

**Description**  
Works by identifying and remediating vulnerabilities in systems supporting the CDE through vulnerability scanning and penetration testing. Implemented via the vendor's internal security testing program ahead of each PCI DSS assessment cycle. Tested by reviewing the vendor's most recent penetration test executive summary provided during due diligence.

**Decision Rationale**  
Rated Partially Effective because the penetration test evidence supplied is over 12 months old, exceeding the PCI DSS annual testing expectation, so current-state assurance over unpatched vulnerabilities cannot be confirmed.

---

## 5. Incident Response & Breach Notification

**Framework:** PCI DSS `12.10` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Effective](https://img.shields.io/badge/status-Effective-28a745) &nbsp;·&nbsp; **Owner:** Augustine Ozor

**Description**  
Works by defining how the vendor detects, responds to, and communicates security incidents affecting shared systems or data. Implemented through the vendor's documented incident response policy and a contractual breach notification clause. Tested by reviewing the incident response policy summary and confirming the notification timeline in the signed contract.

**Decision Rationale**  
Rated Effective because the contract specifies a 24-hour breach notification requirement to FinSecure, consistent with regulatory expectations, and the vendor's incident response policy addresses detection, escalation, and communication steps.

---

## 6. Sub-Processor / Fourth-Party Risk Management

**Framework:** SOC 2 `CC9.2` &nbsp;·&nbsp; **Frequency:** Annual  
**Effectiveness:** ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) &nbsp;·&nbsp; **Owner:** Augustine Ozor

**Description**  
Intended to work by requiring the vendor to assess and monitor the security posture of its own sub-processors involved in payment processing, and to disclose material changes to FinSecure. Meant to be implemented through a documented fourth-party due-diligence process and an up-to-date sub-processor list. Meant to be tested by reviewing that sub-processor list and due-diligence evidence during onboarding and annual reassessment.

**Decision Rationale**  
Rated Not Tested because the vendor provided only a partial sub-processor list and no documented fourth-party due-diligence process, so the control's actual design and operation could not be evaluated during this assessment.

---


---

<div align="center">

[← Risk Assessment](02-risk-assessment.md)&nbsp;&nbsp;|&nbsp;&nbsp;[🏠 Home](README.md)&nbsp;&nbsp;|&nbsp;&nbsp;[Issues Log →](04-issues-log.md)

</div>
