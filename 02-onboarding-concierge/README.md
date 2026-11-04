# Onboarding Concierge: AI onboarding plans

**The problem:** Onboarding plans are often copied from a template and never adjusted for the customer's people, systems or known risks. Slow or generic onboarding delays the moment the customer sees value.

**What it does:** You give the skill a new customer's details: segment, use case, people involved, integrations, target go-live date and known risks. It returns a phased plan with owners and dates, built around those constraints.

## How to use it

1. Fill in the customer's details in the format of [`sample-data/new-account-intake.json`](sample-data/new-account-intake.json).
2. Run the skill in [`SKILL.md`](SKILL.md).
3. Get a plan in five phases: kickoff, setup and integrations, training, go-live, and a value check.

## Sample run

[`sample-output/solstice-retail-onboarding-plan.html`](sample-output/solstice-retail-onboarding-plan.html) plans onboarding for a made-up retailer with 14 locations, 3 integrations, and an IT lead busy with another system migration. The plan:

- Does the two easier integrations first, and schedules the hardest one for when the IT lead is free.
- Fits training around the store managers' available times.
- Ends with 30, 60 and 90-day checks against the goals set at kickoff.

## Why it helps

- Plans match the customer's real situation, so known risks don't cause delays.
- The depth of the plan fits the size of the customer.
- "Onboarding complete" means the customer is getting value, not just that setup is finished.

*The customer and data in this project are made up for demonstration.*
