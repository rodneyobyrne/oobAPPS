# Recognition Context v0.1

## Purpose

Recognition Context is the platform-neutral structure that lets oobAPPS preserve the useful meaning of a conversation without requiring the system to treat the raw conversation itself as the permanent record.

It separates:

- what the user actually said;
- what the system recognized;
- what the user confirmed or corrected;
- what is supported by evidence;
- what remains unknown;
- what action is useful next.

This is not a psychological profile.

## Core principle

**Recognize patterns. Confirm with people. Preserve only what is useful.**

## Working schema

```yaml
context_version: "0.1"
interaction_id: ""
user_context_id: null
created_at: ""
updated_at: ""

source:
  user_statement: ""
  source_type: "conversation"

situation:
  pattern_id: ""
  label: ""
  confidence: null
  user_confirmed: false
  correction: null

trigger:
  value: null
  provenance: "unknown"

responsibility:
  value: null
  provenance: "unknown"

protected_value:
  value: null
  provenance: "unknown"

current_workaround:
  value: null
  provenance: "unknown"

friction:
  items: []

reported_cost_or_consequence:
  items: []

competing_priorities:
  items: []

desired_movement:
  value: null
  provenance: "unknown"

evidence:
  items: []

unknowns:
  items: []

module:
  selected: null
  selection_reason: null

result:
  result_id: null
  result_type: null
  summary: null
  decision: null

next_decision:
  value: null

consent:
  persist_context: false
  create_crm_relationship: false
  permit_follow_up: false
```

The implementation may use JSON/TypeScript rather than YAML. This document defines meaning, not wire format.

## Provenance values

Every field that could be mistaken for a fact should be able to identify its basis.

Recommended values:

- `user_explicit` — user stated it directly
- `user_selected` — user chose it from a structured option
- `document_source` — supported by supplied source material
- `deterministic_result` — produced by a tested bounded engine
- `model_interpretation` — derived by the conversational model
- `working_hypothesis` — plausible but unconfirmed
- `human_verified` — reviewed/confirmed through a human process
- `unknown` — intentionally unresolved

## Important distinctions

### Situation is not identity

A situation record describes what appears to be happening in the current work context.

It must not become a permanent statement about what kind of person the user is.

### Protected value must be supported

The system may notice that a situation often involves protecting quality, trust, mission, autonomy or another value.

Do not silently store that as the user's protected value.

Ask a confirming question or leave it unknown.

### Unknown is valid

The system should not optimize for complete profiles.

If a field is not necessary to help with the current decision, it can remain unknown.

### Corrections matter

A user correction is high-value information.

Store the corrected context for the current interaction and, if the user has opted into saved context, update the saved record.

For generalized pattern learning, a correction event can be useful without retaining the user's identity or raw statement.

## Context lifecycle

### Ephemeral

Created during a conversation and discarded after the interaction unless the user deliberately chooses continuity.

### Saved

The user chooses to preserve some context because it will improve future work.

Saved context should contain only fields useful for continuity.

### CRM

A CRM relationship should not receive every Recognition Context field.

Only consented, commercially relevant fields should be mapped to HubSpot.

### Pattern intelligence

Generalized pattern learning should receive a reduced event representation, for example:

```yaml
situation_pattern: "growth-customer-flow"
route_proposed: "customer-flow-health"
route_confirmed: true
clarification_required: true
user_corrected: false
module_completed: true
result_state: "successful-but-stretched"
next_action_category: "review-handoffs"
usefulness_feedback: null
```

No identity or raw transcript is required for this event to be useful.

## Pattern-library relationship

Recognition Context describes one current interaction.

The pattern library contains reusable knowledge developed across research and repeated evidence.

Pattern knowledge may suggest:

- likely questions to ask;
- distinctions worth testing;
- possible structural explanations;
- appropriate bounded modules;
- likely trust/decision concerns to confirm.

Pattern knowledge may not override the current user's description.

## Minimum-necessary rule

Do not collect a context field simply because it could be interesting later.

Collect or derive it when it materially improves:

- the current answer;
- routing;
- safety/privacy;
- a user-requested saved relationship;
- a defined product/service action.

## Future extension

Versioned additions may include:

- organization-level context separate from individual context;
- multiple decision roles;
- source-document evidence references;
- reusable system/tool inventory;
- time-bound context expiration;
- explicit confidence calibration;
- cross-surface continuity between ChatGPT, web and phone interactions.

Do not add these until a real product need justifies the additional data and complexity.
