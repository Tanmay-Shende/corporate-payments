# Commercial model

*How the economics change as the category moves from an instrument business to an orchestration layer.
A point of view on the shifts, not a price list.*

## The starting economics

Commercial card economics have been **buyer-weighted**: the buyer earns rebates and float, the
supplier absorbs acceptance cost, the provider earns net interchange (interchange minus rebate minus
cost), and, where the provider holds a charter, funding spread on top. It has been a high-margin model
by payments standards, and the pressure on it comes from rail substitution and supplier pushback, not
from a cost problem.

## Four commercial shifts

### 1. From buyer-only to a shared value exchange
The supplier side has to receive real value, faster funds, guaranteed remittance data, financing,
dispute reduction, and pay for some of it. This is what stops acceptance leaking to free rails with
no relationship attached. Blended take rates compress on the raw card leg and are rebuilt through
supplier-side services and financing.

### 2. From one rail's economics to a portfolio
As orchestration routes volume across card, ACH, real-time and cross-border, revenue per dollar moved
varies by rail. The economics have to be managed as a portfolio: card stays the margin engine on the
flows where it earns its keep; other rails monetise through subscription, per-transaction fees, FX
and attached financing. The metric that matters is **margin per dollar moved across the whole
relationship**, not the take on any single leg.

This forces a strategic choice into the open, the **card-economics-versus-rail-neutrality tension**. An
orchestration layer that visibly steers volume to its own highest-margin rail is not trusted as an
orchestrator. Credibility requires routing to the customer's best option and monetising elsewhere.

### 3. From transaction fees to a stack of monetisation
| Layer | How it monetises |
|---|---|
| Instrument issuing | Net interchange plus funding spread |
| AP and AR automation | Subscription plus per-transaction plus supplier-side services |
| Multi-rail orchestration | Routing fee plus FX margin on cross-border |
| Treasury and balances | Deposit spread plus treasury-service fees |
| Embedded working capital | Net interest margin plus origination, underwritten on first-party data |
| Real-time decisioning | Priced into the products it improves (higher auth, lower loss) |
| Trust rails for software-initiated payments | Per-transaction trust and settlement fee |

As instrument interchange plateaus, the other layers can grow. Several of them, treasury and working
capital in particular, are easier for a participant with balance-sheet access, which is part of why
the closed-versus-open question is also a commercial question, not only a product one.

### 4. From flat pricing to packaged offers by motion
- **Embedded and platform partners:** wholesale rails plus revenue share; the partner owns the end
  customer and the brand.
- **Direct mid-market and enterprise:** packaged payments plus treasury plus financing, priced on
  value delivered (days-sales-outstanding improvement, discount capture, staff time), not per API call.
- **Banking and treasury:** relationship pricing anchored on balances.

## Go-to-market implications

- **Two motions, deliberately different.** A partnership and embedded motion (few, large,
  integration-led) and a direct motion (many, mid-market, solution-sold) need different pricing,
  enablement and packaging, and will sometimes compete for the same end customer. That has to be
  managed, not ignored.
- **Supplier enablement is a revenue function, not a cost function.** Fund it, staff it, measure it
  on network growth and supplier engagement.
- **Pricing power comes from the stack, not the instrument.** Switching cost is high because rails,
  treasury, financing, data and trust are integrated, not because moving a card program is hard.

## Metrics that matter

- **Net interchange rate:** the health of the core instrument economics.
- **Total volume processed versus monetised purchase volume:** the gap is the orchestration and
  treasury opportunity.
- **Revenue mix by layer:** instrument issuing versus AP and AR versus treasury versus financing; the
  direction of travel matters more than any single quarter.
- **Product attach rate:** financing attached to payment volume; treasury attached to AP.
- **Deposits and balances held:** the treasury flywheel.
- **Margin per dollar moved, by relationship:** the portfolio view that survives rail substitution.
- **Revenue per employee:** whether the unified platform and AI-native operating model are actually
  producing operating leverage.
