# AI-Powered Legacy Document Ingestion & RAG Chatbot Pipeline

## 🎯 Objective
Migrating away from legacy systems often leaves behind unstructured "dark data"—years of legacy documents, historical emails, and archived Jira tickets that engineering and product teams still need to query. This pipeline automated the extraction, indexing, and retrieval of legacy institutional knowledge during the GCP migration.

## ⚙️ Technical Architecture & Workflow
1. **Data Ingestion:** Batch ingestion of legacy documents, email dumps, and Jira database exports into secure GCP Cloud Storage buckets.
2. **Parsing & Extraction:** Processed via Python-based parsing pipelines leveraging **Vertex AI / Gemini models** to extract structured metadata, technical constraints, and undocumented system dependencies.
3. **Retrieval-Augmented Generation (RAG):** Embedded extracted text chunks into a vector database to power semantic search.
4. **Internal Chatbot Interface:** Built a lightweight, responsive developer UI using **Gradio / FastAPI** deployed securely on GKE.
5. **Verification & Baselining:** Manual sampling and cross-verification of AI-extracted answers against legacy subject matter expert (SME) knowledge to establish baseline retrieval accuracy before wide rollout.

## 📊 Business & Technical Impact
- **Reduced Discovery Time:** Cut technical research time for legacy integration rules from hours to seconds for internal engineering squads.
- **De-risked Migration:** Surfaced undocumented legacy edge cases and hidden API contracts early in the migration planning phase.
