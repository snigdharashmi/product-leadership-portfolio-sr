# Looker Data Mart Executive Summary

| Data Mart | Source Table(s) | Row Count Synced | Latency | Looker Dashboard |
| :--- | :--- | :--- | :--- | :--- |
| `mart_billing_transactions` | `ORA_BILLING.TXN_HEADER` | 48,291,038 | 1.2s | Executive Revenue & Billing Pulse |
| `mart_customer_accounts` | `ORA_BILLING.CUST_MASTER` | 1,420,500 | 0.8s | Customer 360 & Churn Telemetry |
| `mart_unstructured_doc_index` | `GCS://legacy-docs-parsed/` | 12,840 docs | Batch (15m) | RAG Knowledge Coverage & Audit |
