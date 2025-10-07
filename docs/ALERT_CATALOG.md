# Alert Catalog (Specification)

**Scope:** Estonia, high-level KPI guardrails using sanctioned metrics only (NGR, Turnover, NDCS, NRCS).  
**Principle:** To be implemented natively in BI (Looker/Power BI). This document defines thresholds and cadence.

## A1 — NGR Weekly Drop
- **Trigger:** NGR (last 7 days) ≤ −12% vs prior 7 days
- **Cadence:** Daily check, 09:00 EEST
- **Recipients:** Country Manager EE, Marketing Lead, BI channel
- **Action:** Review NDCS & efficiency (NGR/Turnover); confirm campaign/margin drivers

## A2 — NDCS Pacing Miss
- **Trigger:** NDCS-to-date < linear month target by Mon/Wed/Fri 09:00
- **Recipients:** Acquisition owner EE, Marketing Lead
- **Action:** Pull forward acquisition offers, adjust spend mix

## A3 — Efficiency Anomaly
- **Trigger:** |z-score(NGR/Turnover, trailing 90 days)| ≥ 2
- **Recipients:** Trading/Sportsbook, CRM, Marketing Lead
- **Action:** Validate margin/bonus impact, segment mix

## A4 — NRCS→NDCS Conversion Dip
- **Trigger:** Conversion rate down ≥ 5pp WoW
- **Recipients:** CRM/Onboarding owner, Marketing Lead
- **Action:** Review onboarding funnel & bonus comms
