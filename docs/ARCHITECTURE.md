# oobAPPS Architecture

## Architecture principle

ChatGPT is a launch surface, not the system of record.

The core product must remain useful if the conversational platform, distribution model or app permissions change.

```text
Conversational surface
        |
        v
Recognition router
        |
        +---- selected public knowledge
        +---- module registry
        +---- bounded decision engines
        +---- result/artifact renderer
        |
        +---- optional user context store
        +---- de-identified pattern events
        +---- HubSpot relationship sync
        +---- commerce / entitlement
        +---- human-service routing
```

## Repository responsibilities

### oobAPPS

Owns the application layer:

- conversational routing
- context schemas
- shared app-safe knowledge
- application tools/interfaces
- result generation
- integrations
- app-specific privacy controls
- generalized pattern-event definitions

### oobSKILLS

Remains the web-first assessment and free-tool property.

Existing tested logic should be extracted into shared packages where practical rather than copied and independently rewritten.

### oobDISCOVERY

Remains the professional discovery system and methodological source for provenance, source integrity, evidence classes and business-type knowledge.

Its clinical project wording is not automatically public oobAPPS content.

### Private oobCREATIVE Project

Remains the broad exploratory and strategic environment.

Only deliberate downstream selections may become oobAPPS knowledge or instruction.

## Proposed repository structure

```text
oobAPPS/
├── README.md
├── AGENTS.md
├── apps/
│   ├── chatgpt/
│   └── web/
├── server/
│   └── mcp/
├── packages/
│   ├── recognition-context/
│   ├── conversational-router/
│   ├── decision-engines/
│   ├── assessment-modules/
│   ├── result-renderer/
│   ├── pattern-library/
│   └── analytics-events/
├── knowledge/
│   ├── brand/
│   ├── situations/
│   ├── services/
│   └── claims/
├── integrations/
│   ├── hubspot/
│   └── stripe/
├── docs/
└── tests/
```

Directories should be created as implementation requires them rather than adding empty scaffolding solely for appearance.

## Recognition Context

The reusable context object should be platform-neutral.

Working schema:

```yaml
context_version: 0.1
interaction_id:
user_context_id: null
situation:
  stated_problem:
  recognized_pattern:
  confidence:
  user_confirmed: false
trigger:
responsibility:
protected_value:
current_workaround:
friction:
reported_cost_or_consequence:
competing_priorities: []
desired_movement:
evidence: []
unknowns: []
next_decision:
provenance: []
consent:
  persist_context: false
  crm_relationship: false
```

This schema should distinguish the user's exact statement from structured interpretation.

## Provenance classes

Adapt the useful oobDISCOVERY distinction between source and interpretation.

Each structured field should be able to identify a source class such as:

- `user_explicit`
- `user_selected`
- `document_source`
- `deterministic_result`
- `working_hypothesis`
- `human_verified`
- `unknown`

Do not silently promote a working hypothesis to confirmed user context.

## Pattern knowledge evidence

Reusable pattern-library entries should identify their status:

- established / sourced knowledge
- repeated project pattern
- working hypothesis
- project-specific fact
- unknown / research gap

Project-specific facts do not automatically become generalized knowledge.

## Decision-engine boundary

Where an existing deterministic engine determines a result, keep the model out of that decision path.

Preferred flow:

```text
natural-language conversation
        ↓
structured input
        ↓
tested decision engine
        ↓
structured result
        ↓
LLM explanation / clarification
```

Avoid:

```text
conversation
        ↓
unbounded model interpretation
        ↓
confident recommendation
```

## Module contract

Every assessment module should expose the same conceptual contract:

```text
metadata
questions / required inputs
validation
normalized input
bounded evaluation
structured result
artifact renderer
next-step candidates
```

The website and ChatGPT implementations should consume this contract.

## Conversation router

The router's job is not to diagnose the person. Its job is to identify which bounded reasoning tool, if any, can help with the situation being described.

Required router behaviors:

- propose rather than force a pattern
- ask the minimum question necessary to resolve material ambiguity
- allow the user to reject the initial interpretation
- route to no module when none is useful
- preserve stated user language separately from derived labels
- avoid exposing internal persona labels

## Data separation

Maintain four logical data classes.

### 1. Ephemeral interaction context

Used to complete the current request. Do not persist by default merely because the app received it.

### 2. Saved user context

Created only through deliberate continuity actions. Must be viewable, correctable, exportable and deletable where technically supported.

### 3. Generalized pattern events

Derived, de-identified signals used to improve questions, routing and methods. Prefer structured signals over raw conversation storage.

### 4. CRM relationship data

HubSpot receives consented, commercially relevant relationship facts. Do not use the CRM as a transcript archive.

## HubSpot trigger

Do not create a CRM contact solely because an anonymous user completes a free interaction.

Appropriate triggers include:

- save my result
- email/send my workfile
- remember this context
- purchase
- request human help

The user should understand what is being stored when the relationship begins.

## File handling

Default design target:

**process source → derive needed information → discard source**

Persist uploads only when the product explicitly requires persistence and the user understands the purpose.

Do not design the public app to accept patient medical records, identifying clinical records, donor lists, employee personnel records or other categories that materially change security/compliance requirements without a separate approved project.

## Pattern-learning pipeline

```text
private expression
      ↓
structured situation signal
      ↓
user confirmation / correction
      ↓
de-identified event
      ↓
pattern candidate
      ↓
human review
      ↓
promoted reusable knowledge
```

Repeated occurrence is evidence worth examining, not automatic truth.

## Platform portability

ChatGPT-specific code should remain under `apps/chatgpt/` and the relevant server adapter.

Core schemas, decision engines, public knowledge and result structures must not require ChatGPT-specific APIs.

A web fallback should remain a first-class implementation, not an emergency page.
