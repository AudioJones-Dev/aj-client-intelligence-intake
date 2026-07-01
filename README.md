# AJ Client Intelligence Intake

A reusable AJ Digital system for turning client discovery into deployable business memory.

This repo defines the repeatable pipeline for:

- Client intake
- Business context capture
- Knowledge gap detection
- AI receptionist setup
- CRM schema generation
- Obsidian vault generation
- ResponseOS deployment briefs
- Human validation workflows

## Core Thesis

Most AI receptionist and CRM deployments fail because the assistant is connected before the business has been modeled.

This system exists to extract, structure, validate, and maintain the client's operational knowledge before it is used by AI agents.

## Pipeline

```txt
Client Intake Form
→ Structured Intake Record
→ AI Follow-Up Interview
→ Knowledge Gap Detection
→ Obsidian Vault Generation
→ Human Validation
→ ResponseOS Deployment Brief
→ Live Business Memory Updates
```

## Recommended Repo Structure

```txt
aj-client-intelligence-intake/
├── README.md
├── docs/
│   ├── 00-STRATEGY/
│   ├── 01-SPECIFICATION/
│   ├── 02-QUALITY/
│   ├── 03-DELIVERY/
│   ├── 04-GOVERNANCE/
│   ├── 05-EXECUTION/
│   └── 06-REFERENCE/
├── schemas/
├── forms/
├── prompts/
├── templates/
├── examples/
└── scripts/
```

## First Example Client

The first implementation target is:

```txt
examples/florida-ramp-and-lift/
```

Florida Ramp & Lift should be treated as the reference client implementation for accessibility contractors, field-service operations, AI receptionist intake, CRM memory, contractor portal setup, billing rules, and ResponseOS deployment.

## Knowledge Maturity Model

Every captured fact should be classified as one of:

```txt
verified
client-stated
inferred
needs-review
unknown
```

AI agents should prefer `verified` and `client-stated` information over draft, inferred, or unknown information.

## Initial Build Priorities

1. Define intake schemas.
2. Define intake forms.
3. Define knowledge gap detection prompts.
4. Define Obsidian vault generator templates.
5. Create Florida Ramp & Lift reference implementation.
6. Produce a ResponseOS deployment brief from the completed context.

## Non-Goals

This repo should not become a client-specific operations repo.

Client-specific source material belongs in `examples/<client-name>/` or in the generated client vault.

This repo owns the reusable system, schemas, prompts, templates, and governance process.
