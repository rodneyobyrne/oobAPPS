# oobAPPS

oobAPPS is the application layer for oobCREATIVE conversational tools and reusable decision systems.

The first product direction is a conversational communications system that can recognize a work situation, provide useful bounded help, preserve context only when the user chooses, and route higher-intent or higher-complexity work toward an appropriate product or human oobCREATIVE service.

## Core operating model

**Conversation → recognition → useful work → optional saved relationship → recurring utility → product/service escalation**

ChatGPT is an important launch surface, but it is not the product's source of truth. oobCREATIVE owns the underlying methods, decision logic, public knowledge, context schemas, artifacts, customer relationships, and service pathways.

## Repository role

This repository may contain:

- ChatGPT / conversational app code
- MCP and application-server interfaces
- reusable decision-engine packages
- public situation-recognition logic
- result and artifact schemas
- app-safe oobCREATIVE brand/voice guidance
- privacy and provenance rules
- HubSpot and commerce integration code
- tests and launch documentation

It must not become a copy of Rodney O'Byrne's private oobCREATIVE ChatGPT Project.

## Related systems

- **oobSKILLS** — public self-guided assessments and tested decision logic
- **oobDISCOVERY** — professional discovery methodology, provenance and evidence architecture
- **oobCREATIVE private Project** — broad private strategy and creative exploration; downstream use only through selected handoffs
- **HubSpot** — customer relationship system of record when a user deliberately establishes a relationship

## First launch modules

The MVP should prove three different forms of useful intelligence before more modules are migrated:

1. Customer Flow Health
2. AI Workday Review
3. Audience Review

The user should not need to know which module to choose. Conversation should establish the situation, then route into the smallest useful structure.

## Development rule

Do not recreate existing material merely because the delivery surface changes. Every current asset should be classified in `docs/REUSE-REGISTER.md` before being rebuilt.

See:

- `AGENTS.md`
- `docs/PRODUCT.md`
- `docs/ARCHITECTURE.md`
- `docs/REUSE-REGISTER.md`
- `docs/LAUNCH-PLAN.md`
