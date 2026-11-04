# AI Customer Success Toolkit

Four AI workflows I built for everyday Customer Success work: spotting at-risk accounts, planning onboarding, briefing leadership, and running consistent playbooks. Each one is a Claude skill with a sample run on made-up data, so you can see exactly what it produces.

Built by **Pearl McGuire** · [LinkedIn](https://www.linkedin.com/in/pearlmcguire)

## The four projects

| Project | What it does |
|---|---|
| [**Churn Radar**](01-customer-health-score-churn-radar/) | Scores every account's health with a clear rubric and ranks which ones need action first. |
| [**Onboarding Concierge**](02-onboarding-concierge/) | Turns a new customer's details into an onboarding plan built around their real people, systems and risks. |
| [**Weekly Leadership Digest**](03-weekly-leadership-digest/) | Condenses account health into a two-minute briefing with the decisions leadership needs to make. |
| [**Playbooks as Skills**](04-cs-playbooks-as-skills/) | Turns renewal, save and business review playbooks into step-by-step AI skills a team can use in the moment. |

## How they work together

Churn Radar scores the accounts. Its results feed the Weekly Leadership Digest and trigger the save playbook for any account at high risk. Onboarding Concierge brings new customers into the same health tracking from day one.

## How each project is built

- Every project is a **Claude skill**: a written, step-by-step process (`SKILL.md`) anyone can read and edit, not a hidden script.
- No custom code is needed. The same steps can run in automation tools like Zapier, Make or n8n.
- All sample data is **made up**. No real customer or employer data appears anywhere in this repository.

Each project folder has a `README.md` (the problem and what to look for), the `SKILL.md`, sample input in `sample-data/`, and the output in `sample-output/` (See the live demos: 
| Churn Radar: (https://pearlmcguire-gif.github.io/ai-cs-toolkit/01-customer-health-score-churn-radar/sample-output/churn-radar-dashboard.html) |
| Onboarding Concierge link: (https://pearlmcguire-gif.github.io/ai-cs-toolkit/02-onboarding-concierge/sample-output/solstice-retail-onboarding-plan.html) |
| Weekly Digest Link: (https://pearlmcguire-gif.github.io/ai-cs-toolkit/03-weekly-leadership-digest/sample-output/weekly-digest-2026-08-11.html) ) |

Start with [Churn Radar](01-customer-health-score-churn-radar/). The other three build on it.
