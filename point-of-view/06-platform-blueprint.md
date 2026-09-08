# Platform blueprint

*Why a unified core is the precondition for [Horizon 0](../strategy/02-four-horizons.md),
described as an industry pattern. Product-strategy altitude, not an engineering design.*

## The problem, precisely

Commercial-payments participants tend to accumulate multiple authorization and processing stacks, one
per major product line or acquisition. Each re-implements the same primitives. The costs are
structural:

- **Slow delivery.** A new product touches N stacks, N risk reviews, N reconciliation models.
- **Inconsistent experience.** Controls, statuses and data differ by product, so "one experience"
  (see [experience blueprint](../experience/05-experience-blueprint.md)) is impossible to deliver.
- **Duplicated risk surface.** Fraud, compliance and settlement logic maintained in parallel.
- **Cost base scales with the catalogue.** Every product carries its own operational tail.

This is the single biggest reason an incumbent moves slower than a challenger, and it is invisible
from the outside.

## Target: one core, three layers

```
                        +---------------------------------------------+
   Products / surfaces   |  Embedded SDK | Direct app | Partner UI | Agent API |
   (compose the core)    +---------------------------------------------+
                                          |
   +--------------------------------------+--------------------------------------+
   |  PRE-TRANSACTION        TRANSACTION PROCESSING        POST-TRANSACTION       |
   |  - Onboarding / KYB     - Multi-rail issuing & auth   - Settlement           |
   |  - Program config       - Multi-currency funding      - Reconciliation /     |
   |  - Spend controls /     - Real-time balances            remittance           |
   |    policy               - Billing & incentive calc   - Disputes             |
   |  - Credit setup                                       - Fraud & risk         |
   |  - Entitlements                                         decisioning          |
   |                                                      - Reporting / data export|
   +---------------------------------------------------------------------------------+
                                          |
   +--------------------------------------+--------------------------------------+
   |  Shared foundations: identity, data platform, real-time decisioning layer   |
   |  (Horizon 2), ledger, event bus, observability, funding & settlement rails  |
   +---------------------------------------------------------------------------------+
```

**Design commitments**

- **Configuration-driven.** New programs, controls, rail policies and pricing are data, not code.
- **Real-time.** Balances, status, decisions and reconciliation are live, not batch.
- **Multi-rail native.** Card, ACH, real-time, cross-border and check-outsource are peers behind one
  interface, selected by policy and the decisioning layer.
- **API-first, one SDK.** The same primitives serve embedded, direct, partner and agent surfaces.
- **Canonical schemas.** One shape each for payment, invoice, remittance, decision, mandate, dispute,
  shared by processing, UI and analytics.
- **Decisioning as a shared service.** The Horizon 2 real-time layer is part of the foundation, called
  by every product, not rebuilt per product.

## One path through the core

Every business event — a bill approved, an invoice raised, a payroll run, an agent instruction — runs
the same five stages, whatever the product surface that started it:

```
Intent  ->  Orchestration  ->  Decision  ->  Execution  ->  Reconciliation
```

- **Intent** — declarative; what must happen, by when, under what constraints. Names no rail, account
  or date.
- **Orchestration** — assembles context, prices the options, drives the flow. One per intent.
- **Decision** — the Horizon 2 call: rail, funding source, timing, risk. Explainable and reversible.
- **Execution** — carries it out on one rail; the rail's own settlement confirmation is the last step
  inside execution at this altitude.
- **Reconciliation** — ties the result to the bank statement. Only then is the payment complete.

Stating the path once is what lets payables, receivables, cards, treasury and working capital run on
the same core instead of five parallel ones.

## Migration: strangle, do not rewrite

A single large replacement of production payment infrastructure is the wrong risk profile. The pattern
that works:

1. **Stand up the new core** with the pre-transaction, transaction and post-transaction services for
   one rail and one product.
2. **Route all new volume** for that product to the new core from day one; freeze feature work on the
   legacy stack.
3. **Add products and rails incrementally**, each composing the shared services instead of extending
   a legacy stack.
4. **Migrate the back book** on a published schedule, product by product, with parallel-run and
   reconciliation gates.
5. **Decommission** each legacy stack as its last product leaves.

Every step is reversible, platform investment is tied to visible product delivery, and there is no
multi-year program with no output until the end. Shipping one lighthouse Horizon 1 product on the new
core early is a good way to prove the model before the full investment (see
[open questions #8](../strategy/04-open-questions.md)).

## Risks and how the pattern manages them

| Risk | Mitigation |
|---|---|
| Platform program under-funded, stalls half-built | Tie each increment to a shipped product; no "platform-only" phases |
| Legacy stacks kept alive indefinitely | Published decommission schedule with owners; feature freeze on day one |
| New core becomes its own silo | Canonical schemas and one SDK enforced from the first product |
| Reconciliation breaks during migration | Parallel-run and exception-rate gates before each cutover |
| Decisioning bolted on later | Real-time decisioning layer is in the foundation from the start |

## Metrics that show it's working

- Distinct authorization paths in production (down).
- Share of total volume on the unified core (up, a clear majority within the program window).
- New-payment-product time-to-launch (down).
- Unit processing cost per transaction (down).
- Reconciliation exceptions per thousand transactions (down).
- Products consuming the shared decisioning service (up).
