# Skill: Sales Program Health Dashboard

## Skill ID
`sales-program-health`

## What it does
Takes a sales program's revenue metrics and generates a **revenue-aware health dashboard with an AI-written exec narrative** — a single URL you can share with any executive that tells the full ARR story in under 60 seconds.

Unlike a generic program status page, this skill speaks the language of revenue: ARR waterfall, NRR, CAC, LTV:CAC, churn exposure, and growth lever breakdown — all synthesized into a 3-sentence narrative that says what's at risk and what action is needed.

---

## When to use this skill

- Weekly / monthly sales program reviews
- QBR prep — give execs the numbers + the story
- Board-level pipeline health updates
- Anytime you need to answer: *"Are we on track to hit ARR target, and why or why not?"*

---

## How to use it

```
Use the Sales Program Health skill.

Program: [Program Name · Company]
Sponsor: [VP Sales / CRO / CEO]
TPM: [Your name]
Period: [Q2 FY26]

ARR:
  Current ARR: $XM
  ARR Target: $XM by [date]
  NRR: X% (target: X%)

Waterfall (this quarter):
  New ARR: $XM
  Expansion ARR: $XM
  Churned ARR: $XM
  Required quarterly run rate: $XM/quarter

Unit Economics:
  CAC: $X (target: <$X)
  LTV: $X
  LTV:CAC: Xx (target: X×)
  Payback period: X months (target: <X months)

Leading Indicators:
  - [Metric name]: [current] (target: [X]) — [improving/declining/flat]
  - ...

Sub-programs:
  1. [Name] — [Green/Yellow/Red] — [2-3 milestone bullets]
  2. ...

Risks:
  - [HIGH/MED/LOW] [title] — [description]
  ...

Generate the Sales Program Health dashboard.
```

---

## Revenue Metrics Reference

| Metric | What it measures | Red flag threshold |
|---|---|---|
| **ARR** | Annual Recurring Revenue — contracted, predictable | Behind run rate by >15% |
| **NRR / NDR** | (ARR + Expansion − Churn) ÷ Starting ARR | <100% (losing ground) |
| **New ARR** | Revenue from new logos and new licenses | Below quarterly run rate |
| **Expansion ARR** | Upsell and cross-sell on existing accounts | Declining QoQ |
| **Churned ARR** | Lost accounts and downgrades | Accelerating |
| **CAC** | Customer Acquisition Cost | Rising faster than LTV |
| **LTV** | Lifetime Value = avg ACV × avg tenure months | Declining |
| **LTV:CAC** | Business model health ratio | Below 3× (unsustainable) |
| **Payback Period** | Months to recover CAC from margin | >18 months = high risk |

**LTV:CAC benchmarks:**
- `<3×` — Unsustainable. Acquisition costs too high.
- `3–5×` — Healthy. Monitor CAC trends.
- `>5×` — Strong. Consider investing more in growth.

---

## Output

A self-contained `sales-health.html` with:
- Dark-themed header with program name, status badge, and meta
- **Exec Narrative** — 3-sentence AI-generated summary: current state → key risk → required action
- **Escalation pills** — 2–3 color-coded immediate actions from the narrative
- **ARR Snapshot** — 4 KPI cards: Current ARR, NRR, Churned ARR, License Attainment
- **ARR Waterfall** — visual: New ARR + Expansion ARR − Churn = Net New ARR
- **Unit Economics** — CAC, LTV, LTV:CAC ratio, Payback Period with status indicators
- **Leading Indicators** — 4 metrics with trend arrows
- **Sub-program RAG cards** — each with milestone-level detail
- **Risks & Escalations** — severity-tagged, actionable
- Footer with GitHub link

Publishable to GitHub Pages. No build step. No dependencies.

---

## Live example

Kaseya 365 Sales Transformation:
https://goyalsandeep2k.github.io/program-health-dashboard/sales-health.html

---

## Related skills

- [Program Health Dashboard](https://goyalsandeep2k.github.io/program-health-dashboard/) — generic program health for any domain
- [Org Priority Stack](https://goyalsandeep2k.github.io/program-health-dashboard/priorities.html) — revenue-ranked program prioritization
- [PMaaS](https://github.com/goyalsandeep2k/claude-skills) — convert raw updates into stakeholder artifacts

---

## License
MIT © [Sandeep Goyal](https://sandeepgoyal.org)
