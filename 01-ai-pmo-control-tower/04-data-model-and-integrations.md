# Data Model and Integrations

## Source System Contracts

| System | Data ingested | Sync strategy | System of record |
|--------|---------------|---------------|------------------|
| Jira | Tickets, status, priorities, links, versions, comments, sprints | Webhooks + periodic reconciliation | Ticket workflow |
| Confluence | PRDs, requirements, meeting notes, decisions, runbooks | Incremental polling / events | Approved documentation |
| Harvest | Time entries, projects, people, tasks, effort | Scheduled incremental sync | Actual time |
| Outlook | Approved project emails, meetings, action items | Graph delta / notifications | Communications |
| Teams | Approved channel discussions, decisions, ticket references | Graph subscriptions / scoped reads | Discussions |
| Azure DevOps / CI-CD | Builds, deployments, test results, artifacts | Pipeline events / API | Technical delivery evidence |
| On-prem SQL / logs | Schema readiness, migration logs, environment checks | Local gateway events | Technical system state |

## Ingestion Pipeline (Summary)

1. **Acquire** — API, webhook, scheduled sync, or on-prem gateway  
2. **Validate** — Schema, malware screening, deduplication, source identity  
3. **Classify** — Client ownership, confidentiality, document type, permissions  
4. **Normalise** — Map to common PMO entities and relationships  
5. **Enrich** — Extract decisions, risks, dependencies, ticket references  
6. **Index** — Operational facts, searchable content, and provenance  
7. **Evaluate** — Quality checks and publish approved agent events  

The platform supports idempotent ingestion, source updates/deletions, reindexing, retries, and full auditability.

## Core Unified Data Model

| Entity | Essential fields |
|--------|------------------|
| Client | client_id, name, delivery_model, owner, access_policy |
| Project | project_id, client_id, baseline_start, baseline_end, budget |
| Workstream | track_id, project_id, type, lead, status |
| Ticket | ticket_id, source_id, severity, priority, status, estimate |
| Dependency | predecessor, successor, dependency_type, lag |
| Milestone | milestone_id, baseline_date, forecast_date, actual_date |
| Release | release_id, client_id, version, scope, planned_date, gate_status |
| Resource | resource_id, skills, availability, team |
| Effort | person, project, task, date, hours, source |
| Decision | decision_id, subject, approver, outcome, evidence |
| Risk | risk_id, probability, impact, owner, mitigation |
| Evidence | source_uri, source_version, timestamp, ACL, classification |

Every record carries tenant/client ownership, source provenance, and timestamps. Relationships between tickets, requirements, releases, milestones, and discussions form a project knowledge graph.

