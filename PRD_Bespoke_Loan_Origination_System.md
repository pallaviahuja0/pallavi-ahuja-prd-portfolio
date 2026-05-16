# PRD: Loan Origination System (LOS) — Banking Client
**Organisation:** Bespoke Technologies | Chandigarh, India  
**Product Manager:** Pallavi Ahuja  
**Role:** Project Manager / Associate Project Manager  
**Status:** ✅ Shipped (3 major releases)  
**Timeline:** January 2018 – October 2021  
**Client:** Confidential Banking Client  

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

A mid-sized bank's loan origination process was entirely manual and paper-based — creating significant operational inefficiencies, poor customer experience, and compliance risk:

- **Loan officers** spent 60%+ of their time on data entry and document collection
- **Customers** waited 10–21 days for loan decisions on straightforward applications
- **Operations teams** had no centralised system to track application status across branches
- **Compliance teams** struggled with audit trails — paper files were incomplete, lost, or inaccessible
- **Approval workflows** required physical sign-off from multiple stakeholders across different branch locations

The bank was losing retail loan business to digital-first competitors who offered 48-hour approvals. Internally, error rates in manual data entry were causing costly rework and occasional regulatory reporting inaccuracies.

**The core problem:** The bank needed a digital, end-to-end Loan Origination System (LOS) that could automate data collection, workflow routing, document management, and approval processes — reducing TAT, improving compliance, and enabling scale.

---

## 2. Goals & Objectives

### Primary Goal
Deliver a configurable, web-based Loan Origination System that reduces loan processing TAT from 21 days to under 3 days for personal and SME loans, with full audit trails and regulatory compliance.

### Business Goals
| Goal | Target | Timeline |
|------|--------|----------|
| Loan processing TAT | 21 days → <3 days | Release 2 |
| Data entry error rate | ~8% → <0.5% | Release 1 |
| Loan officer productivity | +40% applications processed per officer/day | Release 2 |
| Audit readiness | 100% digital audit trail for all applications | Release 1 |
| System uptime | 99.5%+ during banking hours | Ongoing |

### Product Goals
- Digital loan application capture (all loan types: personal, home, SME)
- Automated document checklist and upload verification
- Rule-based eligibility and preliminary credit assessment
- Configurable multi-level approval workflow (branch → regional → HO)
- Integration with core banking system (CBS) for disbursement
- Compliance reporting and audit log

---

## 3. Non-Goals

- ❌ Consumer-facing mobile app (bank staff/officer-facing system only, v1)
- ❌ Proprietary credit scoring model (uses existing bureau integration)
- ❌ Insurance or investment product origination
- ❌ International or cross-currency loans
- ❌ Real-time CBS integration in v1 (batch sync for v1, real-time in v2)
- ❌ Self-service customer portal (deferred to v3)

---

## 4. Background & Context

Bespoke Technologies was engaged by the banking client to build a custom LOS to replace their legacy paper-based workflow. The engagement was structured in 3 releases over 3 years:

- **Release 1 (2018):** Core loan capture, document management, basic workflow
- **Release 2 (2019):** Automated credit assessment, multi-level approvals, CBS integration
- **Release 3 (2021):** Advanced reporting, regulatory submission automation, branch performance dashboards

The project involved close collaboration with the bank's operations, IT, compliance, and retail banking teams — with UAT conducted jointly with branch operations staff before each release.

**Regulatory context:** The system had to comply with RBI guidelines on digital lending, data localisation requirements, and NPCI standards for disbursement via NEFT/RTGS.

---

## 5. Target Users & Personas

### Persona 1: The Loan Officer (Branch Level)
- **Name:** Sunita, Loan Officer at a Delhi branch
- **Responsibility:** Captures loan applications, collects documents, does preliminary assessment
- **Pain:** Fills 8-page paper forms; re-enters data multiple times; loses track of application status
- **Goal:** Capture a complete loan application digitally in one session; track status without calling HO
- **Tech Comfort:** Moderate — familiar with basic banking software

### Persona 2: The Branch Credit Manager
- **Name:** Vikram, Credit Manager at regional level
- **Responsibility:** Reviews applications escalated from branches; approves within credit authority
- **Pain:** Receives incomplete files; no system to manage his approval queue; relies on email chains
- **Goal:** Structured approval queue with all documents, auto-eligibility checks, and one-click decision
- **Tech Comfort:** High

### Persona 3: The Compliance Officer
- **Name:** Meena, Compliance team at Head Office
- **Pain:** Paper audit trails are incomplete; RBI inspection preparation takes weeks
- **Goal:** Real-time, searchable audit log of every action taken on every application
- **Tech Comfort:** Moderate

### Persona 4: The IT / System Admin
- **Name:** Rajan, Bank IT team
- **Pain:** No ability to configure approval thresholds or loan product parameters without vendor involvement
- **Goal:** Admin panel to configure loan products, eligibility rules, and workflow without coding
- **Tech Comfort:** Very High

---

## 6. Scope

### Release 1 — Core LOS (2018)
- Digital loan application form (all loan types configurable)
- Document checklist: auto-generated based on loan type and amount
- Document upload (PDF, images) with automated completeness check
- Application status tracking dashboard (loan officer + branch manager view)
- Basic approval workflow (2-level: branch → credit manager)
- Audit log: every action logged with user, timestamp, and comment
- Notification: SMS + email at key application milestones

### Release 2 — Automation & Integration (2019)
- Rule-based eligibility engine (income, age, CIBIL score, LTV)
- CIBIL bureau integration for automated credit pull
- Multi-level configurable approval workflow (up to 5 levels)
- Core banking system (CBS) integration: batch sync for disbursement
- Application dashboard for regional and HO teams
- SLA tracking: applications approaching TAT breach highlighted

### Release 3 — Reporting & Compliance (2021)
- Regulatory reporting module (RBI returns automation)
- Branch and officer performance dashboards
- Advanced search and filter across application database
- Self-service admin panel (loan product configuration, rule management)
- Customer-facing status portal (read-only, OTP-authenticated)

### Out of Scope
- Consumer mobile app (deferred)
- Proprietary credit scoring
- Insurance products
- Real-time CBS in v1

---

## 7. User Stories

### Epic 1: Loan Application Capture
```
As a Loan Officer,
I want to capture a complete loan application digitally in a single session,
So that I eliminate paper forms and data re-entry across multiple systems.

Acceptance Criteria:
- Application form dynamically adjusts fields based on loan type selected
- Mandatory fields validated inline (no blank submission)
- Applicant KYC details auto-populated from Aadhaar/PAN lookup (Release 2)
- Application saved as draft if session interrupted
- Completed application submitted with unique reference number
- Confirmation SMS sent to applicant on submission
```

### Epic 2: Document Management
```
As a Loan Officer,
I want the system to generate a document checklist based on loan type and amount,
So that I collect all required documents in one visit and avoid back-and-forth with the customer.

Acceptance Criteria:
- Checklist auto-generated on loan type + amount + applicant profile selection
- Each document uploadable as PDF or image (max 5MB per file)
- System validates file type and size on upload
- Completeness indicator shows % of required documents received
- Incomplete applications cannot be submitted for review
- Uploaded documents stored securely with access control by role
```

### Epic 3: Approval Workflow
```
As a Credit Manager,
I want a structured approval queue with all application details, documents, and eligibility results,
So that I can make informed decisions without requesting additional information from branches.

Acceptance Criteria:
- Queue shows all pending applications sorted by SLA breach risk
- Each application view shows: summary, all documents, eligibility check result, applicant history
- Approve/Reject/Send Back actions available with mandatory comment field
- Decision logged with timestamp, user ID, and comment
- Applicant and loan officer notified on decision via SMS + system notification
- Escalation to next level triggered automatically if within credit authority threshold
```

### Epic 4: Audit & Compliance
```
As a Compliance Officer,
I want a complete, searchable audit log of every action taken on every loan application,
So that I can respond to RBI inspection queries within hours, not weeks.

Acceptance Criteria:
- Every create, update, approve, reject, and document upload logged
- Log fields: action type, user, timestamp, application ID, comments
- Log is immutable (no edits or deletions)
- Searchable by: date range, user, branch, loan type, application ID
- Exportable as CSV or PDF for regulatory submission
- Retained for minimum 8 years per RBI guidelines
```

### Epic 5: Performance Dashboard (Release 3)
```
As a Branch Manager,
I want a dashboard showing my branch's loan pipeline, TAT performance, and officer productivity,
So that I can identify bottlenecks and coach my team proactively.

Acceptance Criteria:
- Dashboard shows: total applications (pipeline, approved, rejected, disbursed)
- Average TAT by loan type and officer
- Applications approaching SLA breach highlighted in red
- Drill-down by officer, loan type, and date range
- Exportable summary report (PDF)
```

---

## 8. Functional Requirements

| ID | Requirement | Priority | Release |
|----|-------------|----------|---------|
| FR-01 | Dynamic loan application form by loan type | P0 | R1 |
| FR-02 | Document checklist auto-generation | P0 | R1 |
| FR-03 | Document upload with completeness validation | P0 | R1 |
| FR-04 | 2-level approval workflow | P0 | R1 |
| FR-05 | Audit log (immutable) | P0 | R1 |
| FR-06 | Application status dashboard | P0 | R1 |
| FR-07 | SMS + email notifications | P1 | R1 |
| FR-08 | Rule-based eligibility engine | P0 | R2 |
| FR-09 | CIBIL bureau integration | P0 | R2 |
| FR-10 | Multi-level configurable workflow (up to 5) | P0 | R2 |
| FR-11 | CBS batch sync for disbursement | P0 | R2 |
| FR-12 | SLA breach alerting | P1 | R2 |
| FR-13 | Regulatory reporting module | P0 | R3 |
| FR-14 | Branch performance dashboards | P1 | R3 |
| FR-15 | Self-service admin panel | P1 | R3 |
| FR-16 | Customer-facing status portal | P2 | R3 |

---

## 9. Success Metrics & KPIs

### Primary Metrics
| Metric | Baseline | Target | Result |
|--------|----------|--------|--------|
| Loan processing TAT | 21 days | <3 days | ✅ Achieved (Release 2) |
| Data entry error rate | ~8% | <0.5% | ✅ Achieved (Release 1) |
| Officer productivity | Baseline | +40% applications/day | ✅ Achieved |
| On-time delivery | — | 100% across releases | ✅ 3/3 releases on time |
| Audit readiness | Weeks to compile | <1 hour | ✅ Achieved |

### Secondary Metrics
| Metric | Target |
|--------|--------|
| System uptime (banking hours) | 99.5%+ |
| User adoption (loan officers) | 95%+ using system within 30 days of go-live |
| Support tickets post-launch | <10% of user base raising tickets in first month |
| Document completeness at submission | >90% of applications submitted complete |
| UAT defect leakage to production | <5 critical defects per release |

### Guardrail Metrics
- Zero data loss or corruption incidents
- Zero unauthorised data access incidents
- 100% audit log integrity (no gaps or deletions)

---

## 10. Product Roadmap

```
2018 — Release 1: Core LOS
├── Requirements workshops with bank stakeholders (6 weeks)
├── BRD + FRD authored and signed off
├── UX design: application forms, document upload, dashboard
├── Development: 6-month build
├── UAT with branch operations team (4 weeks)
├── Defect triage and sign-off
└── Go-live: 12 pilot branches

2019 — Release 2: Automation & Integration
├── Eligibility rule engine (configurable)
├── CIBIL API integration
├── Multi-level approval workflow
├── CBS batch sync
├── SLA tracking dashboard
├── UAT with credit and IT teams
└── National rollout: all branches

2021 — Release 3: Reporting & Compliance
├── Regulatory reporting module
├── RBI return automation
├── Branch performance dashboards
├── Admin self-service panel
├── Customer status portal (OTP)
├── UAT with compliance + HO teams
└── Full production deployment
```

---

## 11. Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| CBS integration complexity causing R2 delay | High | High | Phased integration (batch sync v1, real-time v2); dedicated integration squad |
| Low loan officer adoption (change resistance) | High | High | Training sessions pre-go-live; branch champion programme; helpdesk |
| RBI regulatory change mid-development | Medium | High | Modular compliance architecture; legal counsel on retainer |
| UAT defect volume causing go-live delay | Medium | High | Early UAT involvement; test plan signed off 4 weeks before UAT |
| Data migration from paper/legacy system | High | Medium | Phased migration; parallel run period (3 months) |
| Performance degradation under peak branch load | Medium | High | Load testing pre-go-live; horizontal scaling plan |

---

## 12. Dependencies

| Dependency | Owner | Status |
|-----------|-------|--------|
| CIBIL bureau API access | Bank IT | ✅ R2 Complete |
| Core Banking System (CBS) API specs | Bank IT | ✅ R2 Complete |
| RBI compliance requirements sign-off | Bank Legal/Compliance | ✅ Each release |
| UX design (all releases) | Bespoke Design Team | ✅ Complete |
| Bank staff training programme | Bank HR + Bespoke PM | ✅ Pre-GoLive each release |
| Infrastructure provisioning (bank data centre) | Bank IT | ✅ Complete |
| UAT team availability (bank ops) | Bank Operations | ✅ Scheduled each release |

---

## 13. Open Questions

| # | Question | Owner | Status |
|---|----------|-------|--------|
| 1 | Should the system support co-applicant loan structures in v1? | PM + Bank Ops | Resolved: Yes, in R1 |
| 2 | What is the data retention requirement (RBI)? | Bank Legal | Resolved: 8 years |
| 3 | Should eligibility rules be configurable by bank admin without Bespoke involvement? | PM + Client | Resolved: Yes, R3 admin panel |
| 4 | Is real-time CBS integration feasible in R2 timeline? | Engineering + Bank IT | Resolved: Deferred to post-R3 |
| 5 | Will the bank run a parallel paper process during the transition? | Bank Ops | Resolved: 3-month parallel run |

---

*PRD authored by Pallavi Ahuja | Project Manager | Bespoke Technologies*  
*Contact: pallavixahuja007@gmail.com | linkedin.com/in/pallaviahuja*
