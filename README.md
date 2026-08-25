# Fuuz Integration Orchestrator

A small, generic message-routing and staging application built on the [FUUZ](https://fuuz.app) platform for connecting a Fuuz tenant to external ERP/host systems — the foundation other accelerators (MES, WMS, CMMS, QMS) build their integration flows on top of.

## The Scenario

A Fuuz tenant needs a consistent, auditable way to exchange messages with external systems — an ERP, a host, or another platform — without every accelerator inventing its own integration pattern. The Integration Orchestrator provides a single configuration surface, message staging table, and dashboard that other Fuuz accelerators' packaged integration flows route through.

## One Application, One Platform

**Package:** `Integration Orchestrator@0.0.9.fuuz`

| Component | Count |
|---|---|
| Data Models | 6 |
| Screens | 5 |
| Data Flows | 4 |
| Document Designs | 0 |
| Seeded Reference Data Sets | 6 |

Built against **platform version 2026.7.0**.

## 6 Data Models

| Category | Models | What They Track |
|---|---|---|
| **Integration** | IntegrationConfiguration, IntegrationMessage, IntegrationMessageType, IntegrationStaging, IntegrationType, StagingTableStatus | Per-system integration configuration, the messages exchanged, and their staging-table lifecycle |

## 5 Screens

- **Integration Setup** — define an Integration Configuration and Integration Type per external system
- **Integration Transactions** — review individual integration messages
- **Manage Integration Configuration** — configuration management screen
- **Manage Integration Type** — integration type management screen
- **Integration Dashboard** — live monitoring across all configured integrations

## 4 Data Flows

- **Integration: Main Handler** — top-level message routing
- **Integration: Main Flow Request Handler** — request handling for integration flows
- **Int_Outbound App Tenant Request Handler** — outbound request handling to the source tenant
- **Integration Orchestrator Dashboard** — dashboard data flow

## Seeded Reference Data

This package ships seeded values for `Sequence`, `Topic`, `StagingTableStatus`, `IntegrationMessageType`, `ModuleGroup`, and `Module`.

## Getting Started

### Import into FUUZ

1. Request a [free trial of FUUZ](https://forms.zohopublic.com/mfgxonlinesaas/form/TrialNotificationForm/formperma/syUyoccvUH7Ef5DaReDpfM48vuKiZtaGfYN18JPPu9k)
2. Navigate to **Fuuz Packages**
3. Upload `Integration Orchestrator@0.0.9.fuuz`
4. Review the import preview and confirm
5. Use the Integration Setup screen to define an Integration Configuration and Integration Type for each external system, then monitor message flow via the Integration Dashboard

### Explore the Package

Each `.fuuz` file is a gzipped tarball containing three JSON files:

```bash
mkdir extracted && cd extracted
tar -xzf "../Integration Orchestrator@0.0.9.fuuz"

ls -lh
# manifest.json      - Package metadata (name, version, dependencies)
# definition.json    - Module groups, modules, and enum seed data
# package-data.json  - Data models, screens, flows, and seed data
```

## Requirements

- A Fuuz Industrial Intelligence Platform tenant, platform version 2026.7.0 or later

## Resources

| Resource | Link | Description |
|---|---|---|
| **Free Trial** | [fuuz.app](https://forms.zohopublic.com/mfgxonlinesaas/form/TrialNotificationForm/formperma/syUyoccvUH7Ef5DaReDpfM48vuKiZtaGfYN18JPPu9k) | Request your free trial of FUUZ |
| **Get Started** | [getstarted.fuuz.com](https://getstarted.fuuz.com) | Introductory videos and walkthroughs |
| **FUUZ Academy** | [academy.fuuz.com](https://academy.fuuz.com) | Online LMS with structured courses and certifications |
| **Support & Community** | [support.fuuz.com](https://support.fuuz.com) | Knowledge base, documentation, and customer community |

## License

© Fuuz. All rights reserved. This package is proprietary software provided for use with the Fuuz Industrial Intelligence Platform. Redistribution or use outside of a licensed Fuuz tenant is not permitted without express written permission.
