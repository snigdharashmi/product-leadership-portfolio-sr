# MVP Scope and Backlog

## Priority Functional Requirements (Selected)

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-01 | Connect and synchronise authorised Jira projects | P0 |
| FR-02 | Index approved Confluence pages with citations | P0 |
| FR-03 | Reconcile Harvest actual hours to project tasks | P0 |
| FR-04 | Maintain six client-specific workspaces | P0 |
| FR-05 | Generate portfolio and client status summaries | P0 |
| FR-06 | Identify overdue tickets, blockers, and SLA risks | P0 |
| FR-07 | Generate proposed monthly maintenance release scope | P0 |
| FR-08 | Calculate task dependencies and critical path | P0 |
| FR-14 | Support natural-language PMO questions | P0 |
| FR-15 | Present evidence, timestamps, and assumptions | P0 |
| FR-20 | Log all AI recommendations and executed actions | P0 |

## Example User Stories (with Acceptance Criteria)

**US-01 — Consolidated portfolio health**  
As a PMO Director, I want to see the health of all six clients so I can identify engagements requiring intervention.  
*Acceptance:* Authorised clients appear with baseline and forecast dates, key risks, data freshness, accountable owners, and links to source evidence.

**US-02 — Monthly release recommendations**  
As a Release Manager, I want AI to recommend a feasible release scope based on priority, capacity, dependencies, and readiness.  
*Acceptance:* Proposal includes included/excluded tickets, estimated effort, QA capacity, blocking dependencies, rationale, and an approval workflow.

**US-08 — Controlled agent execution**  
As a Project Manager, I want to approve proposed Jira updates before they are applied.  
*Acceptance:* Agent shows a before/after diff, checks current record versions, requires authorisation, and records the execution result.

## Proposed Pilot Release Slices

| Release | Focus |
|---------|-------|
| **M1 — Pilot** | Jira + Confluence + Harvest, client segregation, grounded Q&A, portfolio dashboard |
| **M2 — Delivery Intelligence** | One support release workflow, one implementation dependency workflow, status reports, risk register |
| **M3 — Supervised Automation** | Scoped Teams/Outlook extraction, approval-based Jira changes, additional dashboards |

## High-Level Epics (Effort in person-days — preliminary)

| Epic | Priority | Effort |
|------|----------|--------|
| Platform Foundation | P0 | 18 |
| Identity & Security | P0 | 20 |
| Data Connectors | P0 | 40 |
| PMO Data Platform | P0 | 25 |
| Knowledge & RAG | P0 | 24 |
| Agent Orchestration | P0 | 30 |
| Support & Release | P0 | 28 |
| Implementation Intelligence | P0 | 30 |
| Dashboards & UX | P0 | 30 |
| Approval Workflows | P1 | 18 |
| Testing & Hardening | P0 | 30 |
| Pilot & Rollout | P0 | 15 |
| **Total** | | **308** |

A practical 90-day pilot delivers selected vertical slices rather than the full backlog.

