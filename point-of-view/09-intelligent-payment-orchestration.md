# Worked example: intelligent payment orchestration

*Routing money the way a mapping app routes traffic. Illustrates [Horizons 1 and 2](../strategy/02-four-horizons.md)
and [bets 3 and 5](../strategy/03-innovation-bets.md). A hypothetical, not a description of any provider.*

## Today

A mid-market distributor runs about 4,000 supplier payments a month. Policy is crude: card if the
supplier accepts it, otherwise ACH, otherwise check. Card acceptance is negotiated supplier by
supplier. FX on the roughly 8% of spend that is cross-border is handled by the bank over email. Nobody
can say what the blended cost of moving a dollar actually is, and finance finds out about a failed or
delayed payment when the supplier calls.

## With intelligent orchestration

Every payment instruction, from the ERP, a file or an AP workflow, runs the same path —
intent → orchestration → decision → execution → reconciliation. The **decisioning call** is one stage
of it, made before anything moves. The call weighs, per transaction:

- **Cost:** interchange and rebate net on card versus ACH fee versus real-time fee versus cross-border
  spread.
- **Acceptance probability:** will this supplier take a card at this amount, based on history.
- **Speed need:** is this invoice near due, in dispute, or eligible for an early-pay discount.
- **Working-capital impact:** does paying by card extend float; is there a financing offer that beats
  the discount.
- **Risk:** fraud and identity signal on the supplier and the instruction.

It returns a rail, a funding source, a settlement time and a plain-language reason. The AP manager
sees "Paid via real-time transfer; supplier does not accept card at this amount; captured 2% early-pay
discount worth $1,240" and can override.

## What changes

| Dimension | Before | After |
|---|---|---|
| Rail decision | Static rule, set once | Per transaction, policy plus economics |
| Cross-border FX | Bank, by email | In flow, at platform rates |
| Cost visibility | Unknown | Blended cost per dollar moved, live |
| Failure handling | Supplier calls | Surfaced before send, alternative proposed |
| Early-pay discounts | Missed | Captured when they beat financing cost |

## Which archetype is well placed to run this?

A **closed-loop participant with balance-sheet access** can see both sides of the transaction, fund the
payment, price FX off its own book, and attach a financing offer at the moment of decision, so
orchestration becomes a revenue surface, not just cost routing. Its risk is the
[card-economics-versus-rail-neutrality tension](../strategy/03-innovation-bets.md): if customers
suspect the router favours the provider's margin, the layer loses credibility.

A **rail-neutral orchestrator** has the opposite profile. It is trusted to route to the customer's
best option, but it captures little of the value it creates and has no balance sheet to attach
financing.

The instructive point is that the decision surface is the same for both. What differs is how each
monetises it and where each has to work to earn trust.

## Signals it's working

Non-card rail mix rises while margin per relationship holds (financing and FX backfill the interchange
give-up); blended cost per dollar moved falls; early-pay discount capture rises; customers actively
configure policy instead of accepting defaults.

## Risks

Orchestration erodes card interchange faster than financing, treasury and data replace it (must be
shipped with Bet 4, not alone); the decisioning model is wrong about acceptance probability and
creates supplier friction; the latency budget is blown, so it cannot sit in the payment path.
