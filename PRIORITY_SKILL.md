# Skill: Org Priority Stack

## Skill ID
`org-priority-stack`

## What it does
Takes a list of competing programs across any organization and produces a **ranked, revenue-sorted HTML priority dashboard** — the single source of truth for program staffing, go/no-go decisions, and resource allocation.

Works for any team, any domain mix, any company. Just supply your programs and the skill handles scoring, ranking, visualization, and DRI assignment.

---

## When to use this skill

- Quarterly planning: "What do we staff first?"
- Portfolio reviews: "We have 20 programs and 12 eng-quarters — what gets cut?"
- Executive alignment: "Why is Program X ranked above Program Y?"
- Onboarding new leaders: "Here's the org's current priority order and who owns what"

---

## How to use it

Paste this into Claude with your data filled in:

```
Use the Org Priority Stack skill.

Organization: [Your org name]
Fiscal period: [e.g. FY26 Q2]
Owner: [Your name + title]

Programs:
1. [Program Name] | Domain: Feature/Reliability/Platform | Annual Goal: [specific measurable target] | Est. Revenue Impact: [$XM - Direct ARR / ARR Protected / Future ARR] | DRI: [Name, Title]
2. ...
(add as many as you have — 10 to 30 works well)

Ranking rule: Sort by Revenue Impact (highest first). Ties broken by customer impact.
Platform investments get a 20% eng capacity floor regardless of rank.

Generate the priority stack HTML dashboard.
```

---

## Revenue Impact types

| Type | Definition | Example |
|---|---|---|
| **Direct ARR** | New revenue the program generates | Selling 10,000 licenses → $10M ARR |
| **ARR Protected** | Existing revenue saved from churn | 99.9% uptime protecting $200M base → $8M saved |
| **Future ARR Unlocked** | Platform enablement, 50% discounted for lag | Microservices enabling 10× velocity over 3 years → $5M |

---

## Output

A self-contained `index.html` with:
- Same dark-themed header as the Program Health Dashboard
- 3 revenue ranking rule cards at the top
- Full priority table: `# · Program · Domain · Annual Input Goal · Revenue Impact · DRI`
- Color-coded domain badges (Feature/Reliability/Platform)
- DRI avatar with initials, name, and title
- Revenue progress bars (proportional to max)
- Footer with GitHub link

Publishable to GitHub Pages for a shareable URL. No build step. No dependencies.

---

## Live example

Kaseya 365 Sales Transformation — 20 programs ranked:
https://goyalsandeep2k.github.io/program-health-dashboard/priorities.html

---

## Related skills

- [Program Health Dashboard](https://goyalsandeep2k.github.io/program-health-dashboard/) — track execution health of a single program
- [PMaaS](https://github.com/goyalsandeep2k/claude-skills) — convert raw updates into stakeholder artifacts

---

## License
MIT © [Sandeep Goyal](https://sandeepgoyal.org)
