---
name: churn-radar
description: Use whenever a CS leader needs to score account health, identify churn risk, or produce a prioritized "who needs attention this week" list from account usage, support, and sentiment data. Trigger on CSV/sheet exports from a CRM or product analytics tool, requests like "which accounts are at risk," "score my book of business," or "build a churn radar."
---

# Churn Radar: Customer Health Scoring Skill

## Purpose

Turn scattered account signals (product usage, support volume, satisfaction, renewal timing) into a single, defensible risk tier per account and a ranked action list for CSMs and leadership. Replaces gut-feel account triage with a consistent, repeatable rubric.

## Required Input

A table (CSV, Sheet, or CRM export) with one row per account and these columns:

- `account_name`
- `segment` (SMB / Mid-Market / Enterprise)
- `arr`
- `csm_owner`
- `usage_trend_30d_pct`: % change in product usage over the trailing 30 days
- `support_tickets_30d`: ticket volume over the trailing 30 days
- `csat_90d`: average CSAT score, trailing 90 days (1–5 scale)
- `nps_last`: most recent NPS response (0–10)
- `days_since_last_ebr`: days since last executive business review / strategic touchpoint
- `renewal_date`

If a column is missing, say so explicitly and score only on what's available. Never invent a number to fill a gap.

## Scoring Rubric

Score each account by summing points across five signals:

| Signal | High risk (points) | Medium risk (points) | Low risk (points) |
|---|---|---|---|
| Usage trend (30d) | ≤ -15% (3) | -5% to -14.9% (2) | > -5% (0) |
| Support tickets (30d) | ≥ 10 (3) | 5–9 (2) | < 5 (0) |
| CSAT (90d) | < 3.5 (3) | 3.5–4.19 (2) | ≥ 4.2 (0) |
| NPS (last) | ≤ 6 / detractor (2) | 7–8 / passive (1) | ≥ 9 / promoter (0) |
| Days since last EBR | > 120 days (+1) |, | ≤ 120 days (0) |

**Tiers:**
- 0–2 points → 🟢 **Green** (healthy)
- 3–5 points → 🟡 **Yellow** (monitor / proactive outreach)
- 6+ points → 🔴 **Red** (immediate CSM + leadership attention)

**Escalation flag:** any 🔴 Red account with a `renewal_date` within 90 days gets a **CRITICAL** flag. These go at the top of the list regardless of ARR.

## Output

Produce two things:

1. A ranked table: Critical → Red → Yellow → Green, sorted by ARR within each tier, with the specific signals driving each score called out in plain language (e.g., "usage down 22% and 11 tickets in 30 days").
2. A short narrative summary: total ARR at risk (Red + Critical), count of accounts per tier, and the 2–3 accounts needing action this week.

Never smooth over a risk signal to make an account look healthier than the data supports, the value of this skill is honesty, not optimism.

## Notes for reuse

This rubric is a starting point, not gospel. In a real engagement, thresholds should be recalibrated against the client's actual churn history (e.g., "accounts that churned in the last 2 years averaged what usage decline before they left?") rather than used as generic defaults.
