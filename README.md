# Program Health Dashboard

A **generic, reusable program health dashboard** template for Technical Program Managers. Tracks lagging indicators, leading indicators, sub-goal health, milestones, risks, and decisions needed — all in a single-page, shareable HTML file.

**Live demo (Kaseya Sales Transformation):** https://goyalsandeep2k.github.io/program-health-dashboard/

Built by [Sandeep Goyal](https://sandeepgoyal.org) · Part of the [Claude Skills Marketplace](https://goyalsandeep2k.github.io/#claude-skills)

---

## What it shows

| Section | What it tracks |
|---|---|
| **Program Header** | Name, overall RAG status, TPM, sponsor, last updated |
| **Mission Statement** | Program purpose and outcome in one sentence |
| **Lagging Indicator** | The one outcome metric that defines program success (e.g. licenses sold, revenue, NPS) |
| **Leading Indicators** | 2–4 predictive success measures with progress bars and trend direction |
| **Timeline** | Key milestones with done / in-progress / planned / blocked status |
| **Sub-Goal Health** | Up to 3 sub-programs, each with RAG status and milestone checklist |
| **Risks & Blockers** | High / Med severity risk items with owner and ETA |
| **Decisions Needed** | Urgent / Med priority decisions with deadline and decision owner |

---

## Use as a Claude Skill

Add this to your Claude session context to generate a program health dashboard for **any program**:

```
Use the Program Health Dashboard skill (https://github.com/goyalsandeep2k/program-health-dashboard).

My program:
- Name: [Your Program Name]
- Mission: [One-sentence goal]
- Lagging indicator: [Outcome metric, target, current value]
- Leading indicators: [List 2–4 success measures with targets]
- Sub-goals: [List 2–3 with key milestones]
- Risks: [List current blockers]
- Decisions needed: [List open decisions]

Generate the dashboard HTML.
```

---

## Customizing

The `index.html` file is self-contained — no dependencies, no build step. Edit the data sections directly:

- **Colors / theme:** Edit CSS variables at `:root`
- **Program data:** Edit the HTML sections (header, mission, KPI numbers, metric cards, sub-goals, risks)
- **New sections:** Follow the existing card/grid patterns

---

## License

MIT © [Sandeep Goyal](https://sandeepgoyal.org)
