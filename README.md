<div align="center">


# Third-Party Risk Management — Payment Processor Due Diligence

<img width="3200" height="840" alt="banner" src="https://github.com/user-attachments/assets/361d9b59-978b-45e4-b80b-3c506dcdb97f" />

![Framework](https://img.shields.io/badge/frameworks-PCI%20DSS%20%7C%20SOC%202-1f4e78)
![Status](https://img.shields.io/badge/status-in%20progress-dbab09)
![Sector](https://img.shields.io/badge/sector-financial%20services-333333)

</div>

## About this repository

FinSecure Banking is integrating a third-party payment processor with direct access to its cardholder data environment (CDE). As the payment processor is a **PCI DSS Level 1 service provider** and FinSecure is subject to **OCC third-party risk management guidance**, this engagement documents a full vendor due-diligence review conducted as TPRM Lead — from vendor intake through risk scoring, control verification against the vendor's **SOC 2 Type II** attestation, and the resulting findings log.

This repo is a structured, portfolio-style write-up of that assessment: a realistic (fictional) case study demonstrating a practical TPRM workflow for a regulated financial institution.


## How to read this

Each page links to the next via the navigation bar at the bottom, so you can walk through the full assessment in order — Vendor Profile → Risk Assessment → Control Verification → Issues Log — the same sequence followed during the actual review.

## Methodology at a glance

- **Risk scoring:** Likelihood (1–5) × Impact (1–5), banded Low / Medium / High / Critical
- **Control effectiveness:** Effective, Partially Effective, Ineffective, or Not Tested — each justified with a decision rationale, not just a label
- **Standards referenced:** PCI DSS (exact sub-requirement references, e.g. `3.4`, `8.3`, `11.3`), SOC 2 Trust Services Criteria (e.g. `CC9.2`)

---

