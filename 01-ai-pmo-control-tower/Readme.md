# AI PMO Control Tower

**Internal enterprise platform for proactive, evidence-based delivery management.**

Hybrid Azure + on-premises · 90-day pilot MVP · 6 clients across 2 delivery models

## Practical Steps

1. **Problem framing** — Move the PMO from reactive status reporting to proactive, evidence-based management.
2. **Persona & workflow definition** — Identify key roles and high-value agent-supported workflows.
3. **Architecture & data design** — Define hybrid deployment, core entities, and source integrations.
4. **MVP scoping** — Prioritise vertical slices that prove value in one support and one implementation client.
5. **Risk, metrics & governance** — Establish evaluation gates, security controls, and delivery cadence.

## Key Artefacts

| Artefact | Description |
|----------|-------------|
| [01-executive-summary.md](./01-executive-summary.md) | Problem, outcomes, in/out of scope, 90-day pilot intent |
| [02-personas-and-workflows.md](./02-personas-and-workflows.md) | Personas, needs, and example agent workflows |
| [03-architecture-overview.md](./03-architecture-overview.md) | Hybrid Azure + on-prem component view |
| [04-data-model-and-integrations.md](./04-data-model-and-integrations.md) | Core entities and source system contracts |
| [05-mvp-scope-and-backlog.md](./05-mvp-scope-and-backlog.md) | Prioritised requirements, epics, and pilot releases |
| [06-risks-metrics-and-governance.md](./06-risks-metrics-and-governance.md) | Risks, evaluation gates, and 90-day plan |
| [prompt-template.md](./prompt-template.md) | Example agent prompt templates for key workflows |
| [sample-ticket-schema.json](./sample-ticket-schema.json) | Sample normalised ticket schema |
| [sample-tickets.json](./sample-tickets.json) | Synthetic normalised tickets across support and implementation clients |
| [sample-release-proposal.md](./sample-release-proposal.md) | Example agent-generated monthly release recommendation |
| [prompts/](./prompts/) | Focused prompt templates (release planning, risk detection) |
| [sample-outputs/](./sample-outputs/) | Corresponding grounded agent outputs for the prompts |

## Strategic Outcomes

- Unified view of all client engagements, risks, releases, budgets, and milestones.
- Assist Product and Project Managers with prioritisation, planning, and dependency management.
- Automate preparation of monthly maintenance releases and readiness assessments.
- Surface emerging delivery risks from Jira, Harvest, discussions, and technical signals.
- Execute approved administrative workflows while retaining human authority over scope, budgets, and production releases.

---

*Part of the Product & Delivery Leadership Portfolio.*
