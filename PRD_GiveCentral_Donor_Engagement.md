# PRD: Donor Engagement & Recurring Giving Optimisation
**Organisation:** GiveCentral  
**Product Manager:** Pallavi Ahuja  
**Role:** Product Manager (Reporting to CEO — Shivansh Pandey)  
**Status:** 🔄 In Progress  
**Started:** December 2025  
**Platform:** GiveCentral — Fundraising & Payments Platform for Nonprofits  

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

Nonprofit organisations using GiveCentral face two interconnected challenges that directly impact their fundraising performance:

### Challenge 1: Low Recurring Giving Conversion
Most donors complete one-time donations but do not convert to recurring (monthly/annual) giving programmes — despite recurring donors being **3–5× more valuable** in lifetime contribution. Current platform flows prioritise one-time donation UX; the recurring giving option is buried and poorly communicated, leading to:
- Low recurring donor conversion rate
- High dependency on year-end campaign spikes
- Unpredictable revenue for nonprofits

### Challenge 2: Donor Drop-Off During the Giving Flow
Analysis of the donation funnel reveals significant drop-off between landing page and completed transaction:
- ~45% of donors who begin a donation form do not complete it
- Drop-off concentrated at: payment detail entry, amount selection, and account creation prompts
- Mobile conversion rate significantly lower than desktop (~30% gap)
- Post-donation engagement is minimal — no personalised thank-you journey, no impact reporting

**The core problem:** GiveCentral's platform does not sufficiently optimise for recurring giving conversion or donor retention — two KPIs that directly drive nonprofit client success and platform stickiness.

---

## 2. Goals & Objectives

### Primary Goal
Increase recurring donor conversion rate by 35% and reduce donation funnel drop-off by 25% through targeted UX improvements, A/B testing, and personalised donor engagement journeys.

### Business Goals
| Goal | Target | Timeline |
|------|--------|----------|
| Recurring donor conversion rate | +35% | Q2 2026 |
| Donation funnel completion rate | +25% (drop-off from 45% → 20%) | Q1 2026 |
| Mobile donation conversion | Close desktop gap to <10% | Q2 2026 |
| Donor retention (Year 2 repeat giving) | +20% | Q3 2026 |
| Transaction success rate | 99.2%+ | Ongoing |
| Nonprofit client NPS | +15 points | Q3 2026 |

### Product Goals
- Redesign recurring giving UX — make it prominent, compelling, and frictionless
- Optimise donation flow for mobile (one-tap payment, guest checkout)
- Build personalised post-donation journey (thank-you, impact updates, renewal prompts)
- Implement A/B testing framework across donation pages
- Define and monitor donor KPIs: conversion, engagement, retention, transaction success

---

## 3. Non-Goals

- ❌ Building a proprietary payment processor (continue using existing gateway)
- ❌ CRM system replacement (integrate with existing nonprofit CRMs)
- ❌ Cryptocurrency donation support (future roadmap)
- ❌ In-person / POS donation hardware
- ❌ Grant management or programme reporting
- ❌ Multi-language support in v1 (English-first)

---

## 4. Background & Context

GiveCentral is a fundraising and payments platform serving nonprofit organisations across the US. The platform enables nonprofits to collect donations online, manage donor databases, run fundraising campaigns, and process payments compliantly (PCI-DSS).

**Market context:**
- US online giving totalled $59.8B in 2023 (Giving USA)
- Monthly recurring donors give 42% more annually than one-time donors (Network for Good)
- Mobile accounted for 57% of nonprofit website traffic but only 28% of donations (M+R Benchmarks 2024) — a conversion gap this PRD directly addresses
- Competitors (Donorbox, Classy, Bloomerang) are aggressively investing in recurring giving UX and AI-powered donor engagement

**Strategic context:**
This PRD addresses GiveCentral's two highest-leverage product opportunities identified in the 30-day discovery sprint (December 2025):
1. Recurring giving conversion (highest ROI for nonprofit clients)
2. Mobile donation funnel optimisation (largest volume opportunity)

---

## 5. Target Users & Personas

### Persona 1: The Nonprofit Fundraising Manager
- **Name:** Sarah, Director of Development at a mid-sized US charity
- **Responsibility:** Runs annual fund, manages donor relationships, sets fundraising goals
- **Pain:** Year-end donation spikes make revenue unpredictable; recurring giving programme is underdeveloped
- **Goal:** Predictable monthly revenue from recurring donors; platform that converts one-time donors to recurring
- **Tech Comfort:** Moderate — uses Salesforce, Mailchimp, basic analytics

### Persona 2: The First-Time Donor (One-Time)
- **Name:** Michael, 38, professional who donates to 3–4 causes per year
- **Channel:** Mobile, discovers via social media or email campaign
- **Pain:** Donation forms feel long; doesn't want to create an account; unsure how much to give
- **Goal:** Complete a donation quickly, feel good about it, receive confirmation
- **Conversion opportunity:** Convert to monthly recurring donor with a well-timed, low-friction ask

### Persona 3: The Recurring Donor
- **Name:** Linda, 54, loyal supporter of a nonprofit for 5+ years
- **Pain:** No visibility into how her monthly gift is being used; renewal prompts feel generic
- **Goal:** Feel connected to the cause; know her impact; easy to update payment method or giving amount
- **Tech Comfort:** Moderate — prefers email, occasionally uses the donor portal

### Persona 4: The GiveCentral Platform Admin (Internal)
- **Name:** GiveCentral customer success and engineering teams
- **Goal:** Ability to configure A/B tests, monitor funnel metrics, and push product improvements without full engineering sprints

---

## 6. Scope

### Phase 1 — Funnel Optimisation (Q1 2026)
- Donation form redesign: streamlined 3-step flow (amount → payment → confirmation)
- Guest checkout: remove mandatory account creation from critical path
- Mobile-optimised payment form (Apple Pay, Google Pay integration)
- Smart amount suggestions (data-driven, personalised to campaign)
- Progress indicator on multi-step forms
- A/B testing framework: headline, CTA, amount options, recurring ask placement
- Real-time funnel analytics dashboard (conversion by step, by device, by campaign)

### Phase 2 — Recurring Giving UX (Q2 2026)
- Recurring giving prominence: featured ask on all donation pages (not buried)
- Post one-time donation: recurring upsell modal (30-day follow-up email + in-portal)
- Recurring plan management: donor self-service (pause, upgrade, cancel, payment method update)
- Impact-based recurring messaging: "Your $25/month funds 3 meals a day"
- Annual recurring donor renewal campaign tooling for nonprofits

### Phase 3 — Donor Retention & Engagement (Q3 2026)
- Personalised post-donation thank-you journey (email sequence based on giving history)
- Impact reports: automated quarterly impact update emails per donor
- Donor anniversary recognition (1-year, 5-year milestone)
- Lapsed donor re-engagement flow (automated, triggered at 90-day no-activity)
- Donor portal: giving history, impact, and self-service recurring management

### Out of Scope
- Cryptocurrency
- CRM replacement
- POS hardware
- Multi-language

---

## 7. User Stories

### Epic 1: Streamlined Donation Funnel
```
As a first-time donor on mobile,
I want to complete a donation in under 2 minutes without creating an account,
So that I don't abandon the form due to friction or time pressure.

Acceptance Criteria:
- Donation form is 3 steps max: amount selection → payment → confirmation
- Guest checkout available (email only, no password required)
- Apple Pay and Google Pay displayed prominently on mobile
- Form loads in <2 seconds on 4G
- Completion confirmation shown immediately with receipt sent to email
- No mandatory account creation in the primary donation path
```

```
As a nonprofit fundraising manager,
I want to run A/B tests on my donation page (headline, CTA, amount options),
So that I can continuously improve conversion without needing engineering resources.

Acceptance Criteria:
- A/B test can be configured via dashboard (no code)
- Test variables: headline text, suggested amounts, CTA button label, recurring ask placement
- Minimum traffic split: 50/50 (configurable)
- Results dashboard shows: conversion rate by variant, statistical significance indicator
- Winning variant can be set as default with one click
```

### Epic 2: Recurring Giving Conversion
```
As a first-time one-time donor,
I want to see a clear, compelling prompt to become a monthly donor immediately after my donation,
So that I can make the choice to give regularly while my motivation is highest.

Acceptance Criteria:
- Post-donation page presents recurring upsell within the confirmation screen
- Recurring ask uses impact language: "Your $X/month does Y"
- One-click opt-in to monthly recurring (payment details already captured)
- Option to choose monthly amount (pre-suggested based on one-time amount)
- If declined, automated follow-up email sent at Day 7 and Day 30
- Conversion rate tracked separately: immediate vs. email follow-up
```

```
As a recurring donor,
I want to manage my giving plan (pause, change amount, update card) from my donor portal,
So that I don't have to contact the nonprofit or cancel when my circumstances change.

Acceptance Criteria:
- Donor portal accessible via email link (no password required for basic actions)
- Can pause giving for 1, 2, or 3 months
- Can upgrade or downgrade monthly amount
- Can update payment method (card or bank account)
- Changes take effect on next billing cycle
- Confirmation email sent on any plan change
```

### Epic 3: Donor Retention & Impact
```
As a recurring donor,
I want to receive a quarterly impact report showing what my contributions have funded,
So that I feel connected to the cause and motivated to continue giving.

Acceptance Criteria:
- Impact report generated and emailed quarterly (configurable by nonprofit)
- Report includes: total given YTD, impact metrics (set by nonprofit), personal message from ED
- Personalised to donor's giving history (not generic)
- One-click option to upgrade giving amount included in email
- Open rate and click-through rate tracked per campaign
```

### Epic 4: KPI & Analytics Dashboard
```
As a nonprofit fundraising manager,
I want a real-time dashboard showing my donation funnel performance, donor conversion, and recurring giving metrics,
So that I can make data-informed decisions about campaigns and platform improvements.

Acceptance Criteria:
- Dashboard shows: total donations, recurring vs. one-time split, funnel drop-off by step
- Donor metrics: new donors, returning donors, lapsed donors, recurring conversion rate
- Transaction metrics: success rate, failed payments, average gift size
- Filterable by: date range, campaign, donation page, device type
- Exportable as CSV and PDF
- Data refreshed every 15 minutes
```

---

## 8. Functional Requirements

| ID | Requirement | Priority | Phase |
|----|-------------|----------|-------|
| FR-01 | 3-step streamlined donation form | P0 | P1 |
| FR-02 | Guest checkout (no mandatory account) | P0 | P1 |
| FR-03 | Apple Pay + Google Pay on mobile | P0 | P1 |
| FR-04 | Smart amount suggestions (data-driven) | P1 | P1 |
| FR-05 | A/B testing framework (no-code) | P0 | P1 |
| FR-06 | Real-time funnel analytics dashboard | P0 | P1 |
| FR-07 | Post-donation recurring upsell (in-page) | P0 | P2 |
| FR-08 | Recurring follow-up email automation (Day 7, Day 30) | P1 | P2 |
| FR-09 | Donor self-service recurring management portal | P0 | P2 |
| FR-10 | Recurring plan: pause, upgrade, cancel, payment update | P0 | P2 |
| FR-11 | Impact-based recurring messaging engine | P1 | P2 |
| FR-12 | Quarterly personalised impact report (automated email) | P1 | P3 |
| FR-13 | Lapsed donor re-engagement flow (90-day trigger) | P1 | P3 |
| FR-14 | Donor anniversary recognition | P2 | P3 |
| FR-15 | Donor giving history portal | P1 | P3 |
| FR-16 | PCI-DSS compliance maintained across all payment flows | P0 | All |
| FR-17 | Payment compliance monitoring: data privacy + regulations | P0 | All |

---

## 9. Success Metrics & KPIs

### Primary Metrics
| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Recurring donor conversion rate | Measured at kickoff | +35% | Q2 2026 |
| Donation funnel completion rate | ~55% | >80% | Q1 2026 |
| Mobile donation conversion | ~30% below desktop | Close gap to <10% | Q2 2026 |
| Donor Year-2 retention | Measured at kickoff | +20% | Q3 2026 |
| Transaction success rate | Measured at kickoff | >99.2% | Ongoing |

### Secondary Metrics
| Metric | Target |
|--------|--------|
| Average gift size (recurring) | +15% via smart amount suggestions |
| A/B test win rate | Positive improvement in >60% of tests run |
| Impact email open rate | >35% |
| Recurring plan self-service adoption | >50% of plan changes via portal (not support) |
| Nonprofit client NPS | +15 points by Q3 2026 |

### Guardrail Metrics
- Payment failure rate: no increase from baseline
- Donor support ticket volume: no increase post-launch
- PCI-DSS compliance: zero violations
- Page load time: <2 seconds on 4G (mobile)

---

## 10. Product Roadmap

```
Dec 2025 — Discovery (Current)
├── 30-day discovery sprint: 10+ nonprofit client interviews
├── Funnel analytics audit (Mixpanel, Google Analytics)
├── Competitive analysis: Donorbox, Classy, Bloomerang
├── Baseline KPI measurement
└── Roadmap prioritisation with CEO

Q1 2026 — Phase 1: Funnel Optimisation
├── Donation form redesign (3-step, mobile-first)
├── Guest checkout
├── Apple Pay / Google Pay
├── A/B testing framework
├── Funnel analytics dashboard
└── Launch + measure: 4-week post-launch analysis

Q2 2026 — Phase 2: Recurring Giving
├── Post-donation recurring upsell
├── Recurring follow-up email automation
├── Donor self-service portal (pause, upgrade, update)
├── Impact-based messaging engine
└── Recurring conversion A/B tests

Q3 2026 — Phase 3: Retention & Engagement
├── Quarterly impact reports (automated)
├── Lapsed donor re-engagement flow
├── Donor anniversary recognition
├── Full donor portal (history + self-service)
└── Client NPS survey + roadmap review

Q4 2026 — Scale & Innovation
├── AI-assisted amount personalisation
├── Predictive churn scoring for recurring donors
├── CRM integrations (Salesforce, HubSpot)
├── Multi-language support (Spanish)
└── Cryptocurrency donation exploration
```

---

## 11. Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| A/B test results inconclusive due to low traffic | Medium | Medium | Minimum traffic threshold before declaring winner; Bayesian significance testing |
| Payment gateway changes impacting Apple/Google Pay | Low | High | Abstraction layer; payment provider SLA monitoring |
| Nonprofit clients resistant to UX changes on their donation pages | Medium | High | Opt-in rollout; A/B test new vs. old; clear ROI communication |
| GDPR / data privacy regulation changes | Medium | High | Privacy-by-design architecture; legal review at each phase |
| Recurring upsell perceived as pushy by donors | Medium | Medium | User testing pre-launch; A/B test timing and copy; easy dismiss option |
| PCI-DSS compliance gap in new payment flows | Low | Critical | Security review at every phase gate; penetration testing pre-launch |
| Low nonprofit engagement with analytics dashboard | Medium | Low | Onboarding training; customer success touchpoints; in-app tooltips |

---

## 12. Dependencies

| Dependency | Owner | Status |
|-----------|-------|--------|
| Apple Pay / Google Pay merchant account setup | Engineering + Finance | 🔄 In Progress |
| A/B testing tool selection (Optimizely / LaunchDarkly / custom) | PM + Engineering | 🔄 Evaluating |
| Mixpanel funnel event taxonomy | PM + Engineering | 🔄 In Progress |
| Email automation platform (existing or new) | PM + Marketing | 🔄 Evaluating |
| Legal review — donor data usage for personalisation | Legal | ⏳ Scheduled |
| Nonprofit client UAT participants (Phase 1) | Customer Success | ⏳ Recruiting |
| PCI-DSS review for new payment flows | Security / Compliance | ⏳ Scheduled |
| UX design — donation form + donor portal | Design | 🔄 In Progress |

---

## 13. Open Questions

| # | Question | Owner | Status |
|---|----------|-------|--------|
| 1 | Should recurring upsell be shown to all donors or only those giving above a certain threshold? | PM | 🔄 Open — A/B test both |
| 2 | What is the right cadence for impact emails — monthly or quarterly? | PM + Client Research | 🔄 Open |
| 3 | Should donor self-service portal require password login or magic link? | PM + Engineering | 🔄 Open — leaning magic link |
| 4 | Which A/B testing tool to adopt — Optimizely, LaunchDarkly, or custom-built? | PM + Engineering | 🔄 Evaluating |
| 5 | How do we handle recurring donors whose cards expire without updating? | Engineering + PM | 🔄 Open — smart retry + email flow needed |
| 6 | Should lapsed donor re-engagement be automated or require nonprofit approval per send? | PM + CS | 🔄 Open |

---

## Appendix: Competitive Analysis Summary

| Feature | GiveCentral | Donorbox | Classy | Bloomerang |
|---------|------------|----------|--------|------------|
| Recurring giving UX | ⚠️ Basic | ✅ Strong | ✅ Strong | ✅ Strong |
| Mobile optimisation | ⚠️ Improving | ✅ Good | ✅ Good | ⚠️ Moderate |
| A/B testing | ❌ Not available | ❌ Not available | ✅ Available | ❌ Not available |
| Donor self-service | ⚠️ Basic | ✅ Good | ✅ Good | ✅ Good |
| Impact reporting | ❌ Not available | ❌ Not available | ⚠️ Basic | ✅ Strong |
| Analytics dashboard | ⚠️ Basic | ⚠️ Basic | ✅ Strong | ✅ Strong |

**Key differentiator opportunity:** GiveCentral can be the **only** platform offering built-in no-code A/B testing + automated impact reporting — a meaningful competitive advantage.

---

*PRD authored by Pallavi Ahuja | Product Manager | GiveCentral*  
*Reporting to: Shivansh Pandey (CEO)*  
*Contact: pallavixahuja007@gmail.com | linkedin.com/in/pallaviahuja*
