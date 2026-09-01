# oobAPPS Launch Plan

## Status

Working internal implementation plan for the first oobCREATIVE conversational communications product.

This document converts existing oobCREATIVE strategy, oobSKILLS tools, oobDISCOVERY methods and current platform opportunities into a staged launch program.

The plan assumes the public `oobAPPS` repository remains portable and does not contain the private oobCREATIVE Project source package.

---

# 1. Launch objective

Build and launch an oobCREATIVE conversational application that can perform appropriate-fidelity top-of-funnel communications work without requiring Rodney's involvement in every early interaction.

The product should:

1. meet a user inside an existing conversation;
2. recognize a relevant work or communication situation;
3. ask only enough additional questions to make the interaction useful;
4. invoke tested oobCREATIVE decision logic where available;
5. return a complete useful result;
6. allow the user to preserve useful context deliberately;
7. create a CRM relationship only after an intentional continuity or commercial action;
8. offer an automated product when the need is strong enough and the product genuinely advances the work;
9. route consequential, ambiguous or implementation-heavy work to human oobCREATIVE services;
10. improve reusable pattern knowledge without requiring a dossier of raw conversations.

The launch is successful if it proves the communication/funnel model. It does not need to prove every future app category.

---

# 2. Strategic premise

## Traditional collateral economics

Traditional top-of-funnel communications often require substantial work before any specific recipient has expressed intent:

**research → strategy → writing → design → production → distribution → exposure → recognition → inquiry**

The resulting flyer, brochure, guide, ad or worksheet is intentionally lower fidelity than a full consulting engagement because its job is to create recognition and move the right person toward the next step.

## Conversational collateral economics

Conversational systems can begin after a user has already expressed something about the problem.

**conversation → recognition → appropriate-fidelity help → useful result → greater intent → appropriate escalation**

The opportunity is not to make worse work cheaply.

The opportunity is to stop spending high-cost human resources on communication stages that do not require high-cost human judgment.

## oobCREATIVE advantage

The differentiation is not access to an LLM.

The differentiation is the combination of:

- human-centered communication strategy;
- existing persona/buying-state intelligence;
- recognizable situation design;
- tested decision engines;
- responsible technology boundaries;
- explicit evidence/provenance rules;
- ability to move from communication into real implementation when warranted.

---

# 3. Product model

Use this operating sequence:

**Conversation → oobCREATIVE recognition → useful work → optional saved relationship → recurring utility → automated product or human service escalation**

## Appropriate-fidelity levels

### Level 1 — Recognition

Purpose: establish whether the situation is relevant.

Typical behavior:

- recognize a repeated work pattern;
- make one useful distinction;
- ask one clarifying question if needed;
- route to the smallest useful next step.

Human cost target: near zero.

### Level 2 — Orientation

Purpose: help the user understand enough to make a better decision.

Typical output:

- explanation;
- boundary;
- options;
- what not to do yet.

### Level 3 — Structured useful result

Purpose: produce a concrete working result.

Typical output:

- assessment result;
- prioritized issues;
- workfile;
- pilot plan;
- message priorities;
- next decision.

### Level 4 — Automated paid product

Purpose: create deeper reusable implementation material without human delivery.

Examples may include:

- expanded action pack;
- AI implementation starter pack;
- customer-flow implementation worksheet;
- audience/message pack.

Do not choose the permanent catalog before beta evidence.

### Level 5 — Human review

Purpose: apply judgment where ambiguity, consequence or collaboration makes automation insufficient.

### Level 6 — Implementation

Purpose: deliver actual oobCREATIVE strategy, design, configuration, workflow, media or integration work.

### Level 7 — Ongoing support

Purpose: maintain, improve or periodically reassess a system over time.

---

# 4. MVP scope

Launch with three modules only.

## 4.1 Customer Flow Health

Source: existing oobSKILLS Customer Flow Health Review.

Why it belongs in MVP:

- already contains a tested deterministic decision engine;
- demonstrates operational recognition;
- explicitly separates uncertainty/visibility from failure;
- can conclude that the business should protect what is working rather than buy technology;
- naturally routes into Communication Systems and Practical AI when implementation is justified.

Migration requirement:

- extract decision logic;
- normalize inputs/outputs;
- keep website behavior equivalent;
- add conversational intake adapter;
- standardize artifact output.

## 4.2 AI Workday Review

Source: existing oobSKILLS AI Workday Review.

Why it belongs in MVP:

- directly expresses the human + technology positioning;
- begins with one responsibility rather than an AI product;
- can conclude that work should remain human;
- already includes owner, review standard, permitted input guidance and stopping condition;
- creates a natural route to automated implementation materials or human AI/workflow services.

Migration requirement:

- separate core assessment logic from page presentation;
- create structured readiness result;
- preserve human-ownership language;
- create conversational questions that do not over-interrogate the user.

## 4.3 Audience Review

Source: existing oobSKILLS Audience Review.

Why it belongs in MVP:

- demonstrates recognition and communication strategy rather than only operations;
- creates a bridge to message, positioning, website and campaign services;
- allows the product to prove that the platform is broader than "AI consulting."

Migration requirement:

- preserve current useful drafts/result behavior;
- refactor questions into reusable module contract;
- distinguish user-supplied customer knowledge from oobCREATIVE interpretation;
- create appropriate conversational sequence.

---

# 5. Conversation router

The router is the defining new product component.

Users should not be greeted with a catalog of assessments.

## Required behavior

1. Read only the context needed for the current task.
2. Identify a plausible situation family.
3. Determine whether an existing module can help.
4. Ask one focused question when ambiguity materially affects routing.
5. Confirm the situation rather than silently classify the person.
6. Invoke the relevant module.
7. Allow correction at any point.
8. Offer "none of these" behavior when the existing tools do not fit.

## Initial situation families

Seed the router with public-safe patterns already reflected in oobCREATIVE strategy:

- too much work or judgment still depends on one person;
- work is difficult to explain without losing meaning;
- communication has become structurally chaotic;
- customers do not understand the value of expertise;
- an organization wants a practical, responsible use of AI;
- an existing project has stalled or failed;
- an idea is ready for a bounded test;
- customer information/follow-up is becoming harder as the business grows.

These are routing seeds, not public products and not personality labels.

---

# 6. Recognition Context v0.1

Create a platform-neutral structured context object.

Minimum fields:

- stated situation;
- recognized situation pattern;
- confidence;
- user confirmation/correction;
- trigger;
- responsibility;
- protected value when explicitly supported;
- current workaround;
- structural friction;
- reported cost/consequence;
- competing priorities;
- desired movement;
- evidence;
- unknowns;
- next decision;
- provenance;
- consent state.

## Design rule

Store the user's exact statement separately from structured interpretation.

Do not present inferred emotion or personality as fact.

The system may recognize how a situation is framed when that framing is relevant to the task, but should convert that into a useful confirmation question rather than a hidden psychological profile.

---

# 7. Privacy model

## Principle

Privacy and pattern learning are separate concerns.

The app should be able to learn from recurring structures without retaining every raw expression or tying pattern intelligence to identity.

## Four data classes

### Ephemeral interaction

Used for the current request.

Default: do not persist raw conversation merely because it was available.

### Saved user context

Created through deliberate continuity actions.

The user should be able to understand what is saved and, where technically supported, view, correct, export and delete it.

### Pattern events

De-identified structured signals used to improve routing and methods.

Prefer fields such as:

- situation type;
- module chosen;
- correction occurred;
- clarifying question required;
- result state;
- next-action category;
- usefulness feedback.

Avoid raw transcript storage in the pattern layer by default.

### CRM relationship

HubSpot should contain consented relationship facts, not a transcript archive.

## Explicit non-MVP data categories

Do not design the public MVP to collect or retain:

- patient medical records;
- identifiable health information;
- donor lists;
- employee personnel files;
- secret credentials;
- customer databases uploaded wholesale;
- other data categories that materially expand compliance/security obligations.

---

# 8. Relationship and CRM strategy

Anonymous/free use should remain possible where practical.

Do not create a HubSpot contact solely because someone completed a free interaction.

A relationship begins when the user deliberately asks for continuity or commercial action.

## Suggested triggers

- save my result;
- remember this context;
- send/email my workfile;
- purchase a product;
- ask oobCREATIVE for help.

## HubSpot fields to design

- source = oobAPPS / ChatGPT / web;
- first relationship date;
- organization where supplied;
- module completed;
- confirmed situation category;
- desired movement;
- saved-result ID;
- product purchased;
- human-help requested;
- consent scope;
- lifecycle stage.

Do not synchronize private model hypotheses into HubSpot as facts.

---

# 9. Pattern intelligence and governance

Use the strongest reusable idea from oobDISCOVERY: keep source, interpretation and promoted knowledge distinct.

## Pattern evidence statuses

- established / sourced;
- repeated project pattern;
- working hypothesis;
- project-specific fact;
- unknown / research gap.

## Promotion flow

```text
interaction
  ↓
derived signal
  ↓
user confirmation/correction
  ↓
de-identified event
  ↓
pattern candidate
  ↓
human review
  ↓
reusable oobCREATIVE pattern knowledge
```

Repeated occurrence does not automatically become truth.

A business-type or situation pattern should help the app ask sharper questions, not force a new user into an inherited model.

---

# 10. Technical architecture

## 10.1 Core packages

Create only as implementation begins:

- `packages/recognition-context`
- `packages/conversational-router`
- `packages/decision-engines`
- `packages/assessment-modules`
- `packages/result-renderer`
- `packages/pattern-library`
- `packages/analytics-events`

## 10.2 ChatGPT surface

Keep ChatGPT-specific implementation isolated under `apps/chatgpt`.

The app should use a remote application/MCP server and interactive components where structured UI is more useful than prose.

## 10.3 Web fallback

Keep web as a first-class product surface.

Reasons:

- current oobSKILLS already works on the open web;
- search/SEO/LLM retrieval remain valuable;
- ChatGPT app availability can vary by product surface, plan and platform changes;
- oobCREATIVE must retain a distribution path it controls.

## 10.4 Shared module contract

Every migrated module should expose:

- metadata;
- required inputs;
- questions;
- validation;
- normalization;
- bounded evaluation;
- structured result;
- artifact rendering;
- relevant next-step candidates.

Both web and ChatGPT should consume the same contract.

## 10.5 File input spike

Before promising upload-driven products, test exactly what an app can access from files shared in the ChatGPT conversation.

Test:

1. user uploads file;
2. user invokes oobCREATIVE app;
3. determine available content and metadata;
4. determine whether a secure external upload is needed;
5. document retention/deletion behavior.

Fallback: temporary oobCREATIVE upload path with explicit source-file lifecycle.

---

# 11. Creative strategy

## Brand behavior

Use selected public brand principles:

- Go Deeper, Not Louder.
- Start with what matters and what is at stake.
- Preserve human agency and judgment.
- Keep technology connected to a specific responsibility.
- Give useful information before asking for a sale.
- Clarify without flattening.
- Avoid hype, manipulation and unsupported promise.

## Conversational sequence

Preferred:

**recognition → useful distinction → minimum clarification → answer → context → choice**

Avoid:

**diagnosis → escalating pain → sales pressure**

## Visual strategy

Do not invent a new oobCREATIVE identity for the app.

Adapt existing oobSKILLS working language:

- open/light surfaces;
- black/ink;
- established blue accent where currently approved;
- outlined workfile/worksheet feel;
- hand-drawn entry cue where supported;
- current marks/logos only.

The source system does not yet contain a complete final typography/color/visual standard. Treat that as a known gap rather than silently finalizing one inside the app.

---

# 12. Existing content and asset migration

The full inventory lives in `REUSE-REGISTER.md`.

## Priority migration work

### Extract

- Customer Flow decision engine;
- common question/validation contract;
- structured result object;
- reusable result renderer.

### Adapt

- Customer Flow intake/result;
- AI Workday intake/result;
- Audience Review intake/result;
- current workfile outputs;
- oobDISCOVERY provenance rules;
- oobDISCOVERY business-type knowledge pattern.

### Redraft

- app-specific privacy policy;
- oobSKILLS hub language to introduce conversational use;
- tool pages to offer ChatGPT route;
- service pages to accept contextual app handoffs;
- CRM follow-up messages;
- app store/directory listing;
- paid-product descriptions after beta.

### Reuse as principle

- useful answer before lead capture;
- optional sharing;
- human responsibility;
- bounded scope;
- no unsupported claims;
- persona names internal only;
- recognize situations before services.

### Keep private

- full private Project history;
- private persona evolution;
- founder collaboration notes;
- unselected concepts;
- private client commentary;
- unverified proof.

---

# 13. Website changes

Do not sunset oobSKILLS.

After conversational MVP is stable:

## `/free-tools/`

Retain the complete public inventory for search and browsing.

Add a conversational route for users who prefer to describe the problem rather than choose a tool.

## `/assessments/`

Position as structured self-guided versions of oobCREATIVE reviews.

## Individual assessment pages

Retain the complete experience.

Add a conversational alternative where the same shared module exists.

## Services

App handoffs should deep-link to the most relevant bounded service family/path rather than a generic contact page whenever possible.

---

# 14. Commerce

Do not depend on native ChatGPT commerce for MVP viability.

Use oobCREATIVE-owned checkout and entitlement, initially expected to be Stripe-compatible.

## First automated product

Do not choose from preference alone.

Choose after beta based on:

- repeated user request;
- clear incremental value beyond free result;
- low/no human fulfillment;
- low support burden;
- strong connection to existing oobCREATIVE services;
- understandable bounded output.

Planning price range for testing: **$49–$99**.

This is a hypothesis, not approved permanent pricing.

---

# 15. Financial plan

## 15.1 Lean cash launch budget

Planning ranges only.

| Area | Lean | Planned |
|---|---:|---:|
| managed app/MCP hosting setup | $100 | $400 |
| database/storage/monitoring | $100 | $400 |
| legal/privacy review | $750 | $2,500 |
| payment setup | $0 | $100 |
| app listing creative | $0 | $300 |
| testing/device services | $100 | $300 |
| initial paid acquisition experiment | $500 | $1,000 |
| contingency | $200 | $500 |
| **Total planning cash** | **$1,750** | **$5,500** |

Existing GitHub repositories, current web tools, discovery architecture, brand work and HubSpot groundwork reduce launch cash needs.

## 15.2 Labor planning

| Workstream | Planning hours |
|---|---:|
| product architecture + governance | 16–24 |
| asset extraction/refactor | 24–36 |
| app/MCP/backend | 50–75 |
| UI/result system | 24–36 |
| HubSpot/commerce/analytics | 16–24 |
| QA/security/submission | 20–30 |
| **Total** | **150–225** |

Treat this primarily as founder/development opportunity cost unless outside development is hired.

## 15.3 Revenue sensitivity

Do not call these conversion forecasts.

For every 1,000 completed useful interactions:

| Paid conversion | Price | Gross revenue |
|---:|---:|---:|
| 2% | $49 | $980 |
| 5% | $79 | $3,950 |
| 8% | $99 | $7,920 |

The app's value is broader than digital-product revenue. Also measure:

- human time avoided at low-intent stages;
- qualified service leads;
- service-project revenue;
- reduced speculative collateral production;
- improved sales context;
- reusable intelligence created.

---

# 16. Measurement

## Acquisition

- app listing views where available;
- app starts/connections;
- web-to-app starts;
- paid-acquisition starts.

## Recognition quality

- route accepted;
- route corrected;
- route rejected;
- clarifying questions required;
- sessions where no existing module fits.

## Utility

- module starts;
- module completions;
- workfile generated;
- result saved;
- result marked useful/not useful;
- repeat use.

## Relationship

- save-context opt-in;
- email/account continuity;
- HubSpot relationship creation;
- return session.

## Commercial

- automated product offer rate;
- purchase conversion;
- human-help request;
- qualified opportunity;
- proposal;
- closed project;
- revenue by originating situation/module.

## Trust/quality

- user corrections;
- unsupported claim incidents;
- privacy complaints;
- data-deletion requests;
- module failures;
- escalation that should have occurred earlier;
- automated recommendation later judged inappropriate.

---

# 17. Risks and mitigations

## Platform dependency — high

Mitigation:

- own core packages, backend, CRM and artifacts;
- isolate ChatGPT-specific code;
- keep web fallback first-class;
- do not make native platform commerce a launch requirement.

## Privacy/context misuse — high

Mitigation:

- minimum necessary data;
- explicit save action;
- separate saved context from pattern intelligence;
- avoid raw transcript CRM storage;
- give user correction/deletion controls;
- do not overpromise anonymity.

## Vague "emotional intelligence" claims — high

Mitigation:

- work from expressed situation and confirmed context;
- use patterns to ask better questions;
- avoid psychological diagnosis or hidden personality labels.

## LLM inconsistency — high

Mitigation:

- use structured schemas;
- retain deterministic engines;
- test routing;
- allow rejection/correction;
- make unknown a valid result.

## Free utility without revenue — high

Mitigation:

- free insight remains complete;
- monetize implementation assets, setup, configuration and human work rather than withholding the useful answer;
- choose paid product from real beta demand.

## Product sprawl — high

Mitigation:

- one router;
- three MVP modules;
- migrate additional modules only when usage shows demand.

## Weak defensibility — medium/high

Mitigation:

- formalize Recognition Context;
- maintain tested decision engines;
- build governed pattern knowledge;
- accumulate trusted cross-domain implementation behavior;
- protect brand trust through transparent boundaries.

---

# 18. Project phases

## Phase 0 — Foundation and downstream handoff

Deliverables:

- repository governance;
- product thesis;
- launch plan;
- reuse register;
- Recognition Context v0.1 specification;
- app-safe brand/voice selection;
- privacy architecture;
- MVP definition;
- unresolved-decision list.

Gate:

The public repo contains no unselected private Project material.

## Phase 1 — Shared module extraction

Deliverables:

- extracted Customer Flow engine;
- shared tests;
- common module contract;
- Customer Flow adapter;
- AI Workday adapter;
- Audience Review adapter;
- shared structured result format.

Gate:

Equivalent structured inputs yield equivalent core results across existing web behavior and the new package.

## Phase 2 — Recognition router

Deliverables:

- initial situation taxonomy;
- routing rules;
- confirmation behavior;
- no-fit route;
- correction behavior;
- test corpus based on approved public situation patterns.

Gate:

The router can revise or reject its initial interpretation when the user corrects it.

## Phase 3 — ChatGPT application MVP

Deliverables:

- remote application/MCP server;
- ChatGPT app integration;
- three working modules;
- structured UI where useful;
- result/artifact delivery;
- failure recovery;
- privacy disclosure;
- web fallback links.

Gate:

A new user can complete each core route without Rodney.

## Phase 4 — Saved relationship

Deliverables:

- account/identity approach;
- save-context function;
- context review/edit/delete;
- HubSpot synchronization;
- explicit consent record;
- return-to-result path.

Gate:

The free useful result remains accessible without forced lead creation.

## Phase 5 — Paid automated product

Deliverables:

- one product selected from beta evidence;
- checkout;
- entitlement;
- automated fulfillment;
- CRM purchase state;
- refund/support process.

Gate:

The product can be purchased and delivered without manual fulfillment under normal conditions.

## Phase 6 — Private beta

Recruit users across:

- founder/owner situations;
- nonprofit/mission-driven organizations;
- communications/operations roles;
- practical AI adopters.

Observe actual language and behavior rather than demo scripts.

Do not run a meaningful paid ad campaign before this phase produces stable behavior.

Gate:

No unresolved critical privacy, routing or result-quality defect.

## Phase 7 — Public distribution preparation

Deliverables:

- listing name/description;
- icons/screenshots;
- example prompts;
- privacy policy;
- terms/support information;
- production endpoint;
- security review;
- submission package.

## Phase 8 — Public launch

Launch coordinated across:

- ChatGPT app/plugin distribution;
- oobSKILLS updates;
- main oobCREATIVE website;
- direct network/client outreach;
- a small paid acquisition test if platform access and economics justify it.

---

# 19. Materials to draft/redraft before launch

## New

- public app listing;
- app onboarding interaction;
- situation-router copy;
- app privacy policy;
- terms/support copy;
- saved-context explanation;
- account-continuity explanation;
- first automated product page/offer;
- human-handoff language;
- app launch announcement;
- beta invitation;
- beta feedback instrument.

## Redraft from existing

- oobSKILLS Free Tools hub;
- oobSKILLS Assessments hub;
- each migrated module landing page;
- relevant main-site service CTAs;
- HubSpot follow-up messages;
- assessment follow-up form language;
- privacy language that currently assumes browser-only assessment processing.

## Repurpose

- existing workfile/result copy;
- current assessment question logic;
- existing service-family language;
- current situation-based Start Here strategy;
- public voice rules;
- brand responsibility principles;
- evidence/claim classifications;
- oobDISCOVERY provenance and source-integrity methods.

---

# 20. Launch gates

## Product

- three MVP modules complete;
- router functional;
- no-fit route functional;
- user correction works;
- free useful result does not require sales contact.

## Technical

- tests pass;
- failure paths recover;
- secrets remain server-side;
- persistence behavior matches documentation;
- context delete/edit behavior works;
- CRM writes are correct;
- paid product delivers correctly;
- web fallback works.

## Privacy

- data map reviewed;
- raw conversation persistence minimized;
- saved context requires deliberate action;
- pattern events separated from identity;
- file lifecycle documented;
- privacy policy matches implementation.

## Creative

- public app uses selected downstream knowledge only;
- persona names are not exposed as user labels;
- claims are evidence-safe;
- emotional recognition is restrained rather than manipulative;
- app does not pretend automated output is equivalent to full consulting.

## Commercial

- one clear paid automated next step;
- one clear human-service route;
- HubSpot attribution;
- basic funnel analytics;
- fulfillment/support boundaries.

---

# 21. Explicit non-goals for launch

Do not build:

- all existing assessments;
- a proprietary CRM;
- a proprietary general-purpose LLM;
- a full emotion-detection system;
- a large subscription platform;
- an enterprise admin suite;
- a standalone mobile app;
- a new visual identity;
- a large advertising campaign;
- dozens of industry-specific pattern libraries;
- a public clinical/patient assessment system;
- a broad grant software platform.

These may be future opportunities, but they do not validate the central funnel hypothesis.

---

# 22. Phase 2 module expansion priority

Initial working order after MVP:

1. Founder Bottleneck Review
2. Workflow & Systems Review
3. Customer Contact Workflow Review
4. Website Message Clarity Review
5. Idea-to-Test Review
6. Digital Project Recovery Review
7. AI Fit Check
8. AI Tool Match
9. Human Review Checklist
10. 14-Day AI Test Plan

Observed demand may change this order.

---

# 23. Final launch hypothesis

The MVP is intended to prove this statement:

> A meaningful portion of oobCREATIVE's traditional top-of-funnel communication can become adaptive conversational collateral, allowing expensive human attention to enter later, when demonstrated intent, complexity and consequence justify it.

The long-term value is not simply a ChatGPT app.

The durable asset is the combination of situation recognition, confirmed context, governed pattern knowledge, tested decision logic, responsible communication and a real implementation business behind the conversation.
