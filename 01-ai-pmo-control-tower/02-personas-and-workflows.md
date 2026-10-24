# Personas and Example Workflows

## Key Personas

| Persona | Primary needs | AI-supported decisions |
|---------|---------------|------------------------|
| PMO Director | Portfolio performance, utilization, delivery confidence | Which clients need intervention? |
| Product Manager | Product roadmap, customer priorities, feature scope | What should enter the next release? |
| Project Manager | Plans, risks, dependencies, resources, budgets | Can we meet committed milestones? |
| Release Manager | Scope, readiness, deployment and rollback | Is the release ready for approval? |
| Support Lead | SLA, defects, customer tickets | What needs immediate attention? |
| Technical Lead | Architecture, migrations, module dependencies | What technical blockers affect delivery? |
| Finance / Resource Lead | Harvest actuals, allocation, forecasting | Are we over budget or over capacity? |
| Leadership | Cross-client reporting and strategic visibility | Where should we invest or intervene? |

Each persona receives a tailored workspace. The underlying data model and agent services remain shared.

## Example Workflow: Monthly Maintenance Release Planning

**Trigger:** Release Manager requests the proposed scope for the next monthly release.

1. Retrieve Jira tickets and release history.
2. Product Agent prioritises scope.
3. Resource Agent validates capacity.
4. Planning Agent estimates feasibility.
5. Risk Agent checks blockers.
6. If feasible → draft release plan with scope and schedule options.
7. Release Manager reviews and approves.
8. If approved → update authorised Jira records and record the decision with audit trail.
9. If not approved → return for revision.

**Required outputs:** Prioritised release scope, excluded tickets, capacity assumptions, test readiness, dependencies, forecast confidence, and an approval record.

## Example Workflow: Implementation Dependency Impact

When a migration reconciliation fails:

- Implementation Agent detects the event and links it to the milestone.
- Risk Agent evaluates affected successors.
- Planning Agent recalculates the schedule.
- Resource Agent identifies possible parallel activities.
- Supervisor generates recovery scenarios for the Project Manager (with evidence, cost implications, and approval requirements).

## Decision Extraction Principle

Discussions in Teams or Outlook are never treated as approved scope changes. The system extracts *candidate* decisions, links them to client and ticket, identifies the owner, and requests confirmation. Only after approval is the decision register or Jira updated.

