---
name: weekly-leadership-digest
description: Use whenever a CS leader needs to roll up book-of-business health into a concise weekly briefing for executives or the board. Trigger on requests like "build my weekly leadership update," "summarize the book for the CEO," or when a churn-radar/health-score output needs to be turned into an executive-facing digest.
---

# Weekly Leadership Digest Skill

## Purpose

Leadership doesn't need a spreadsheet of every account. They need to know what requires their attention, their money, or their air cover *this week*, and what's going well. This skill compresses account-level health data into a short, decision-oriented briefing.

## Required Input

- Account health/risk data (ideally the output of the `churn-radar` skill: tier, ARR, CSM owner, renewal date, driving signals)
- Optional: known wins, expansion signals, or reference-candidate accounts
- Optional: CSM headcount/book assignments, to surface workload imbalance

## What Goes In vs. What Gets Cut

Leadership digests fail when they try to be comprehensive. Include only:

1. **Portfolio snapshot**: total ARR, and the % split across health tiers. One line, not a full table.
2. **Needs leadership attention this week**: the 2–4 highest-stakes accounts (by ARR × urgency), each with a one-line reason and a specific ask (exec sponsor call, discount/save-play approval, escalation support), not just "this account is at risk."
3. **Workload flags**: If one CSM is carrying a disproportionate share of critical accounts relative to the team, say so. This is a resourcing signal leadership can act on, not a complaint.
4. **Wins & expansion signals**: 1–3 accounts trending well, especially any with expansion or reference/case-study potential. Leadership digests that are 100% bad news get ignored; real wins build credibility for the risk asks.
5. **Decisions needed from leadership**: the explicit list of things only leadership can approve (budget, discount authority, temporary staffing support, exec-to-exec outreach). If there's nothing to decide, say so. Don't pad the section.

Do not include full account lists, routine status updates, or anything the exec doesn't need to act on or know for a board/investor conversation.

## Output Format

A short briefing (email or Slack-length), five sections max, written so a time-constrained executive can read it in under two minutes and know exactly what's being asked of them.
