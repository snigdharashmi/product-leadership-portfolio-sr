# Chatbot RAG Query Response

**User Query:** "What is the recommended strategy for migrating the Oracle billing database to GCP, and what are the known risks?"

**Retrieved Context Sources:**
* Private Jira Page: `MIG-104` (Legacy Billing DB Extraction & GoldenGate Replication Strategy)
* Architecture Runbook: `03-data-migration-and-looker/oracle-goldengate/runbooks/cutover-and-fallback.md`

**Generated Response (Gemini):**
Based on internal Jira tracking (`MIG-104`) and migration runbooks, the recommended strategy uses **Oracle GoldenGate** for real-time Change Data Capture (CDC) from the on-prem Oracle 19c database into GCP Cloud SQL.

**Key Risks & Considerations:**
1. **Timestamp Discrepancies:** Legacy tables store timestamps without explicit time zones; explicit conversion rules must be configured in the GoldenGate replicat parameters.
2. **Initial Load Window:** Transferring the 4.2TB historical baseline requires a scheduled maintenance window before enabling continuous CDC pumps.
