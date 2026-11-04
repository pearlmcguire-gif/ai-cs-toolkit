---
name: onboarding-concierge
description: Use whenever a new account needs an onboarding plan, kickoff-to-value tracker, or implementation timeline built. Trigger on new-logo intake forms/data, requests like "build an onboarding plan for [account]," or "what should this customer's first 90 days look like."
---

# Onboarding Concierge: Kickoff-to-Value Planning Skill

## Purpose

Turn a new-account intake into a tailored, realistic onboarding plan the CSM and customer can both follow, replacing generic templates or one-off planning with something that reflects the account's actual tier, use case, and constraints.

## Required Input

Intake data with at minimum:

- `account_name`: `segment` (SMB / Mid-Market / Enterprise)
- `primary_use_case`: what the customer is trying to accomplish, in their words
- `executive_sponsor` and `day_to_day_stakeholders`
- `target_go_live_days` (or infer a reasonable default by segment if not given: SMB 14 days, Mid-Market 30 days, Enterprise 45–60 days)
- `integrations_required`
- `known_risks`: anything already flagged that could slow onboarding (competing IT priorities, limited stakeholder bandwidth, etc.)

Never invent stakeholders, integrations, or risks that weren't provided. If the intake is thin, note what's missing and ask for it rather than filling gaps with assumptions.

## Planning Logic

Match plan depth to segment:

- **SMB**: lightweight, self-serve-leaning plan. Fewer touchpoints, templated config, group or async training.
- **Mid-Market**: guided plan with a dedicated kickoff call, live configuration support, and structured training for a small group of admins/power users.
- **Enterprise**: full white-glove plan: multi-stakeholder kickoff, phased integration and configuration, role-based training tracks, a named executive check-in cadence, and a formal value-confirmation milestone.

Structure every plan in phases, each with: objective, key activities, owner (customer vs. CSM/implementation team), and target date relative to contract start.

1. **Kickoff & Alignment**: confirm success criteria, stakeholders, timeline; surface known risks early and build mitigation into the plan rather than ignoring them.
2. **Configuration & Integration**: build out the environment and connect the systems in `integrations_required`.
3. **Training & Adoption**: get named users comfortable and confident, sized to `user_seats`/stakeholder group.
4. **Go-Live & Validation**: confirm the system is live and being used as intended.
5. **Value Confirmation (30/60/90)**: check the plan actually delivered against the success criteria defined at kickoff, not just that implementation finished.

If `known_risks` includes a scheduling or bandwidth conflict, adjust the relevant phase's timeline or touchpoint format around it explicitly, call this out in the plan rather than burying it.

## Output

A dated, phase-by-phase plan (table or timeline) plus a one-line summary of the biggest risk to hitting `target_go_live_days` and how the plan accounts for it.
