# Existing Asset Reuse Register

## Purpose

This register prevents oobAPPS from recreating work simply because the delivery surface changes.

Every source asset should be classified before implementation.

### Classifications

- **REUSE** — use essentially intact
- **EXTRACT** — move the underlying logic into a shared package
- **ADAPT** — preserve the intellectual structure but change interaction or format
- **REDRAFT** — retain the underlying idea but rewrite for a different job
- **REFERENCE** — leave in source system; use as controlled input
- **RETIRE** — superseded, duplicate or no longer useful
- **PRIVATE** — deliberately excluded from the public app/repository

This document records migration intent, not permission to expose private material.

---

# 1. oobSKILLS

## Current public assessment/tool inventory

| Asset | Classification | oobAPPS use | Notes |
|---|---|---|---|
| Customer Flow Health Review | ADAPT | MVP conversational module | Preserve current business-problem-first logic and useful complete result |
| Customer Flow decision engine | EXTRACT | Shared deterministic package | High priority; do not replace with free-form LLM scoring |
| Customer Flow input normalization | EXTRACT | Shared module contract | Preserve validation and unknown/visibility handling |
| Customer Flow result builder | ADAPT | Chat result + portable workfile | Separate structured result from presentation copy |
| Workflow & Systems Review | ADAPT | Phase 2 module | Follow-on when one workflow is already known |
| Customer Contact Workflow Review | ADAPT | Phase 2 customer-contact/phone module | Strong connection to current Twilio/ElevenLabs/HubSpot services |
| AI Fit Check | ADAPT | Fast routing submodule | Useful when user needs a narrow go/no-go decision |
| AI Tool Match | ADAPT | Post-recognition tool-category aid | Should follow a defined need, not lead with software |
| Human Review Checklist | ADAPT | Embedded checklist / workfile | Better as structured UI than pure conversation |
| 14-Day AI Test Plan | ADAPT | Automated working-output generator | Candidate component of a low-cost paid or enhanced free product |
| AI Workday Review | ADAPT | MVP conversational module | Preserve responsibility-first, human-owner and stopping-condition logic |
| Website Message Clarity Review | ADAPT | Phase 2 communications module | May accept URL/content/file context later |
| Audience Review | ADAPT | MVP conversational module | Preserve recognition/trust/message-priority intent |
| Founder Bottleneck Review | ADAPT | Phase 2 high-priority module | Strong fit for founder capacity and knowledge transfer |
| Digital Project Recovery Review | ADAPT | Phase 2 recovery module | Preserve keep/repair/replace/investigate framing |
| Idea-to-Test Review | ADAPT | Phase 2 test/launch module | Preserve bounded test and stopping condition |

## oobSKILLS shared experience assets

| Asset | Classification | oobAPPS use |
|---|---|---|
| Browser-only privacy pattern | REFERENCE | Baseline for user-agency standard, not directly portable to server app |
| Optional-share model | REUSE | Core relationship principle |
| Markdown workfile output | ADAPT | Common portable artifact format |
| Print / Save PDF result design | ADAPT | Web fallback and downloadable artifact design |
| Assessment validation patterns | EXTRACT/REFERENCE | Shared quality behavior |
| Accessibility requirements | REUSE | App/web QA standard |
| Answer → recognition → understanding → choice → practical action | REUSE | Conversation/result sequencing |
| Useful answer before lead capture | REUSE | Product rule |
| Hand-drawn worksheet / cut-line visual language | ADAPT | App UI where supported; retain web implementation |
| Current public `/free-tools/` inventory | REDRAFT | Add ChatGPT conversational entry while retaining SEO inventory |
| Current `/assessments/` hub | REDRAFT | Position as self-guided web versions of conversational reviews |
| Individual tool landing pages | REDRAFT selectively | Add conversational route without removing complete web fallback |

---

# 2. oobDISCOVERY

The clinician/Varetto questionnaire itself is not a public oobAPPS launch module. Its methods and data-governance patterns are reusable.

| Asset | Classification | oobAPPS use | Boundary |
|---|---|---|---|
| Preserve original response separately from interpretation | REUSE | Provenance architecture | Core rule |
| Source-first result review | ADAPT | Context review / "what we understood" view | Do not imply a finished diagnosis/classification |
| Evidence classes | REUSE | Pattern-library governance | Established, repeated pattern, hypothesis, project-specific, unknown |
| Business-type knowledge structure | ADAPT | Industry/context knowledge library | Keep hypotheses clearly marked |
| Plumbing seed | REFERENCE | Example of non-clinical business-type context | Do not generalize project facts |
| Clinician business-type knowledge | REFERENCE | Method/example only for public app | Clinical/privacy boundaries remain |
| Central tension question | ADAPT | General context: what must not be lost/protected | Remove clinical framing |
| Help-seeking threshold | ADAPT | Trigger: what changed enough to deal with this now | General commercial/work context |
| Function and cost | ADAPT | Current workaround: what it solves vs. costs | No psychological diagnosis |
| Ambivalence | ADAPT | Competing priorities / two truths | User-confirmed wording |
| Trust bridge | ADAPT | What must be understood before acting feels safe/credible | General decision context |
| Decision system | ADAPT | Who experiences, influences, approves and acts | Strong fit across B2B/B2C |
| Language signals | ADAPT | Recognized vs. distancing language | Avoid stylometric identity profiling |
| Healing direction | REDRAFT | Desired movement / meaningful improvement | Do not reuse therapy terminology publicly |
| Trait-bleed protection | ADAPT | Do not carry assumptions between situation patterns | Important anti-stereotyping rule |
| Production API / authenticated results architecture | REFERENCE | Proven backend/auth learning | Do not automatically combine databases |
| Invitation/password reset implementation | REFERENCE | Potential account-system precedent | Reuse selectively if architecture fits |

### Keep separate

- patient or clinical intake
- diagnosis
- patient medical records
- identifiable health information
- client-specific Varetto source data

These are outside the public oobAPPS launch scope.

---

# 3. Private oobCREATIVE Project Source System

The private Project is authoritative for broad thinking but uses **selective downstream inheritance**. oobAPPS must receive selected outcomes, not the entire private source package.

## Source-system-level treatment

| Source role | Classification | oobAPPS treatment |
|---|---|---|
| START-HERE / source precedence | REFERENCE | Preserve private-vs-downstream boundary |
| Private Project Operating System | PRIVATE | Do not copy into public repo |
| Brand Philosophy and Responsibility | ADAPT | Extract selected public brand nonnegotiables |
| Public Voice portion of Voice/Founder file | ADAPT | Extract public voice only |
| Founder collaboration preferences | PRIVATE | Do not publish as app instruction unless separately selected |
| Audience and Emotional Strategy | ADAPT | Translate buying-state intelligence into situations and app behavior |
| Services, Offers and Participation | ADAPT | Service-routing and escalation map |
| Persona Evolution and Publishing | REFERENCE/PRIVATE | Use publication method; do not publish private evolution |
| Downstream Governance and Handoffs | REUSE conceptually | Core repository/app inheritance rules |
| Proof, Claims and Knowledge Gaps | REUSE conceptually | Claims/evidence governance |
| Website & LLM Working Reference | REFERENCE | Useful web-fallback and information-architecture guidance; nonbinding |
| Private Working Concepts | PRIVATE by default | No automatic app inheritance |
| Seven persona intelligence files | ADAPT selectively | Internal pattern knowledge only through deliberate published baseline/handoff; persona names not user-facing |
| Logo reference sheet | REFERENCE | Use approved existing marks; do not invent brand system |
| Manifest | REFERENCE | Source inventory and privacy model |

## Selected public principles already suitable for oobAPPS

- Go Deeper, Not Louder.
- Creative thinking should help people see, understand, decide, connect or act more effectively.
- Technology should support human judgment rather than erase it.
- AI should be tied to a real responsibility and remain human-reviewed where consequence requires it.
- Clients should leave with greater capability rather than unnecessary dependency.
- Complex work should be clarified without flattening nuance.
- Communication should preserve dignity, context, consent and agency.
- Do not manufacture urgency, exploit emotion or make claims that outrun evidence.
- Start from recognizable situations rather than forcing users to diagnose a service.

---

# 4. Persona and situation materials

## Existing personas

**Treatment: ADAPT + PRIVATE/PUBLISHED separation**

Persona names remain useful internal strategic shorthand but should not become public user classifications.

For oobAPPS, deliberately selected persona intelligence should be translated into public-safe situation records containing fields such as:

- recognizable situation
- protected value
- likely structural friction
- common trigger
- desired movement
- useful confirmation questions
- likely objections
- relevant service families
- what must not be assumed

Do not commit private-evolution notes into this public repository.

## Existing emotional entry pathways

Current selected pathways include situations equivalent to:

- work still depends too heavily on one person
- valuable work is difficult to explain
- communication has become structurally chaotic
- customers do not understand the value of expertise
- an organization needs a practical, responsible way to use AI
- a digital/communications project has stalled or failed
- an idea is ready for an honest test

**Treatment: REUSE + ADAPT**

These are strong router seeds, not seven mandatory public products.

---

# 5. Services and commercial pathways

## Current service families

| Service family | Classification | oobAPPS role |
|---|---|---|
| Message, Positioning and Identity | REUSE | Escalation destination |
| Website Strategy and Visual Refresh | REUSE | Escalation destination |
| Communication Systems and Practical AI | REUSE | Primary initial destination for operational/AI modules |
| Campaigns, Launches and Storytelling | REUSE | Escalation destination |
| Ongoing Communications Support | REUSE | Recurring human-support destination |

Do not turn each situation/persona into a separate public service unless market evidence justifies it.

## Participation models

Two language sets currently exist in source strategy:

- Guided / Co-Created / Full Implementation
- DIY Assist / Co-Create / Custom Services

**Classification: REFERENCE — unresolved globally**

Do not select one set for the app without a task-specific decision.

---

# 6. Proof and claims

## Evidence framework

**Classification: REUSE**

The app should distinguish:

- brand belief
- capability claim
- experience claim
- observable outcome
- measurable result
- testimonial

A complete verified proof register does not yet exist in the private source package.

Therefore:

- do not manufacture case-study proof
- do not infer metrics
- do not imply completed work merely because a capability is planned or described
- use restrained capability language until evidence is deliberately added

---

# 7. Current integrations and adjacent systems

| Asset/system | Classification | oobAPPS role |
|---|---|---|
| HubSpot setup | ADAPT | Relationship system of record after deliberate opt-in |
| Existing assessment-follow-up concept | ADAPT | Preserve context on lead rather than generic contact submission |
| Twilio + ElevenLabs phone system | REFERENCE | Future conversational surface and proof-of-concept; not MVP dependency |
| Phone-context/middleware concept | REFERENCE | Parallel architecture: source system remains source of truth; agent receives needed context |
| Stripe | REUSE/ADAPT | Launch commerce path for automated paid product |
| Existing oobCREATIVE website | REFERENCE/REDRAFT selectively | Authority, search, service validation and human-service destinations |

---

# 8. New assets that do not currently exist

These should be created rather than disguised as reuse:

- Recognition Context schema
- conversation router
- situation taxonomy beyond current seven entry pathways
- pattern-event schema
- public app knowledge package
- app-specific privacy policy
- app listing metadata and examples
- ChatGPT UI components
- MCP server and tool contract
- account/context review experience
- standardized cross-surface module contract
- shared result/artifact renderer
- app analytics plan
- first automated paid product chosen from beta evidence

---

# 9. Migration order

1. Lock public/private governance.
2. Extract Customer Flow decision logic into a cross-surface package.
3. Normalize Customer Flow module contract.
4. Normalize AI Workday module contract.
5. Normalize Audience Review module contract.
6. Build Recognition Context v0.1.
7. Build situation router using only selected public-safe pattern intelligence.
8. Build ChatGPT surface against shared packages.
9. Add optional saved context and HubSpot relationship trigger.
10. Choose paid product from observed beta demand.
11. Migrate remaining oobSKILLS modules only as usage justifies them.

This register should be updated whenever a source asset is migrated, superseded or intentionally left behind.
