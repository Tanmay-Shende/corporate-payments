# Worked example: working capital underwritten on payment data

*Illustrates [Horizon 2](../strategy/02-four-horizons.md) and
[bet 4](../strategy/03-innovation-bets.md). This is where
[open question #6](../strategy/04-open-questions.md), the consent model for payment data, stops being
abstract. A hypothetical, not a description of any provider.*

## Today

A specialty-food distributor turns over $40M a year, heavily weighted to the fourth quarter. In
September it needs $1.2M of inventory to serve a November peak it can forecast with some confidence,
because it has run the same cycle for six years.

Its bank asks for two years of financials, a personal guarantee and five weeks. The decision rests on
a credit file assembled fourteen months ago, which knows the company's filed accounts and nothing
about the fact that its top twenty buyers have never paid late. By the time the line is approved, the
buying window has closed and the distributor has funded a smaller order from cash.

The payment platform it already uses, meanwhile, has watched every one of those cycles.

## What the platform can see that the lender cannot

- **Observed revenue** rather than stated revenue: settled inflows, already verified.
- **Buyer concentration and quality**: who pays, how quickly, how reliably, and how that has moved.
- **Seasonality across several complete cycles** of this specific business.
- **Receivables in flight**: invoices issued, approved and scheduled but not yet settled.
- **Refunds and disputes** as a live quality signal on the underlying trade.
- **Behaviour on the paying side**: whether the company pays its own suppliers on time.

That set is a stronger underwriting input than a credit file, and it refreshes daily rather than
annually. It is also first-party data, which is the part an external lender cannot replicate at any
price.

## With embedded working capital

The offer appears where the decision already is, rather than in a separate application:

- **In the AP workflow.** "Extend terms on this $340k order to 60 days for 1.1%," shown at the moment
  the order is approved.
- **In the treasury view.** "Advance $800k against these 47 approved invoices," priced from the
  observed payment behaviour of those specific buyers.
- **At the seasonal moment.** A pre-approved line, sized to the pattern the platform has already seen
  twice, drawn down in the same session rather than applied for.

Underwriting runs continuously, so the limit tracks the business instead of resetting at renewal. The
same real-time decisioning layer that chooses a rail is choosing whether to lend, which is what makes
this affordable to operate rather than a separate credit business bolted alongside.

## What changes

| Dimension | Before | After |
|---|---|---|
| Underwriting input | Filed accounts, 14 months stale | Observed cash flow, refreshed daily |
| Time to decision | Five weeks | In session |
| Where the offer appears | A separate application | Inside the workflow that created the need |
| Limit | Fixed until renewal | Moves with observed performance |
| Security | Personal guarantee | Receivables the platform can already see and settle |
| Seasonal peak | Funded from cash, order cut | Funded to the forecast the data supports |

## The consent problem this creates

This is the genuinely unresolved part, and it should not be waved past. Payment data is the strongest
underwriting input available precisely because the customer generated it while doing something else.
Using it to price credit needs a model the customer accepts and a regulator will bless: explicit
purpose limitation, opt-in per use rather than a blanket term, portability so the customer can take
its own history elsewhere, and ideally a visible share of the value back.

Get this wrong and the failure is not a compliance finding, it is that customers route flows away to
avoid being scored. The data advantage is self-limiting: it exists only as long as customers are
willing to keep producing it (see [open question #6](../strategy/04-open-questions.md)).

## Which archetype is well placed to run this?

It needs both halves. A participant with **balance-sheet access and first-party flow data** can see
the risk and fund it, whether through an owned charter or a deep banking-as-a-service relationship. A
**rail-neutral orchestrator** sees much of the same flow but has no balance sheet, so it can originate
and must place the credit elsewhere, keeping a thinner margin. A **bank** has the funding but sees
only its own slice of the flow and none of the invoice context.

The instructive point is that this bet is the one that pays for
[bet 3](../strategy/03-innovation-bets.md). Orchestration on its own erodes instrument economics;
financing attached to the same decision is what replaces them.

## Signals it's working

Attach rate of financing to payment volume; loss rates at or below comparable products; limit
utilisation (an unused limit is a mispriced one); incremental margin per transaction; retention on
financed accounts; and the honest one, whether customers widen data permissions over time or narrow
them.

## Risks

Credit losses in a downturn, made worse because the data is procyclical and looks strongest just
before it turns; adverse selection, where the customers who accept the offer are the ones who could
not get cheaper money elsewhere; regulatory scrutiny of embedded lending, which arrives faster when
the lender is also the payment rail; and the data-advantage-versus-trust tension, which is the one
that can undo the rest of the platform rather than just this product.
