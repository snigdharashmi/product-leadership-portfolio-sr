02-cloud-migration-playbook/
├── README.md                                      # Playbook overview + links to both projects
│
├── 2.1-Legacy-to-GCP-Migration/
│   ├── README.md
│   ├── 01-executive-summary.md
│   ├── 02-current-state-assessment.md
│   ├── 03-risk-and-dependency-mapping.md
│   ├── 04-migration-strategy-and-waves.md         # 6Rs / 7Rs, prioritization
│   ├── 05-raid-log.md
│   ├── 06-hle-roadmap-and-milestones.md
│   ├── 07-governance-and-operating-model.md
│   ├── 08-cutover-and-rollback.md
│   ├── diagrams/
│   │   ├── gcp-architecture-flow.mmd              # (you already have this)
│   │   ├── dependency-map.mmd
│   │   └── ai-pmo-rag-pipeline.mmd                # (existing)
│   └── artefacts/
│       ├── sample-raid.csv                        # or .xlsx
│       └── legacy-document-ai-pipeline-spec.md    # (existing)
│
├── 2.2-AEM-6.5-to-AEMCaaS/
│   ├── README.md
│   ├── 01-executive-summary.md
│   ├── 02-assessment-bpa-and-gap-analysis.md      # Best Practices Analyzer, Cloud Acceleration Manager
│   ├── 03-code-refactoring-and-repository-modernizer.md
│   ├── 04-content-migration-strategy.md           # Content Transfer Tool, batches, deltas, top-ups
│   ├── 05-third-party-integrations.md             # Smartling + Akamai (and others)
│   ├── 06-raid-and-dependencies.md
│   ├── 07-cloud-manager-pipelines-and-cicd.md
│   ├── 08-cutover-go-live-and-hypercare.md
│   ├── 09-governance-and-operating-model.md
│   ├── diagrams/
│   │   ├── aem-target-architecture.mmd
│   │   ├── content-flow-smartling.mmd
│   │   ├── cdn-akamai-to-adobe.mmd
│   │   └── cutover-sequence.mmd
│   └── artefacts/
│       ├── bpa-findings-summary.md
│       ├── smartling-connector-migration.md
│       └── akamai-byocdn-checklist.md
│
└── shared/                                        # Optional but useful
    ├── templates/
    │   ├── raid-template.md
    │   ├── dependency-map-template.md
    │   └── hle-template.md
    └── frameworks/
        └── migration-governance.md
