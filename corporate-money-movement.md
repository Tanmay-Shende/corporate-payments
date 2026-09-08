# Who Owns Corporate Money Movement?
### An outside-in point of view on the evolution of corporate money movement

*This is an outside-in hypothesis about where corporate payments and financial infrastructure are
heading. It is deliberately company-agnostic, and meant as a starting point for discussion rather than
a recommendation or a roadmap.*

---

## The thesis, in one line

**Corporate payments is shifting from issuing an instrument to orchestrating the customer's money
movement, and the open question is who ends up owning that orchestration layer.**

For two decades the winning move was to place an instrument, increasingly a virtual card, inside a
workflow and earn economics on the volume. That still works, but it is now one option among many. The
unit of value is climbing the stack: from the instrument, to the choice of rail, to the orchestration
of an entire financial workflow across rails, AP/AR, treasury, liquidity, financing, fraud, identity
and reconciliation, with software increasingly making the routing calls and, before long, executing
the workflow itself. Whoever operates that layer holds the corporate relationship. Everyone else
supplies it.

Put as a contrast: today is disconnected workflows, manual routing decisions and fragmented
infrastructure; the direction is one intent, an intelligent decision, optimised execution and
continuous reconciliation. The move is not automating any single finance process — it is coordinating
the decisions that determine how corporate money moves.

## Why now

Four structural forces, not a market-size argument.

1. **Money movement is becoming multi-rail by default.** Real-time rails now carry structured
   remittance data through ISO 20022, and enterprise adoption intent is broad. Rail *selection*,
   rather than rail *access*, becomes the product surface.
2. **The workflow is consolidating around software.** Finance teams want to pay, get paid, forecast
   and reconcile without leaving their system of record. Whoever sits there shapes the payment
   decision.
3. **Decisioning is moving into the transaction.** Value shifts from the transaction record to the
   decision that produced it: which rail, which funding source, what risk posture, whether to finance,
   when to settle.
4. **Software is starting to act, not just advise.** Agentic tooling in finance operations is moving
   from experimentation toward infrastructure. Invoice handling and payment scheduling are
   increasingly executed rather than surfaced.

None of these is complete. Together they move the center of gravity from the instrument to the
orchestration of the flow.

## The strategic question

**Who will own the intelligent orchestration layer for corporate money movement?** Several archetypes
have a claim, each advantaged and constrained differently.

**Closed-loop financial platforms**, with control of both acceptance and issuance and often with
balance-sheet access, have the richest data, the tightest loop from risk to financing to settlement,
integrated funding, two-sided network effects, and control of the experience. They also tend to carry
legacy and post-acquisition fragmentation, proprietary-rail incentives that can conflict with
customer-optimal routing, interoperability limits, and regulatory weight. The advantages and the
constraints come from the same property: control.

The other claimants are mirror images. **Payment networks** have reach and identity standards but sit
thin in the workflow. **Banks** have the balance sheet and the regulatory perimeter but slower product
cycles. **ERP and software platforms** own the workflow but lack rails and risk infrastructure.
**Fintech infrastructure and orchestrators** are rail-neutral and fast but hold neither the customer
relationship nor the balance sheet.

The question underneath all of this is whether orchestration is won by *owning* the loop or by being
the most *trusted and interoperable* layer across loops that stay separate. The answer is open.

## Four horizons

Sequential in dependency, not in time. The industry is working on all four at once.

**Horizon 1. Unify the foundation.** Fragmented payment infrastructure becomes reusable primitives:
onboarding, configuration, multi-rail processing, settlement, reconciliation, risk. The least visible
horizon, and the one that sets the marginal cost of everything above it.

**Horizon 2. Orchestrate money movement.** Past instrument issuing into multi-rail payments, AP/AR
with genuine two-sided value, supplier enablement as a reusable network, and the treasury and
liquidity layer most providers still lack.

**Horizon 3. Make every transaction intelligent.** A real-time decision per transaction on rail,
funding source, fraud and identity, FX, financing offer and settlement timing. The same data
underwrites embedded working capital from observed cash flow rather than a credit file.

**Horizon 4. Make financial workflows agentic.** Software executes AP, AR and treasury workflows
end-to-end, with scoped authority, policy enforcement, auditability and settlement guarantees. The
provider's role shifts from moving money on instruction to standing behind money moved by software.

## One path, many surfaces

Whatever starts a payment — a person in an app, an application through an API, an AI agent under a
mandate — the money runs the same five stages: **intent → orchestration → decision → execution →
reconciliation**. Intent is declarative and names no rail or date; orchestration coordinates the
workflow; the decision chooses rail, funding source and timing and can explain itself; execution
carries it out on one rail; reconciliation ties the result to the bank record, and only then is the
payment complete. Stating the path once is what lets payables, receivables, cards, treasury and
working capital run on one core instead of several, and what makes an agent a first-class caller
rather than a bolt-on.

Read as strategy, that core carries three pillars: **intelligent money movement** — optimise rail ×
funding × timing as one governed, explainable decision; **network** — suppliers, customers, banks and
financial infrastructure connected through reusable verified identity, so value compounds as buyers ×
suppliers rather than buyers + suppliers; and **autonomous finance** — software running whole finance
workflows within explicit mandates, policies and limits, every action logged and reversible.

## The experience this converges toward

**The best payment experience will not expose more financial complexity. It will absorb more of it.**

The instruction stays simple, *"pay this invoice,"* while supplier preference, rail selection, funding
source, FX, fraud and identity checks, approval policy, liquidity, settlement and reconciliation
resolve underneath it. As a product principle: **increasing system intelligence should reduce customer
cognitive load, not increase it.**

This holds across every surface: embedded APIs and SDKs, ERP workflows, direct applications, partner
platforms, the CFO and treasury view, the supplier's view, and an AI agent's interface. Sophisticated
treasury users need depth and control; everyone else needs the decision made well and explained on
request. One core serves both, through progressive disclosure rather than two products.

## What this looks like in practice

Five scenarios, each carrying a different part of the thesis. All are hypotheticals, developed in full
under [examples](examples/) and worked through together as a navigable reference prototype that renders
the whole argument — the one core, the intent → orchestration → decision → execution → reconciliation
path, the three pillars, and every scenario below — as a single clickable system.

**Paying 4,000 suppliers a month without knowing what it costs.** A mid-market distributor routes on a
static rule: card if the supplier accepts it, otherwise ACH, otherwise check. Instead, every
instruction hits a real-time decision weighing cost, acceptance probability, speed and working-capital
impact, which returns a rail, a funding source and a reason the AP manager can override. Blended cost
per dollar moved becomes visible for the first time.
[Intelligent payment orchestration](examples/09-intelligent-payment-orchestration.md)

**An AP team that works the exceptions instead of the queue.** A services firm turns on an AP agent
under a scoped mandate: approved counterparties, a per-invoice threshold, three-way match required, no
new bank details without out-of-band verification. It processes 220 invoices, escalates the genuine
judgment calls, and blocks one payment because a supplier's bank details changed that week.
[Software-run AP/AR](examples/10-agentic-ap-ar.md)

**A controller who never leaves the ERP to manage cash.** Treasury run across four bank portals and a
spreadsheet becomes one live cash position, sweeps that run themselves, a forecast with a confidence
band, and liquidity options offered at the branch points rather than discovered late.
[Embedded treasury](examples/11-embedded-treasury.md)

**A supplier that enrols once instead of once per buyer.** The party who is a recipient in every other
model becomes a user: one durable network profile, remittance data attached to the money, its stated
payment preference read by the router, and early pay priced off history the network already observed.
[The supplier side as a network](examples/12-supplier-enablement.md)

**A seasonal business financed on what it actually does.** A distributor needing inventory for a peak
it can forecast is underwritten on observed cash flow refreshed daily, in session, instead of on filed
accounts fourteen months stale. It is also where the consent question gets real.
[Working capital underwritten on payment data](examples/13-embedded-working-capital.md)

Read together, these name the users the shift actually serves: the AP manager, the controller and CFO,
the treasury team, the supplier's AR team, the platform partner, the developer, and now the agent. Two
are under-served today. The supplier's AR team is a recipient in most models rather than a user, and
the software agent needs not a screen but a contract of identity, authority, policy and audit. The
[experience blueprint](experience/05-experience-blueprint.md) develops all seven.

## What it takes to win

Eight capabilities matter. No participant needs to own all of them. The judgment is which to **own**,
which to **partner** for, and which to make **interoperable**.

| Capability | Typical posture |
|---|---|
| Unified financial infrastructure | Own |
| Multi-rail orchestration | Own |
| Two-sided network economics | Own, build over time |
| Real-time risk and decisioning | Own |
| Balance-sheet and liquidity | Own or partner, charter-dependent |
| AI-native product and engineering | Own |
| Trust, identity and delegated authority | Interoperate, shared standards |
| Interoperability and distribution | Partner or interoperate |

The pattern: the differentiated core is infrastructure, decisioning and the two-sided relationship.
Identity, standards and reach are worth more shared than hoarded.

## The counter-thesis

Corporate payments may never converge on a single financial operating system. Banks, networks, fintech
infrastructure, ERP platforms, orchestrators and AI platforms may each hold a different layer of the
workflow more or less permanently, because each has a structural advantage the others cannot easily
take.

If that is the outcome, the winning position is not owning the entire closed loop. It is becoming the
most trusted and interoperable orchestration layer across loops that never merge, the layer everyone
routes through precisely because it is not trying to capture the whole flow. A serious strategy should
survive either world.

## Strategic tensions

- **Closed versus open.** Does owning the loop create advantage, or constrain interoperability?
- **Card economics versus rail neutrality.** Optimize the customer's cost, or the provider's
  highest-margin rail? The answer sets the layer's credibility.
- **Automation versus control.** How autonomous can financial agents become before customers demand a
  human in the loop?
- **Data advantage versus trust.** How much transaction data can fund underwriting before customers
  pull back?
- **Build versus partner.** Which capabilities are differentiating, and which are commodities?
- **Simplicity versus complexity.** How do you give treasury users depth without overwhelming everyone
  else?

## Open questions

1. Does orchestration accrue to whoever owns the rails and balance sheet, or to whoever owns the
   workflow the customer already lives in?
2. As real-time rails scale, what happens to the economics that fund today's rebates and float, and
   how fast?
3. When software moves money autonomously, where does liability sit, and who is structurally best
   placed to price that risk? *When software starts moving money autonomously, trust becomes part of
   the payment product.*
4. Will the supplier side pay for two-sided value at scale, or does it stay a cost of doing
   buyer-side business?
5. How much of a credible treasury offer genuinely requires a charter versus a banking-as-a-service
   relationship?
6. What consent and data-rights model lets payment data power underwriting without eroding the trust
   that produced the data?

---

*Supporting material develops each thread: [the forces](strategy/01-market-thesis.md), the
[horizon model](strategy/02-four-horizons.md), [where to place bets](strategy/03-innovation-bets.md),
an [experience blueprint](experience/05-experience-blueprint.md), a [platform blueprint](platform/06-platform-blueprint.md),
an [AI-native operating model](operating-model/07-ai-native-operating-model.md), a [commercial model](commercial/08-commercial-model.md),
and five worked [examples](examples/). A [deck outline](deck-outline.md) covers the same ground for a
live discussion.*
