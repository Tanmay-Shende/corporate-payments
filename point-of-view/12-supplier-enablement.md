# Worked example: the supplier side as a network

*Illustrates [Horizon 1](../strategy/02-four-horizons.md) (supplier enablement) and
[bet 2](../strategy/03-innovation-bets.md). This is where
[open question #4](../strategy/04-open-questions.md), whether the supplier side will pay for two-sided
value, gets concrete. A hypothetical, not a description of any provider.*

## Today

A regional building-products supplier invoices about 900 buyers. Getting paid is a research project.
It logs into eleven buyer portals, each with its own credentials and its own idea of what a remittance
looks like. Card payments arrive as a PDF emailed separately from the funds, so cash application is
manual and usually two days behind. A virtual card for $46,000 turns up carrying an acceptance cost
the supplier never priced into that order. Disputes run over email and take weeks. Three different
payment providers have called this quarter asking it to enrol again, each on behalf of one buyer.

The supplier is a recipient in every one of these models. Nobody has treated it as a user.

## What the supplier actually wants

- **Funds when promised**, on a date it can plan against, not a range.
- **Remittance data attached to the money**, so cash application happens without a person.
- **A choice of how to be paid**, priced transparently, rather than a card it must accept or a check
  it must wait for.
- **One enrolment that works across every buyer**, not one per buyer relationship.
- **A way to be paid earlier** when cash is tight, priced off its own history rather than a credit
  file.

## With the supplier as a first-class user

The supplier enrols once, and that enrolment is a durable network record rather than a per-buyer
artifact:

- **A directory profile.** Verified identity, bank details under change control, accepted methods with
  per-method pricing the supplier sets itself.
- **Straight-through remittance.** Structured ISO 20022 data travels with the payment, so the ERP
  applies cash automatically.
- **Preference read by the router.** The buyer's decisioning call takes the supplier's stated
  preference as an input, not an afterthought, and prices the trade-off openly.
- **Self-serve early pay.** "Take this $46,000 nine days early for 0.4%," priced from payment
  behaviour the network has already observed.
- **Dispute tooling.** Raise, evidence and track in one place instead of an email chain.

Every new buyer that joins inherits the enrolment. Enablement stops being rebuilt per relationship and
starts compounding.

## What changes

| Dimension | Before | After |
|---|---|---|
| Enrolment | Once per buyer, by phone | Once per network, self-serve |
| Remittance | PDF by email, applied by hand | Structured data with the funds, applied automatically |
| Payment method | Whatever the buyer chose | Supplier preference priced and honoured |
| Being paid early | Factoring, negotiated separately | An offer in flow, priced on network history |
| Bank detail changes | Email, and a live fraud vector | Change control with out-of-band verification |
| The supplier's status | A recipient | A user, with its own reasons to stay |

## Why this is a bet and not a feature

The buyer-weighted model gives the buyer rebates and float and asks the supplier to absorb acceptance
cost. That holds only while the supplier has no alternative, and real-time rails that carry structured
data are exactly that alternative. A provider whose supplier proposition stays thin will watch
acceptance leak to rails that pay it nothing and carry no relationship.

Turning enablement into a network inverts the economics. The cost of onboarding a supplier is paid
once and earned back across every buyer that later pays it, which is the only version of supplier
enablement that improves with scale rather than growing linearly with it. It also creates the
two-sided position that the [commercial model](../commercial/08-commercial-model.md) depends on: the
supplier side becomes a revenue function, not a cost centre.

## Signals it's working

Supplier-initiated enrolment rate (up, and the key one: suppliers coming to the network rather than
being chased); repeat suppliers reused across buyers; share of payments where the supplier is engaged
rather than merely paid; supplier-side revenue as a share of the relationship; supplier satisfaction
measured separately from buyer satisfaction.

## Risks

Suppliers accept the free rails and decline to pay for anything, leaving a better experience with no
business model attached ([open question #4](../strategy/04-open-questions.md)); enablement stays a
cost centre because it is funded and staffed as one; the directory becomes a competitive weapon rather
than shared infrastructure, so no network reaches useful coverage; and buyer-side economics have to be
given up to fund the supplier proposition faster than the supplier-side revenue arrives.
