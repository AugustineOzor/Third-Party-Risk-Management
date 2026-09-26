# ⚠️ Risk Assessment

> 4 vendor-related risks identified during due diligence for **PaySecure Processing Inc.**, scored by likelihood × impact.

| # | Title | Category | Status | Risk Score |
|---|---|---|---|---|
| 1 | Cardholder Data Exposure via Vendor Access | Data Protection | ![Open](https://img.shields.io/badge/status-Open-d73a49) | 15 (3 × 5) — Critical |
| 2 | Inadequate Vendor Employee Access Controls | Access Control | ![In Progress](https://img.shields.io/badge/status-In%20Progress-dbab09) | 12 (3 × 4) — High |
| 3 | Regulatory Non-Compliance (PCI DSS / OCC) | Compliance | ![Open](https://img.shields.io/badge/status-Open-d73a49) | 10 (2 × 5) — High |
| 4 | Service Availability / Business Continuity Risk | Availability | ![Open](https://img.shields.io/badge/status-Open-d73a49) | 12 (3 × 4) — High |

## 1. Cardholder Data Exposure via Vendor Access

**Category:** Data Protection  
**Status:** ![Open](https://img.shields.io/badge/status-Open-d73a49)  
**Likelihood:** 3/5 &nbsp;·&nbsp; **Impact:** 5/5 &nbsp;·&nbsp; **Risk Score:** 15 (3 × 5) — Critical  
**Owner:** Augustine Ozor

**Description**  
PaySecure has direct access to FinSecure's cardholder data environment (CDE) for transaction processing. Unauthorized access, misconfiguration, or a breach at the vendor could expose cardholder data.

**Decision Rationale**  
Likelihood rated Possible (3) because the vendor holds an active SOC 2 Type II report showing operating controls, but noted access-review exceptions increase uncertainty. Impact rated Severe (5) because any cardholder data exposure through a Level 1 service provider triggers PCI DSS and OCC regulatory consequences and significant reputational damage.

---

## 2. Inadequate Vendor Employee Access Controls

**Category:** Access Control  
**Status:** ![In Progress](https://img.shields.io/badge/status-In%20Progress-dbab09)  
**Likelihood:** 3/5 &nbsp;·&nbsp; **Impact:** 4/5 &nbsp;·&nbsp; **Risk Score:** 12 (3 × 4) — High  
**Owner:** Augustine Ozor

**Description**  
PaySecure employees and contractors with access to FinSecure's cardholder data environment may not be governed by sufficiently granular role-based access controls, timely deprovisioning, or background screening, increasing the risk of insider misuse or unauthorized access to cardholder data.

**Decision Rationale**  
Likelihood rated Possible (3) because insider access issues are a recognized risk across payment processors and the vendor's SOC 2 report already noted access-review exceptions, suggesting access governance is not fully mature. Impact rated Major (4) because insider misuse of CDE access could result in direct cardholder data compromise, though it is somewhat narrower in scope than a full external breach.

---

## 3. Regulatory Non-Compliance (PCI DSS / OCC)

**Category:** Compliance  
**Status:** ![Open](https://img.shields.io/badge/status-Open-d73a49)  
**Likelihood:** 2/5 &nbsp;·&nbsp; **Impact:** 5/5 &nbsp;·&nbsp; **Risk Score:** 10 (2 × 5) — High  
**Owner:** Augustine Ozor

**Description**  
Failure of the vendor to maintain PCI DSS compliance or to meet OCC third-party risk management expectations could expose FinSecure to regulatory findings, fines, or restrictions.

**Decision Rationale**  
Likelihood rated Unlikely (2) given the vendor holds current attestations and is a Level 1 service provider subject to annual assessment. Impact rated Severe (5) because as the regulated entity, FinSecure — not the vendor — bears ultimate regulatory accountability for a payment processor's non-compliance under OCC guidance.

---

## 4. Service Availability / Business Continuity Risk

**Category:** Availability  
**Status:** ![Open](https://img.shields.io/badge/status-Open-d73a49)  
**Likelihood:** 3/5 &nbsp;·&nbsp; **Impact:** 4/5 &nbsp;·&nbsp; **Risk Score:** 12 (3 × 4) — High  
**Owner:** Augustine Ozor

**Description**  
An outage, ransomware event, or disaster at PaySecure could disrupt FinSecure's ability to process customer payment transactions.

**Decision Rationale**  
Likelihood rated Possible (3) reflecting the general frequency of availability incidents among payment processors industry-wide. Impact rated Major (4) because a processing outage directly affects customer-facing banking services and revenue, though FinSecure's own contingency/backup processing arrangements would partially mitigate full-scale impact.

---


---

<div align="center">

[← Vendor Profile](01-vendor-profile.md)&nbsp;&nbsp;|&nbsp;&nbsp;[🏠 Home](README.md)&nbsp;&nbsp;|&nbsp;&nbsp;[Control Verification →](03-control-verification.md)

</div>
