# Experience blueprint

*The experience the category is converging toward, at industry level. A point of view on what "good"
looks like, not a spec for anyone.*

## The principle

> **The best payment experience will not expose more financial complexity. It will absorb more of it.**

Every step up in backend intelligence, more rails, more decisioning, more automation, more agents, is
an opportunity to *remove* a decision from the customer, not add one. State it as a hard product
principle:

> **Increasing system intelligence should reduce customer cognitive load, not increase it.**

The instruction stays simple:

```
Customer:   "Pay this invoice."

Underneath: supplier preference, rail selection, funding source, FX,
            fraud, identity, approval policy, liquidity check,
            settlement, reconciliation
```

None of that chain should surface unless the customer asks, or unless a genuine judgment call needs a
human. The system's job is to make the decision well and be able to explain it, not to route the
decision back to the user.

## Who it serves

| Persona | The job today | What "absorbed complexity" looks like |
|---|---|---|
| **AP manager or analyst** | Chases approvals, matches invoices, fixes exceptions | Invoices pay themselves on the right rail; only real exceptions surface |
| **Controller or CFO** | Rebuilds cash position from bank portals and spreadsheets | One live view of cash, payables and options; a forecast worth trusting |
| **Treasury** | Manual sweeps, FX by phone, liquidity guesswork | Rules that run themselves; FX and liquidity actions in context |
| **Supplier AR team** | Logs into buyer portals; reconciles opaque payments by hand | Predictable funds; machine-readable remittance; self-serve preferences |
| **Platform or partner PM** | Integrates a payments API; owns the end customer | Drop-in UI and API that matches their brand and adds no support load |
| **Developer** | Wires issuing, auth, webhooks | One SDK, one sandbox, one set of primitives across products |
| **AI agent** | (new) executes AP, AR and treasury tasks | Scoped mandate, machine-readable policy, explainable decisions, reversible actions |

The two under-served personas are the **supplier AR team**, a recipient in most models rather than a
user, and, increasingly, the **agent**, which needs a first-class interface of its own: not a UI, but
a contract of identity, authority, policy and audit.

## Experience commitments

1. **Real-time or it does not count.** Balances, status, reconciliation and decisions update live.
2. **Two-sided by construction.** Every buyer flow has a defined supplier counterpart. A payment is
   done when it is received, reconciled and explained, not when it is sent.
3. **Configuration, not customisation.** Programs, controls, approval rules and rail policy are set
   through UI and API. No professional-services engagement to change a limit.
4. **One journey, many surfaces.** Embedded, direct, partner console and agent interface are
   renderings of the same flows and data, not products that drift apart.
5. **Explainable by default.** Every automated decision carries a plain-language "why," logged and
   reversible.
6. **Progressive autonomy.** The customer chooses how much the system does unattended, from "suggest"
   to "do it and tell me," per workflow, and can dial it back.

## Depth without overwhelm

Sophisticated treasury users need levers: rail overrides, funding rules, settlement timing, exposure
limits. Everyone else needs those same decisions made well and kept out of sight. The resolution is
not two products. It is one core with **progressive disclosure**: defaults that are genuinely good, a
"why did it do that" view one click away, and controls that appear only for the users and workflows
that use them.

## Design system as buildable artifacts

The experience is expressed as **tokens, schemas and prompts**, not just screens:

- **Tokens:** visual and semantic (`status.pending`, `rail.realtime`) so any surface, including
  partner-branded ones, renders consistently.
- **Schemas:** canonical shapes for payment, invoice, remittance, decision, mandate and dispute,
  shared by UI, API and analytics so concepts mean the same thing everywhere.
- **Prompts:** reviewed templates and guardrails for AI-assisted surfaces (natural-language
  configuration, exception explanation, agent instructions) so generated behaviour stays on-rails and
  auditable.

## What "good" looks like

- Time to change a payment program: minutes, self-serve.
- Straight-through processing for standard invoices: a large majority, no human touch.
- Reconciliation exceptions: trending toward zero.
- Supplier onboarding: same session, self-serve.
- One design system, one component library, one SDK across every surface, including the agent's.
