# Product Requirements Document

## Product Name

AJ Client Intelligence Intake

## Summary

A reusable intake and knowledge-engineering system that captures client business context, identifies missing information, generates structured Obsidian vaults, and prepares ResponseOS deployment briefs.

## Primary Users

- AJ Digital strategist
- Client founder/operator
- Implementation agent
- Codex/Claude build agent
- ResponseOS deployment operator
- AI receptionist configuration agent

## Core Jobs To Be Done

### 1. Capture Client Context

Collect company profile, services, customers, operations, sales process, tools, service areas, team members, documents, and AI receptionist rules.

### 2. Detect Knowledge Gaps

Analyze intake responses and identify missing information required for reliable AI receptionist, CRM, and operations workflows.

### 3. Generate Business Memory

Create a structured Obsidian vault with client-specific context, source labels, confidence levels, and retrieval-friendly markdown.

### 4. Prepare AI Deployment

Generate ResponseOS deployment briefs, AI receptionist prompts, escalation rules, lead qualification flows, and CRM context documents.

### 5. Maintain Knowledge Over Time

Support post-launch updates from calls, CRM events, field notes, owner decisions, and human corrections.

## Required Modules

```txt
1. Intake Forms
2. Intake Schemas
3. AI Follow-Up Interview Prompts
4. Knowledge Gap Detector
5. Vault Generator Templates
6. ResponseOS Deployment Brief Generator
7. Validation Workflow
8. Client Example Implementations
```

## Required Artifacts Per Client

```txt
client-profile.json
service-catalog.json
crm-model.json
ai-receptionist-config.json
knowledge-gap-report.md
obsidian-vault/
responseos-deployment-brief.md
validation-checklist.md
```

## Non-Functional Requirements

- Markdown-first
- Git-compatible
- Obsidian-compatible
- AI retrieval optimized
- Source and confidence aware
- Repeatable across clients
- Human validation required before production use

## Out of Scope For v1

- Full SaaS UI
- Payment processing
- Live CRM syncing
- Native telephony integration
- Production ResponseOS runtime deployment

## v1 Success Criteria

- Florida Ramp & Lift can be onboarded using the process.
- The system can generate a usable Obsidian vault skeleton and seeded context package.
- The system can identify missing business context before AI receptionist deployment.
- The resulting knowledge base can support a demo AI receptionist conversation accurately.
