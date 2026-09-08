# AI-native operating model

*How a corporate payments product organisation builds in an AI-native, regulated environment. A point
of view on ways of working, not an org chart.*

## Two uses of AI, kept distinct

1. **AI in the product:** real-time decisioning, exception explanation, natural-language
   configuration, cash-flow forecasting, and (Horizon 3) agents that operate finance workflows.
2. **AI in how the product is built:** discovery, prototyping, spec-to-code, design-to-engineering,
   test generation, documentation.

Both matter; conflating them produces demos instead of products. This doc is mostly about the second,
because that is the part a product operating model controls directly.

## Building AI-native

- **Spec-driven development.** The durable artifact is a precise, reviewed specification: schemas,
  acceptance criteria, decision tables, edge cases. Code, whether human- or AI-generated, is
  downstream of a spec that a person owns.
- **Prompt-to-code prototyping.** Product and design produce working prototypes directly from specs
  to validate journeys with customers in days, not sprints, then throw them away or promote them
  through the real quality gates.
- **Design-to-engineering as artifacts.** Design outputs are tokens, schemas and component contracts
  (see [experience blueprint](../experience/05-experience-blueprint.md)), so what design hands over
  composes with the platform instead of needing re-interpretation.
- **AI in the SDLC.** Test generation, migration scaffolding, reconciliation-rule drafting and doc
  generation are assisted by default, with human review as the gate, not the exception.
- **Evaluation over vibes.** Any AI feature ships with an eval set and a monitored quality metric.
  "It seemed good in the demo" is not a launch criterion.

## Doing it inside a regulated, bank-adjacent business

This is the constraint that separates a payments AI operating model from a generic one. Governance is
a **product requirement**, not compliance overhead bolted on at the end:

- **Model risk management.** Every model in a decision path (fraud, credit, rail selection, agent
  authorisation) has an owner, documentation, validation and monitoring, consistent with how a bank
  governs models.
- **Explainability and audit.** Every automated decision emits a plain-language reason and an
  immutable log. Regulators, customers and disputes teams can all reconstruct "why."
- **Two compliance surfaces, kept distinct.** Entity-level attestation — KYB status, sanctions-screening
  cadence, disclosures, regulatory-reporting status — is a governance record that rolls up to the legal
  entity. Per-payment screening — sanctions, duplicate, anomaly and changed-bank-detail holds — is an
  operational surface in the payment path. They share data but answer different questions; conflating
  them hides which one is failing.
- **Human-in-the-loop by design.** Progressive autonomy: the customer and the operator choose where
  the system suggests, acts and notifies, or acts silently, and can dial back per workflow.
- **Data governance.** Purpose limitation, consent tracking and lineage for any data used to train or
  prompt models, especially first-party payment data used for underwriting.
- **Change control.** Prompt and model changes go through versioning, review and rollback like any
  other production change.

## Team and talent shape

- **Product managers as owners, fluent in AI workflows.** PMs write specs, run evals and prototype,
  not just backlogs. The skill bar shifts toward systems thinking and decision design.
- **Design embedded and systematised.** Designers own the token, schema and component system and the
  AI-surface prompt guardrails, not just screens.
- **A shared platform team** owns the unified core and the decisioning layer so product teams compose
  rather than rebuild.
- **Risk and compliance partners embedded** in product teams from discovery, so governance is designed
  in.
- **Distributed by default.** Payments product talent is spread across regional centres and time
  zones; that only works if it runs off shared specs and systems rather than shared meetings.
- **Psychological safety as an operating requirement.** Teams have to be able to flag a risky model, a
  bad rail decision or an unsafe agent behaviour without friction. In a regulated payments business the
  cost of silence is measured in losses and consent orders.

## What this changes about delivery

| Before | AI-native |
|---|---|
| Requirements doc, design, build, test | Spec (owned, reviewed), prototype, build assisted, eval-gated |
| Design hands over screens | Design hands over tokens, schemas, component contracts |
| AI feature is a model call | AI feature is model plus eval set plus monitored metric plus governance owner |
| Governance reviewed at the end | Governance designed in from discovery |
| Velocity from more people | Velocity from better specs and reusable platform services |

## Signals it's working

- Cycle time from validated spec to production (down).
- Share of features shipped with an eval set and a monitored quality metric (up, toward 100% for AI
  features).
- Prototype-to-customer-feedback time (days).
- Reused platform services per new product (up); duplicated primitives (down).
- Zero "unexplained" automated decisions in audit sampling.
