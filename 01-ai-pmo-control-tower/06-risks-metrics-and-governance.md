# Risks, Metrics, and Governance

## Key Risks and Mitigations

| Risk | Mitigation |
|------|------------|
| Inconsistent Jira project structures | Canonical taxonomy and mapping rules |
| Unstructured Teams discussions | Scoped ingestion, ticket linking, and decision confirmation |
| Incomplete Harvest time tracking | Reconciliation and data-quality reporting |
| AI hallucinations | RAG citations, deterministic calculations, evaluation gates |
| Client confidentiality breaches | Client isolation, ACL enforcement, adversarial tests |
| Incorrect schedule forecasts | Validated dependency graph, calendars, baseline controls |
| Low PM adoption | Start with high-value workflows; integrate with existing tools |
| Uncontrolled AI execution | Least-privilege tools and human approvals |
| Platform costs exceed savings | Usage budgets, model routing, ROI reviews |

## Evaluation Gates (Pilot Investment)

| Gate | Criterion |
|------|-----------|
| **Gate 1 — Data readiness** | ≥95% of required pilot records ingested correctly with verified client ownership and permissions |
| **Gate 2 — AI usefulness** | ≥90% of benchmark answers factually correct with valid source evidence; zero critical access violations |
| **Gate 3 — Operational impact** | Demonstrated reduction in manual PMO effort and acceptable recommendation quality across both delivery models |
| **Gate 4 — Controlled rollout** | Security sign-off, operational ownership, rollback plan, monitoring, and approval workflows verified |

## Non-Functional Targets (Design Proposals)

- Availability: 99.5% monthly (pilot)
- Dashboard performance: P95 < 3 seconds (cached views)
- AI response time: P95 < 15 seconds (grounded queries)
- Data freshness: Jira events < 5 minutes; Harvest < 60 minutes
- Access control: Client-scoped authorisation on every query and tool call
- Audit: Complete trace for approved writes and material decisions

## 90-Day Pilot Cadence (Summary)

| Sprint | Timeline | Deliverable / Exit Gate |
|--------|----------|-------------------------|
| Sprint 0 | Weeks 1–2 | Architecture, permissions, security, source inventory approved |
| Sprint 1 | Weeks 3–4 | Core connectors, normalised data, access tests |
| Sprint 2 | Weeks 5–6 | RAG, portfolio dashboard, grounded Q&A |
| Sprint 3 | Weeks 7–8 | Maintenance release and implementation agents |
| Sprint 4 | Weeks 9–10 | Forecasting, decision extraction, evaluations |
| Sprint 5 | Weeks 11–12 | Pilot UAT, supervised actions, hardening |
| Transition | Week 13 | Go/no-go, training, operations handover |

## Governance Forums

| Forum | Cadence | Decisions |
|-------|---------|-----------|
| AI Product Working Group | Weekly | Priorities, backlog, UX, acceptance |
| Delivery Steering Committee | Biweekly | Schedule, budget, risks, dependencies |
| Security & Architecture Review | Design and release gates | Access, compliance, technical exceptions |
| Model Evaluation Review | Every sprint | Accuracy, leakage tests, agent reliability |
| Pilot Go/No-Go Board | End of pilot | Production readiness and rollout |

