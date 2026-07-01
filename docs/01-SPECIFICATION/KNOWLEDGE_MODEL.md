# Knowledge Model

## Purpose

This document defines how client knowledge should be captured, classified, validated, stored, and retrieved.

## Core Principle

The system must distinguish between what is known, what is client-stated, what is inferred, and what still needs validation.

## Knowledge Confidence Levels

```txt
verified       Confirmed by authoritative source or human review
client-stated  Provided by client but not independently validated
inferred       Reasoned from available context, requires review
needs-review   Potentially useful but not ready for production AI use
unknown        Missing or unresolved
```

## Standard Knowledge Record

Every durable business fact should be representable as:

```json
{
  "fact": "string",
  "domain": "company | service | crm | sales | operations | billing | ai_receptionist | technical | marketing",
  "source": "string",
  "confidence": "verified | client-stated | inferred | needs-review | unknown",
  "owner": "string",
  "last_validated": "YYYY-MM-DD",
  "related_entities": ["string"],
  "retrieval_priority": "high | medium | low",
  "notes": "string"
}
```

## Required Knowledge Domains

```txt
company
services
products
manufacturers
customers
crm
sales
operations
billing
ai_receptionist
field_service
marketing
analytics
governance
```

## Retrieval Priority

### High

Knowledge that an AI receptionist or operational agent may need in live customer interaction.

Examples:

- Services offered
- Service area
- Escalation rules
- Emergency handling
- Booking rules
- Customer qualification rules

### Medium

Knowledge useful for sales, operations, or internal workflow.

Examples:

- Pricing logic
- CRM stages
- Contractor onboarding
- Manufacturer preferences

### Low

Background knowledge useful for context but not usually needed during real-time interaction.

Examples:

- Strategic history
- Internal roadmap
- archived decisions

## Required Metadata For Markdown Notes

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

## AI Behavior Rule

AI agents must not treat `inferred`, `needs-review`, or `unknown` content as authoritative.

When uncertain, the agent should either:

1. Ask a follow-up question.
2. Escalate to a human.
3. State that the business will confirm details.

## Source Hierarchy

```txt
1. Human-approved source-of-truth documents
2. Client-stated interview answers
3. Existing business documents
4. Website and public data
5. CRM/call/field records
6. AI-generated summaries
7. Inferences and assumptions
```

## Validation Requirement

Before a client vault powers a live AI receptionist, these areas must be human-reviewed:

- Business overview
- Service offerings
- Service areas
- Emergency escalation
- Scheduling rules
- Pricing disclaimers
- Sales promises
- Legal/compliance disclaimers
- Do-not-say rules
