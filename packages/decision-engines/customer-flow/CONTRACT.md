# Customer Flow Health — Shared Decision Contract

Status: Phase 1 extraction contract. This document preserves the behavior that must survive when the existing oobSKILLS engine is made platform-neutral.

## Source

Current implementation:
`rodneyobyrne/oobSKILLS/assessments/customer-flow-review/decision-engine.js`

Current regression tests:
`rodneyobyrne/oobSKILLS/tests/test-customer-flow.cjs`

Do not change the decision model during extraction unless a separate reviewed change explicitly does so.

## Normalized input

The shared evaluator must accept the current decision inputs independent of browser form markup.

```js
{
  contactChannels: [],
  responseConfidence: '',
  missedCall: '',
  infoPlaces: [],
  historyEase: '',
  familiarPhrase: '',
  taskFrequency: {
    copy: '',
    reenter: '',
    check: '',
    remind: '',
    tell: '',
    handled: ''
  },
  adminTime: '',
  toolCategories: [],
  toolFeeling: '',
  growthChanges: [],
  paceMatch: '',
  improvementPriorities: [],
  yearConcern: '',
  changeTiming: '',
  slowPeriod: ''
}
```

Optional presentation-only fields such as business name do not belong in the scoring contract unless they are later proven to affect evaluation.

## Structured result

The evaluator must return a structured object that includes at minimum:

```js
{
  stage,
  stageName,
  summary,
  action,
  decision,
  flowFriction,
  scores: {
    communication,
    information,
    workflow,
    capacity,
    changePressure
  },
  statuses: {
    communication,
    information,
    workflow,
    capacity,
    changePressure
  },
  visibility,
  workingSignals,
  recognitionSignals,
  focusAreas,
  toolContext,
  usefulTools,
  beforeBuying
}
```

The shared package returns data. Website rendering, ChatGPT conversation, cards, Markdown and downloadable workfiles are separate adapters/renderers.

## Current stage states

1. Holding Up Well
2. Some Patchwork Is Showing
3. Successful but Stretched
4. People Are Bridging the Systems
5. Growth Is Amplifying the Gaps

## Required behavioral invariants

### Uncertainty is not failure
Unknown answers such as missed-call uncertainty, unknown administrative time, uncertainty about the tool stack and unknown future consequence must affect visibility rather than automatically increase friction.

### Quantity is not automatically dysfunction
More contact channels or more information locations alone must not raise friction scores.

### Preserve what works
A low-friction result must be able to recommend protecting the current operating model instead of manufacturing a technology project.

### Software is not the default answer
The engine must continue distinguishing workflow/information handoffs from software replacement and must preserve `before buying` safeguards.

### Human estimates remain estimates
Self-reported administrative-time estimates must not be converted into guaranteed savings or unsupported performance claims.

### Deterministic evaluation remains deterministic
Do not replace stage/scoring logic with LLM interpretation. LLMs may help collect conversational inputs and explain a structured result, but the bounded decision engine owns the evaluation where the current engine already does so.

## Regression fixtures required

Port the existing oobSKILLS cases for:
- Holding Up Well
- multiple channels without added friction
- uncertainty / Limited visibility
- Some Patchwork Is Showing
- Successful but Stretched
- People Are Bridging the Systems
- Growth Is Amplifying the Gaps

For every fixture, scores must remain within 0–100 and the structured arrays must remain present.

## Privacy boundary

The original browser implementation includes a separate test ensuring the assessment does not automatically transmit answers. In oobAPPS, transmission behavior will differ because the user is intentionally interacting with a remote app, but the principle remains:

- do not silently persist assessment inputs;
- distinguish transient processing from saved context;
- saving/CRM continuity requires the separately defined consent/data rules;
- do not treat network processing as permission to retain raw conversation or assessment data.

## Extraction completion gate

Extraction is complete only when:
1. current fixtures produce equivalent core outputs;
2. the shared evaluator has no dependency on DOM/browser presentation;
3. both a web adapter and future ChatGPT adapter can consume the same result object;
4. no change to oobSKILLS customer-facing behavior is required merely to reuse the engine.
