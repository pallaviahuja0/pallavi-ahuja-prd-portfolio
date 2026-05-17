# PRD: Digital Lending & Payment Gateway Platform
**Organisation:** App-knit (Tech Startup) | Chandigarh, India  
**Product Manager:** Pallavi Ahuja  
**Role:** Technical Product Manager  
**Status:** ✅ Shipped  
**Timeline:** November 2021 – January 2024  
**Reporting To:** Founder / CTO  

---

## Table of Contents
1. [Problem Statement](#1-problem-statement)
2. [Goals & Objectives](#2-goals--objectives)
3. [Non-Goals](#3-non-goals)
4. [Background & Context](#4-background--context)
5. [Target Users & Personas](#5-target-users--personas)
6. [Scope](#6-scope)
7. [User Stories](#7-user-stories)
8. [Functional Requirements](#8-functional-requirements)
9. [Success Metrics & KPIs](#9-success-metrics--kpis)
10. [Product Roadmap](#10-product-roadmap)
11. [Risks & Mitigations](#11-risks--mitigations)
12. [Dependencies](#12-dependencies)
13. [Open Questions](#13-open-questions)

---

## 1. Problem Statement

Indian SMBs (small and medium businesses) seeking short-term working capital loans faced a frustratingly slow, paper-heavy lending process through traditional banks:
- Loan disbursement took **15–30 days** on average
- Documentation requirements were complex and non-digital
- SMB owners had **no visibility** into application status
- Payment collection from borrowers was manual (cheques, bank transfers)

Simultaneously, SMB merchants processing customer payments had **no affordable, integrated payment gateway** — they relied on fragmented tools (Razorpay standalone, UPI apps, cash) with no unified dashboard, reconciliation, or analytics.

**The core problem:** Indian SMBs needed a single digital platform to access working capital quickly and accept customer payments seamlessly — with full visibility into both lending status and payment flows.

---

## 2. Goals & Objectives

### Primary Goal
Build a mobile-first B2B digital lending and payment platform that reduces loan disbursement time from 30 days to under 72 hours, and provides SMB merchants with an integrated payment gateway and analytics dashboard.

### Business Goals
| Goal | Target | Timeline |
|------|--------|----------|
| Loan disbursement TAT | 30 days → <72 hours | Q2 2022 |
| Payment gateway onboarding | 500 SMB merchants in Year 1 | Q4 2022 |
| Sprint on-time delivery | 95%+ across all sprints | Ongoing |
| Post-launch support reduction | 45% reduction in support tickets | Q1 2023 |
| User adoption | 70%+ of onboarded users active in first 30 days | Q2 2022 |

### Product Goals
- Digital loan origination with e-KYC and document upload
- Automated credit decisioning (rule-based v1)
- Integrated payment gateway (UPI, cards, net banking via Razorpay/Paytm)
- Unified merchant dashboard: payments, settlements, analytics
- Self-service onboarding with knowledge base

---

## 3. Non-Goals

- ❌ Consumer (B2C) lending — SMB-only for v1
- ❌ Proprietary payment processing (uses third-party gateway APIs)
- ❌ Investment or wealth management products
- ❌ Cross-border payments (v1)
- ❌ Desktop-first experience (mobile-first priority)
- ❌ Full credit bureau integration (v1 uses rule-based scoring)

---

## 4. Background & Context

App-knit was a Chandigarh-based fintech startup building digital financial solutions for the Indian SMB segment — a market of 63 million+ businesses largely underserved by traditional banking infrastructure.

**Market opportunity:**
- 40% of Indian SMBs report difficulty accessing formal credit (RBI 2021 data)
- Digital payment adoption post-COVID accelerated: UPI transactions grew 90% YoY in 2021–22
- MSME lending gap estimated at ₹20–25 lakh crore (SIDBI report)

App-knit identified a product opportunity to build a **vertically integrated platform** combining lending origination and payment acceptance — creating a data flywheel where payment history informs creditworthiness for future lending.

---

## 5. Target Users & Personas

### Persona 1: The SMB Borrower
- **Name:** Ramesh, owner of a textile trading business in Ludhiana
- **Revenue:** ₹50L–2Cr annually
- **Pain:** Bank loan process takes weeks; needs ₹5–10L quickly for inventory purchase
- **Goal:** Get working capital in 72 hours with minimal paperwork
- **Tech Comfort:** Moderate — uses WhatsApp, basic banking apps

### Persona 2: The SMB Merchant
- **Name:** Priya, owner of a boutique in Chandigarh
- **Pain:** Uses 3 different apps to accept UPI, cards, and cash — no unified view of daily sales
- **Goal:** One dashboard to see all payments, settlements, and track revenue
- **Tech Comfort:** High — smartphone-first, uses Google Analytics for her e-commerce store

### Persona 3: The Platform Admin (Internal)
- **Name:** Ops team at App-knit
- **Pain:** Manual loan application review; no workflow tool for document verification
- **Goal:** Streamlined loan decisioning queue with document checklist and status tracking
- **Tech Comfort:** High

---

## 6. Scope

### In Scope — v1 (Q1–Q2 2022)
- Digital loan application flow (mobile & web)
- e-KYC: Aadhaar + PAN verification via third-party API
- Document upload: bank statements, GST returns, ITR
- Rule-based credit decisioning engine (v1)
- Loan status tracking dashboard (borrower-facing)
- Payment gateway integration: Razorpay, Paytm
- UPI, cards, net banking acceptance
- Merchant dashboard: daily settlements, transaction history
- Self-service onboarding + knowledge base

### In Scope — v2 (Q3–Q4 2022)
- Bureau integration (CIBIL / Experian)
- EMI repayment tracking and auto-debit (NACH)
- Advanced merchant analytics (top products, peak hours)
- Referral programme for merchant onboarding
- Multi-user access for merchant accounts

### Out of Scope
- Consumer B2C lending
- Cross-border payments
- Proprietary payment rail
- Investment products

---

## 7. User Stories

### Epic 1: Loan Origination
```
As an SMB owner,
I want to apply for a working capital loan digitally in under 15 minutes,
So that I don't have to visit a bank branch or submit physical documents.

Acceptance Criteria:
- Application form completable in <15 minutes on mobile
- Aadhaar + PAN e-KYC verified within 60 seconds via API
- Bank statements uploadable as PDF (last 6 months)
- Application submitted confirmation with reference number
- Status trackable in real-time via dashboard
```

```
As a platform admin,
I want a loan decisioning queue with all documents and a rule-based eligibility check,
So that I can review and approve/reject applications within 24 hours.

Acceptance Criteria:
- All uploaded documents visible in one view per application
- Rule engine auto-flags eligible vs. ineligible applications
- Approver can add notes and trigger disbursement in one click
- Applicant notified via SMS + in-app notification on decision
```

### Epic 2: Payment Gateway
```
As an SMB merchant,
I want to accept payments via UPI, cards, and net banking through a single integration,
So that I don't need multiple payment apps and can track all revenue in one place.

Acceptance Criteria:
- Single QR code accepts UPI from any app
- Payment link shareable via WhatsApp/SMS
- Card payments via POS SDK or hosted checkout
- Settlement T+1 to merchant bank account
- Real-time notification on every payment received
```

### Epic 3: Merchant Dashboard
```
As a merchant,
I want a dashboard showing today's sales, pending settlements, and transaction history,
So that I know my cash position at the end of each business day.

Acceptance Criteria:
- Dashboard loads in <2 seconds on 4G connection
- Shows: today's collections, pending settlement amount, last 30 days trend
- Filterable by payment method (UPI, card, net banking)
- CSV export of transaction history (any date range)
- Dispute/chargeback alerts with one-tap resolution flow
```

### Epic 4: Self-Service Onboarding
```
As a new merchant,
I want to onboard to the payment platform in under 30 minutes without agent assistance,
So that I can start accepting payments the same day I sign up.

Acceptance Criteria:
- Onboarding wizard: business details → KYC → bank account → go live
- Document upload: GST certificate, PAN, cancelled cheque
- Verification completed within 4 business hours
- In-app onboarding checklist showing progress
- Knowledge base accessible throughout (contextual help tooltips)
```

---

## 8. Functional Requirements

| ID | Requirement | Priority | Notes |
|----|-------------|----------|-------|
| FR-01 | Digital loan application form (mobile + web) | P0 | |
| FR-02 | e-KYC: Aadhaar + PAN verification | P0 | Third-party API |
| FR-03 | Document upload (PDF, images) | P0 | Bank statements, GST, ITR |
| FR-04 | Rule-based credit decisioning engine | P0 | Configurable rule sets |
| FR-05 | Loan status tracking dashboard | P0 | Real-time |
| FR-06 | Razorpay payment gateway integration | P0 | UPI, cards, net banking |
| FR-07 | Paytm payment gateway integration | P1 | |
| FR-08 | Merchant transaction dashboard | P0 | |
| FR-09 | T+1 settlement to merchant bank account | P0 | |
| FR-10 | SMS + in-app push notifications | P1 | |
| FR-11 | Self-service knowledge base | P1 | Reduces support load |
| FR-12 | CIBIL/Experian bureau integration | P2 | v2 |
| FR-13 | NACH auto-debit for EMI repayments | P2 | v2 |
| FR-14 | Advanced merchant analytics | P2 | v2 |

---

## 9. Success Metrics & KPIs

### Primary Metrics
| Metric | Baseline | Target | Result |
|--------|----------|--------|--------|
| Loan disbursement TAT | 30 days | <72 hours | ✅ Achieved |
| Sprint on-time delivery | ~70% | 98% | ✅ 98% across 8 sprints |
| Post-launch support tickets | Baseline | -45% | ✅ 45% reduction |
| Sprint goal completion | — | 92% | ✅ 92% achieved |

### Secondary Metrics
| Metric | Target |
|--------|--------|
| Merchant onboarding completion rate | >75% of started onboardings completed |
| Payment gateway uptime | 99.5%+ |
| App store rating | >4.2 stars |
| DAU/MAU ratio | >50% (sticky daily usage) |
| Knowledge base deflection rate | >40% of support queries self-served |

### Guardrail Metrics
- e-KYC API failure rate: <1%
- Payment gateway error rate: <0.5% of transactions
- Loan data accuracy: zero mismatched disbursement amounts

---

## 10. Product Roadmap

```
Q1 2022 — MVP Build
├── Loan application flow (mobile)
├── e-KYC integration
├── Document upload
├── Rule-based credit engine
└── Admin decisioning queue

Q2 2022 — Launch
├── Loan status dashboard
├── Razorpay payment gateway
├── Merchant dashboard v1
├── Self-service onboarding
├── Knowledge base
└── Beta launch: 50 pilot merchants

Q3 2022 — Scale
├── Paytm integration
├── Advanced merchant analytics
├── Referral programme
├── Multi-user merchant accounts
└── 500 merchant target

Q4 2022 — Lending v2
├── CIBIL/Experian bureau integration
├── NACH auto-debit (EMI)
├── Improved credit scoring model
└── Cross-sell: offer loans to active payment merchants

2023 — Growth
├── Cross-border payment exploration
├── BNPL (Buy Now Pay Later) module
├── API access for merchant integrations
└── B2B marketplace payment escrow
```

---

## 11. Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| e-KYC API downtime causing drop-offs | Medium | High | Fallback to manual KYC queue; SLA with provider |
| Low loan repayment rate (credit risk) | Medium | High | Conservative rule engine thresholds; small ticket sizes in v1 |
| Payment gateway settlement delays | Low | High | T+1 SLA contractually enforced; monitoring dashboard |
| Low merchant adoption post-onboarding | Medium | Medium | In-app activation nudges; onboarding concierge for first 30 days |
| Regulatory change (RBI digital lending norms) | Medium | High | Legal counsel on retainer; modular compliance architecture |
| Support overload at launch | High | Medium | Knowledge base + chatbot pre-built; dedicated launch support team |

---

## 12. Dependencies

| Dependency | Owner | Status |
|-----------|-------|--------|
| Aadhaar/PAN e-KYC API (Digio / Karza) | Engineering | ✅ Integrated |
| Razorpay payment gateway | Engineering | ✅ Integrated |
| Paytm payment gateway | Engineering | ✅ Integrated |
| NACH integration (v2) | Engineering | 🔄 Planned |
| CIBIL bureau API (v2) | Engineering | 🔄 Planned |
| RBI digital lending compliance review | Legal | ✅ Complete |
| Knowledge base content | Product + CS | ✅ Complete |
| UX design — onboarding wizard | Design | ✅ Complete |

---

## 13. Open Questions

| # | Question | Owner | Status |
|---|----------|-------|--------|
| 1 | Should the credit rule engine be configurable by ops without engineering? | PM + Eng | Resolved: Yes, via admin UI |
| 2 | What is the maximum loan ticket size for v1? | CEO + Risk | Resolved: ₹10L cap |
| 3 | Should the merchant app be native iOS/Android or React Native? | Engineering | Resolved: React Native (cross-platform) |
| 4 | How do we handle GST on platform fees? | Finance + Legal | Resolved: 18% GST on processing fee |

---

*PRD authored by Pallavi Ahuja | Technical Product Manager | App-knit*  
*Contact: pallavixahuja007@gmail.com | linkedin.com/in/pallaviahuja*
