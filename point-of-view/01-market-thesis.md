# The forces reshaping corporate money movement

*Context for [the horizon model](02-four-horizons.md). An industry view, deliberately
built on structural evidence rather than market-size figures. The argument should hold even with every
TAM number removed.*

## The shift, stated plainly

The last era of commercial payments rewarded placing an instrument inside a workflow and earning
economics on the volume. The next era rewards operating the layer that decides *how* money moves and,
increasingly, *executes* the movement: rail, funding source, risk posture, financing, FX, settlement
timing, reconciliation, as one orchestrated flow rather than a sequence of disconnected steps.

That layer is where the corporate relationship will sit. The instrument becomes a component of it.

Stated as a contrast: today it is disconnected workflows, manual routing decisions and fragmented
infrastructure; the direction is one intent, an intelligent decision, optimised execution and
continuous reconciliation. The move is not automating one finance process — it is coordinating the
decisions that determine how corporate money moves.

## Four structural forces

### 1. Multi-rail is becoming the default
Real-time rails now carry structured remittance data through ISO 20022, which removes the historical
reason to prefer cards for reconciliation. Card, ACH, real-time, cross-border and check-outsource are
becoming peers, chosen per transaction on cost, speed, acceptance and working-capital impact. Rail
*selection*, not rail *access*, is the emerging product surface.

### 2. The workflow is consolidating around software
Finance teams increasingly expect to pay, get paid, forecast and reconcile inside the systems they
already run: ERPs, vertical software, treasury tools. The participant embedded in that workflow
influences the payment decision before a payments provider is ever chosen. This is what puts software
platforms in the orchestration conversation at all.

### 3. Value is moving from the record to the decision
"Payment, then transaction record" is being replaced by "payment, then decision, then action." Each
transaction is an opportunity to choose the rail, the funding source, the risk and identity posture,
and whether to extend credit, computed in real time. The same first-party data (observed revenue,
volume, seasonality, buyer concentration, refunds, receivables) is a stronger underwriting input than
a credit file, which quietly turns payments into a financing business.

### 4. Software is beginning to act
Agentic tooling in finance operations is moving from experimentation toward infrastructure. Invoice
intake, matching, approval routing and payment scheduling are increasingly executed by software rather
than surfaced to a person. This does not require believing any particular protocol wins; it requires
only that a growing share of payment *initiation* stops being a human action.

## The unresolved question: closed or open

These forces do not name a winner. They sharpen a structural question:

| Archetype | Structural advantage | Structural constraint |
|---|---|---|
| **Closed-loop financial platform** | Richest data; tight risk-to-financing-to-settlement loop; integrated funding; two-sided network effects; experience control | Legacy and post-acquisition fragmentation; proprietary-rail incentives versus customer-optimal routing; interoperability limits; regulatory weight |
| **Payment network** | Reach; trust; emerging identity and agent-authorization standards | Limited presence in the workflow itself |
| **Bank** | Balance sheet; regulatory perimeter; treasury relationships | Slower product cycles; thinner software distribution |
| **ERP or software platform** | Owns the workflow and the customer's attention | Lacks rails, funding, risk infrastructure |
| **Fintech infrastructure or orchestrator** | Rail-neutral; fast; interoperable by design | Holds neither the customer relationship nor the balance sheet; must earn trust as a layer |

The closed-loop model's advantages and constraints come from the same property: control. The open
model's speed and neutrality come at the cost of the relationship and the balance sheet. Whether
orchestration is won by *owning* the loop or by being the *most trusted interoperable layer across
loops* is the open question this package keeps returning to (see [open questions](04-open-questions.md)).

## What the evidence supports today

A few things can be said with reasonable confidence:

- **Rail adoption is broad-based, not niche.** Enterprise intent to add real-time payments over the
  next two years is measured in majorities, not early adopters
  ([PYMNTS, 2026](https://www.pymnts.com/real-time-payments/2026/53percent-businesses-plan-rtp-adoption-payment-habits-shift/)).
- **AI is already inside finance operations.** A majority of AP organisations report using or piloting
  AI, with autonomous processing rates on standard invoices well past half by the first year of use
  ([Forrester, 2026](https://www.forrester.com/blogs/top-agentic-ai-use-cases-for-ap-automation-in-2026/)).
- **Agent-authorization standards are being built now.** Multiple identity-and-authority frameworks
  for software-initiated payments are in active development across networks and platforms
  ([overview](https://universalcommerceprotocol.fr/en/visa-mastercard-agentic-commerce/)).
- **Embedded finance in B2B is scaling faster than the broader category**, though published estimates
  vary widely enough that no single figure should carry weight in a strategy argument.

## Counter-arguments worth holding

- **"The instrument stays the margin engine for a decade."** Plausible. Rebate and float economics
  are sticky and enterprise change is slow. A strategy that assumes the instrument is permanent is
  fragile; one that assumes it disappears quickly is probably early.
- **"Orchestration is a feature, not a layer."** Possible if platforms and networks each absorb the
  routing logic for their own flows. Then the value is in interoperability, not aggregation.
- **"Agentic payments are over-hyped."** The timeline is genuinely uncertain. The direction, less
  human initiation and more software initiation, is not.

## Sources

- PYMNTS, "53% of Businesses Plan RTP Adoption" (2026): https://www.pymnts.com/real-time-payments/2026/53percent-businesses-plan-rtp-adoption-payment-habits-shift/
- Forrester, "Top Agentic AI Use Cases For AP Automation In 2026": https://www.forrester.com/blogs/top-agentic-ai-use-cases-for-ap-automation-in-2026/
- Agent-authorization standards overview: https://universalcommerceprotocol.fr/en/visa-mastercard-agentic-commerce/
