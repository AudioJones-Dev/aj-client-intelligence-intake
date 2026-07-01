# Obsidian Vault Template

## Purpose

This folder defines the reusable Obsidian vault structure generated for each client.

## Generated Client Vault Goals

Each generated vault should support:

- Business overview
- AI receptionist retrieval
- CRM memory
- Sales process
- Operations knowledge
- Product/service documentation
- Human validation
- Live memory updates

## Required Vault Folders

```txt
00-HOME/
00-STRATEGY/
01-SPECIFICATION/
01.5-KNOWLEDGE-ENGINEERING/
02-QUALITY/
03-DELIVERY/
04-GOVERNANCE/
05-EXECUTION/
06-REFERENCE/
07-COMPANY/
08-PRODUCTS-SERVICES/
09-MANUFACTURERS/
10-KNOWLEDGE-BASE/
11-CRM/
12-SALES/
13-OPERATIONS/
14-FIELD-SERVICE/
15-CLIENT-SPECIFIC-PLATFORM/
16-BILLING/
17-AI-RECEPTIONIST/
18-RESPONSEOS/
19-MARKETING/
20-ANALYTICS/
21-MEETINGS/
22-RESEARCH/
23-MEDIA-LIBRARY/
24-PROJECTS/
25-AI-MEMORY/
26-TEMPLATES/
99-ARCHIVE/
```

## Standard Markdown Frontmatter

```yaml
---
title:
type:
category:
status:
owner:
created:
updated:
tags:
related:
summary:
entities:
retrieval_priority:
confidence:
source:
last_validated:
---
```

## Generation Rules

1. Do not generate unsupported facts.
2. Mark missing information as TODO.
3. Preserve confidence labels.
4. Create index files for major folders.
5. Optimize for AI retrieval and human review.
6. Keep generated content plain markdown.
