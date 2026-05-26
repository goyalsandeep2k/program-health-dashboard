# Skill: Program Health Dashboard

## Skill ID
`program-health-dashboard`

## Description
Generate a complete, single-page HTML program health dashboard for any technical program. Covers lagging indicators, leading indicators, sub-goal RAG status, milestone timelines, risks, and decisions needed.

## When to use this skill
- Weekly / monthly program reviews
- Exec stakeholder updates
- Quarterly business reviews (QBRs)
- Any program status communication where a snapshot URL is needed

## Inputs (provide these to Claude)

| Input | Description | Example |
|---|---|---|
| `program_name` | Full program name | "Sales Transformation · Kaseya 365" |
| `mission` | One-sentence purpose + outcome | "Transform sales motion to close 10,000 licenses by Dec 2026" |
| `lagging_indicator` | Main outcome metric | `{name, target, current, deadline}` |
| `leading_indicators` | 2–4 success measures | `[{name, target, current, trend}]` |
| `sub_goals` | 2–3 sub-programs | `[{name, status, milestones[]}]` |
| `milestones` | Program timeline | `[{label, date, status}]` |
| `risks` | Current blockers | `[{severity, title, description}]` |
| `decisions` | Open decisions | `[{urgency, title, description}]` |
| `tpm` | Your name | "Sandeep Goyal" |
| `sponsor` | Executive sponsor | "VP of Sales" |

## Status values
- `green` / **On Track** — All key milestones on schedule
- `yellow` / **At Risk** — One or more milestones at risk, mitigation in place
- `red` / **Off Track** — Critical milestone missed or blocked, escalation needed

## Output
A self-contained `index.html` file with dark-themed dashboard. No dependencies. Publishable to GitHub Pages, Notion embed, or any static host.

## Example prompt
```
Use the Program Health Dashboard skill.

Program: Cloud Migration · FY26
Mission: Migrate all on-prem workloads to OCI by Q4 FY26, reducing infra cost by 30%
Lagging: Workloads migrated — target 450, current 180
Leading indicators:
  - Migration velocity: 22/week (target 35/week) — declining
  - Env stability post-migration: 94% (target 99%) — improving
  - Team capacity utilization: 87% (target <80%) — at risk
Sub-goals:
  1. Dev/Test workloads — On Track — 3 of 4 milestones done
  2. Prod workloads — At Risk — blocked on network peering approval
  3. Data / DB migration — Off Track — tooling not finalized
Risks: Network peering approval blocked (HIGH), DB migration vendor not selected (HIGH)
Decisions: Approve network peering config by June 20 (URGENT)
TPM: Sandeep Goyal · Sponsor: CTO

Generate the dashboard HTML.
```
