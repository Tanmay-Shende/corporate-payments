# The four horizons

*How corporate money movement matures from an instrument business into an orchestration layer. The
horizons are **sequential in dependency**, each resting on the one before, but not sequential in time.
The industry is working on all four simultaneously, and different participants enter at different
points.*

---

## Horizon 0. Unify the foundation

**The problem.** A participant that has launched many products or absorbed acquisitions typically
runs several authorization and processing stacks side by side. Each re-implements the same primitives,
onboarding, configuration, spend controls, funding, settlement, reconciliation, disputes, risk,
slightly differently. The cost compounds: slow delivery, inconsistent experience, duplicated risk and
compliance surface, an operating base that grows with the catalogue.

**The target.** One modern core, three shared layers, all configuration-driven and real-time:

- **Pre-transaction:** client and supplier onboarding and KYB, program configuration, controls and
  policy, credit setup, entitlements.
- **Transaction processing:** multi-rail issuing and authorization, multi-currency funding, real-time
  balances, billing and incentive calculation.
- **Post-transaction:** settlement, reconciliation and remittance, disputes, fraud and risk
  decisioning, reporting and data export.

**Why it comes first.** Horizons 1 through 3 are only affordable if they compose these services
rather than rebuild them. This horizon rarely appears in a market narrative, but it sets the marginal
cost of every subsequent move. It also favours an incremental approach, routing new volume to the new
core and migrating the back book on a schedule, over a single large rewrite.

**Signals it's working.** Time-to-launch for a new payment product (down); distinct authorization
paths (down); unit processing cost (down); share of volume on the unified core (up); reconciliation
exceptions per thousand transactions (down).

---

## Horizon 1. Orchestrate money movement

**Beyond instrument issuing.** The layer chooses and executes across rails, card where it earns its
keep, real-time and ACH where they do not, cross-border where that is the need, by policy and
economics rather than by whichever rail the provider prefers to sell.

**AP/AR with two-sided value.** Suppliers receive real value, faster funds, straight-through
reconciliation with remittance data, fewer disputes, optional financing, not just an instrument they
must accept. Supplier enablement becomes a persistent, reusable network that every new buyer inherits,
rather than a cost rebuilt per relationship.

**The treasury and liquidity layer.** Balances and operating accounts, automated sweeps, liquidity
views, cash-flow forecasting and FX, capabilities most payment providers lack. Whether this requires
an owned charter or a banking-as-a-service relationship is a live strategic question, not a settled
one.

**Signals it's working.** Non-card rail mix; supplier-initiated enablement rate; share of revenue
from AP, treasury and orchestration versus legacy instrument issuing; balances held; buyer *and*
supplier satisfaction.

---

## Horizon 2. Make every transaction intelligent

Every transaction passes through a real-time decision before it settles:

- **Rail:** expected cost versus acceptance probability versus speed versus working-capital impact.
- **Funding source:** which account or credit line, given balances and policy.
- **Fraud and identity:** one decision, not a separate hop.
- **Financing:** a dynamic offer (pay early, extend terms, finance this invoice) priced from live
  data.
- **Settlement timing:** hold, accelerate or schedule based on liquidity and risk.

The same layer turns first-party payment data into embedded working capital, underwriting from
observed revenue, volume, seasonality, buyer concentration, refunds and receivables, signal an
external lender cannot see. This is where "payment, then decision, then action" becomes literal, and
where a data platform built for internal analytics is pointed at the transaction path.

**Signals it's working.** Authorization rate at constant fraud loss; blended cost per dollar moved;
attach rate of financing to payment flows; loss rates on data-underwritten credit; incremental margin
per transaction.

---

## Horizon 3. Make financial workflows agentic

AP, AR and treasury workflows are executed end-to-end by software inside the customer's system of
record: invoice intake, matching, approval routing, payment scheduling, exception handling, cash
positioning. The payments participant's role shifts from moving money on instruction to standing
behind money moved by software:

- **Verified agent identity**, aligned to emerging cross-industry standards.
- **Scoped authority**, cryptographically bounded mandates: which counterparties, what amounts, what
  conditions.
- **Policy enforcement at the rails**, limits enforced in infrastructure, not only in a prompt.
- **Auditable, reversible decisions**, every action explained, logged, and unwindable.
- **Settlement certainty**, a defined party stands behind the movement.

The strategic point is not "AI will make payments." It is that **when software moves money
autonomously, trust becomes part of the payment product.** Identity, authority, liability,
explainability and dispute resolution are now product surfaces, not compliance footnotes.

**Signals it's working.** Share of volume initiated by software; straight-through rate for
agent-initiated flows; human-intervention rate on exceptions; disputed or reversed agent
transactions; customers widening mandates over time.

---

## The through-line

Each horizon compounds the previous one. Horizon 0 makes 1 affordable. Horizon 1 gives 2 more surfaces
to be intelligent about. Horizon 2 makes 3 safe by turning software decisions into governed, priced,
auditable events. Skipping 0 makes everything above it expensive; skipping 2 makes 3 reckless. The
strategy is the sequence, not any single layer, and it does not depend on one participant owning all
four.
