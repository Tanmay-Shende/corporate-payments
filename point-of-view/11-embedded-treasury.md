# Worked example: embedded treasury, the CFO never leaves the ERP

*Illustrates [Horizon 1](../strategy/02-four-horizons.md) (the treasury leg) and the
[commercial stack](../commercial/08-commercial-model.md). A hypothetical, and the place where the
[closed-versus-open and charter-versus-BaaS questions](../strategy/04-open-questions.md) get concrete.*

## Today

A company with $120M in revenue runs treasury across four bank portals and a spreadsheet. Cash
position is a day stale. Sweeps between operating and reserve accounts are manual and often skipped.
Payroll cover is checked by eyeballing balances every second Thursday. FX for European supplier
payments is booked by phone. Idle cash earns nothing because moving it is a chore.

## With embedded treasury

Inside the same software where the company already manages payables, the controller sees:

- **One live cash position** across all external bank accounts and the platform-held operating account.
- **Automated sweeps**, rules like "keep $250k in operating, sweep the rest to the yield account,
  unsweep to cover scheduled payroll and AP two days out."
- **A forecast** built from scheduled payables, historical receivables patterns and payroll, with a
  confidence band, not a single line.
- **In-app FX**, the €600k of supplier payments next week priced and booked in two clicks, no email.
- **Liquidity actions**, for example "you will be $300k short on the 28th; options: delay these three
  non-critical payments, draw $300k on the credit line at X, or accelerate this receivable via
  financing."

The controller sets the rules once; the system runs them and asks for a decision only at the branch
points.

## What makes it possible

- **Horizon 0 core.** Treasury is balances, ledger and movement on the *same* unified platform as
  payments, not a bolted-on product with its own integration.
- **Balance-sheet access.** Operating accounts, the yield on swept balances and settlement need
  either an owned charter or a deep banking-as-a-service relationship. Which of those is sufficient is
  a genuine strategic question ([open questions #5](../strategy/04-open-questions.md)); the experience
  above can be built on either, with different economics and control.
- **Decisioning layer.** The forecast and the liquidity options are the same real-time engine that
  routes payments, pointed at cash.

## Why it matters strategically

Treasury deepens the relationship in three ways at once: it raises switching cost (the customer's cash
operations now live here), it grows the **deposit base** that funds the rest of the platform, and it
creates a natural home for **working-capital products** (the credit line, the receivable acceleration)
underwritten on data already in hand. It moves a participant from payments vendor toward the
customer's finance platform, which is precisely the position every archetype in
[the strategic question](../strategy/01-market-thesis.md) is competing for.

## Signals it's working

Balances and deposits held (up); share of payments customers attaching treasury (up); forecast
accuracy versus actuals (improving); working-capital products attached to treasury accounts (up);
customer-reported time spent on cash management (down).

## Risks

Built as a separate product, it becomes a distraction from money movement (see
[open questions #8](../strategy/04-open-questions.md)); regulatory and capital implications of holding
more operating balances; competing with customers' existing banks can strain those relationships;
forecast quality has to be genuinely good or trust evaporates fast.
