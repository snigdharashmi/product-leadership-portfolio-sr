# Architecture Overview

## Recommended Pattern

Azure-hosted AI orchestration with controlled on-premises data access. Sensitive legacy systems and operational records can remain on-premises; permitted metadata and documents are processed by Azure AI services.

## High-Level Layers

**User Experience Layer**  
PMO Web Portal · Teams Copilot · Power BI · Approval Inbox

**Azure Application and Agent Layer**  
API Gateway · Agent Orchestrator · Agent Tool Services · Workflow Engine · Policy & Approval Engine · Notification Service

**AI Intelligence Services**  
Azure OpenAI · RAG · Semantic Search · Dependency Reasoning · Forecasting

**Cloud Data Services**  
Azure SQL / PostgreSQL · Blob Storage · Azure AI Search · Audit Logs

**Connectivity**  
ExpressRoute / Site-to-Site VPN

**On-Premises Integration Zone**  
Integration Gateway · Local Data Connectors · Legacy SQL / Files · Deployment Logs · Local Secrets / Policies · Outbound Event Publisher

**External Systems**  
Jira · Confluence · Harvest · Outlook · Teams · Azure DevOps / CI-CD

## Component Responsibilities (Summary)

| Component | Responsibility | Proposed deployment |
|-----------|----------------|---------------------|
| React / Node.js portal | Dashboards, conversational UI, approvals | Azure App Service / Container Apps |
| Agent orchestration | Route tasks and coordinate specialist agents | Azure containers |
| Workflow engine | Durable approvals, retries, long-running tasks | Azure Functions / Durable Functions |
| LLM inference | Summarisation, reasoning, extraction | Azure OpenAI |
| Retrieval engine | Hybrid keyword and vector search | Azure AI Search |
| Operational database | Normalised portfolio and workflow records | Azure SQL / PostgreSQL |
| Document store | Approved source copies and processed documents | Azure Blob Storage |
| Integration gateway | Controlled access to local services | On-premises container / VM |
| Identity and secrets | SSO, workload identity, secrets | Entra ID / Key Vault |

## Data Classification Policy

| Data classification | Processing strategy |
|---------------------|---------------------|
| Internal operational metadata | Cloud processing allowed |
| Client-confidential documents | Cloud processing only with client and security approval |
| Restricted / on-prem-only information | Local processing or sanitised derived metadata only |

**Note:** Prompts, embeddings, extracted text, logs, backups, and telemetry must all be included in the data-classification assessment.

