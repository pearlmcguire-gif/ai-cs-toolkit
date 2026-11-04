# Churn Radar: AI customer health scoring

**The problem:** Many Customer Success teams judge account risk by feel. One person mentions an account "seems quiet," and the pattern across all accounts goes unnoticed until a renewal is lost.

**What it does:** You give the skill a standard export (usage trend, support tickets, customer satisfaction score, Net Promoter Score, renewal date). It scores every account against a clear rubric and returns a ranked list: Critical, Red, Yellow or Green, with the exact signals behind each score.

## How to use it

1. Export account data in the format of [`sample-data/accounts.csv`](sample-data/accounts.csv).
2. Run the skill in [`SKILL.md`](SKILL.md).
3. Get a ranked report, with the highest-value, most urgent accounts at the top.

## Sample run

[`sample-output/churn-radar-dashboard.html`](sample-output/churn-radar-dashboard.html) scores 15 made-up accounts:

- 7 of the 15 are flagged Critical (high risk and renewing within 90 days). Together they hold $1.37M of the sample's $3.07M in annual recurring revenue.
- Every flag shows its reasons, for example "usage down 22%, 11 tickets in 30 days, no executive review in 145 days."

## Why it helps

- Turns "I have a bad feeling about this account" into a score leadership can act on.
- Catches risk early, while there's still time to act.
- Gives the whole team the same rubric.

For real use, the thresholds should be tuned to the team's own churn history.

*All data in this project is made up for demonstration.*
