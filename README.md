# ClaimFlow

ClaimFlow is an n8n-based claims automation system built for allied-health clinics.

The project was developed during the **n8n University Hackathon**, where it received the **People's Choice Award** and an **Honourable Mention**.

## Overview

ClaimFlow connects multiple stages of the claims process into automated workflows that retrieve clinic data, validate claim requirements, prepare submissions, and support follow-up and reconciliation.

## What It Does

### NDIS Claims
- Syncs participant information from Cliniko
- Retrieves invoices and invoice items
- Validates participant and claim information
- Checks support-item codes, pricing, and plan dates
- Supports simulated API-based claim submission
- Reconciles remittance outcomes
- Monitors ageing claims and failed workflows

### Workers Compensation
- Retrieves invoice and funding information
- Supports claim validation and review
- Assists with Allied Health Treatment Request (AHTR) preparation
- Generates and populates AHTR documents
- Routes claims for review and follow-up

## Workflows

| Workflow | Purpose |
|---|---|
| `ndis-claims-intake-validation.json` | Retrieves and validates NDIS claims |
| `ndis-participant-sync.json` | Syncs NDIS participant information from Cliniko |
| `ndis-api-submission-simulated.json` | Simulates API-based NDIS claim submission |
| `ndis-remittance-reconciliation.json` | Reconciles claim and payment outcomes |
| `ndis-claims-ageing-check.json` | Identifies unresolved or ageing claims |
| `ndia-api-simulator-mock.json` | Mock NDIA endpoint used during development |
| `workers-comp-invoice-processing.json` | Processes and validates workers compensation invoices |
| `ahtr-assistant.json` | Assists with Allied Health Treatment Request preparation |
| `ahtr-template-loader.json` | Loads AHTR templates for document generation |
| `claims-review.json` | Supports review and routing of pending claims |
| `claims-failure-alerts.json` | Generates alerts when workflows fail |

## Built With

- **n8n** — workflow orchestration
- **Cliniko API** — practice-management data integration
- **JavaScript** — validation and transformation logic
- **Webhooks & REST APIs** — workflow communication and simulated submissions
- **PDF.co** — document-generation workflow integration
- **Gmail integrations** — notifications and workflow outputs

## Repository Structure

```text
claimflow/
├── README.md
└── workflows/
    ├── ndis-claims-intake-validation.json
    ├── ndis-participant-sync.json
    ├── ndis-api-submission-simulated.json
    ├── ndis-remittance-reconciliation.json
    ├── ndis-claims-ageing-check.json
    ├── ndia-api-simulator-mock.json
    ├── workers-comp-invoice-processing.json
    ├── ahtr-assistant.json
    ├── ahtr-template-loader.json
    ├── claims-review.json
    └── claims-failure-alerts.json
```

## Privacy & Configuration

These are sanitized workflow exports for portfolio/demo use.

- n8n credential references have been removed.
- Personal notification email addresses have been replaced with placeholders.
- Deployment-specific n8n webhook hostnames have been replaced with `YOUR_N8N_INSTANCE`.
- You will need to configure your own credentials and deployment URLs before running the workflows.

## Recognition

**People's Choice Award & Honourable Mention**  
n8n University Hackathon, 2026
