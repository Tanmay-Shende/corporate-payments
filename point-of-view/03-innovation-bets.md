# Where to place bets

*Six positions that follow from [the forces](01-market-thesis.md) and [the horizons](02-four-horizons.md).
Each is framed as an industry bet, "here is where the value concentrates and why," with the signal
that would confirm it and the risk that would break it. For each, the harder question is not whether
it matters but whether it is a capability to **own**, to **partner** for, or to make **interoperable**.*

---

## Bet 1. The unified transaction core (Horizon 0)

**Thesis.** The participants that compete effectively above Horizon 0 are the ones that collapsed many
authorization and processing stacks into one configuration-driven, real-time, multi-rail core with
shared pre-transaction, transaction and post-transaction services.
**Own, partner or interoperate.** Own. This is the differentiated substrate; it cannot be outsourced
without giving away the economics of everything above it.
**Signal.** New-product time-to-launch falls; distinct authorization paths shrink; unit processing
cost falls; a clear majority of volume runs on the unified core.
**Risk.** Treated as "tech-debt cleanup," under-funded, and never reaching the point where new
products actually compose it. Half a platform is worse than none.

---

## Bet 2. The supplier side as a product and a network (Horizon 1)

**Thesis.** The buyer-weighted model, where buyers get rebates and float and suppliers absorb
acceptance cost, is under pressure. Value concentrates around participants that make the supplier
experience first-class (fast funds, straight-through reconciliation, financing, dispute tooling) and
turn enablement into a reusable network. (See [worked example](../examples/12-supplier-enablement.md).)
**Own, partner or interoperate.** Own the supplier relationship and the network; interoperate on the
directory standards that let suppliers be reached across providers.
**Signal.** Supplier-initiated enablement rate; repeat suppliers reused across buyers; supplier
satisfaction; share of volume where the supplier is engaged, not merely paid.
**Risk.** The supplier proposition stays thin, enablement remains a cost centre, and acceptance keeps
leaking to free rails with no offsetting relationship.

---

## Bet 3. Multi-rail orchestration as a decision surface (Horizons 1 and 2)

**Thesis.** Rail selection becomes a visible, governed decision optimised per transaction on cost,
speed, acceptance and working-capital impact. (See [worked example](../examples/09-intelligent-payment-orchestration.md).)
**Own, partner or interoperate.** Own the decision logic; partner for rail access where scale is not
differentiating; interoperate on the data formats that make routing portable.
**Signal.** Non-card rail mix rises without margin collapse; customers configure policy rather than
accept defaults; blended cost per dollar moved improves.
**Risk.** Orchestration cannibalises instrument economics faster than new value (financing, treasury,
data) replaces it. This bet has to be paired with Bet 4 or 5, not shipped alone. It also forces the
**card-economics-versus-rail-neutrality** tension into the open: a layer that visibly optimises for its
own margin loses credibility as an orchestrator.

---

## Bet 4. Data-underwritten embedded working capital (Horizon 2)

**Thesis.** First-party payment data underwrites financing embedded in the flow, pay-early,
term-extension, invoice financing, priced from live revenue, volume, seasonality and concentration.
(See [worked example](../examples/13-embedded-working-capital.md).)
**Own, partner or interoperate.** Own the underwriting models and the decision; partner for
balance-sheet capacity where a charter is not available; keep the consent model explicit and portable.
**Signal.** Attach rate of financing to payment volume; loss rates at or below comparable products;
incremental margin per transaction; retention on financed accounts.
**Risk.** Credit losses in a downturn; regulatory scrutiny of embedded lending; data-use missteps
that damage trust. This bet lives or dies on risk discipline and on the **data-advantage-versus-trust**
tension.

---

## Bet 5. The real-time decisioning layer (Horizon 2)

**Thesis.** One in-line decision per transaction, rail, funding, fraud and identity, financing offer,
settlement timing, as a shared capability every product calls.
**Own, partner or interoperate.** Own. It is the connective tissue between the core and every product,
and the thing that makes Horizon 3 safe.
**Signal.** Authorization rate up at constant fraud loss; decision latency within budget; number of
products consuming the layer; measurable margin contribution.
**Risk.** Built as a fraud tool only and never extended to rail, funding or credit, so it
under-returns the investment; or governance lags capability and creates regulatory exposure.

---

## Bet 6. Trust rails for software-initiated payments (Horizon 3)

**Thesis.** As software initiates more payments, value accrues to whoever provides verified agent
identity, scoped mandates, policy enforcement, auditable decisions and settlement certainty. (See
[worked example](../examples/10-agentic-ap-ar.md).)
**Own, partner or interoperate.** Interoperate on identity and authorization standards; these are
worth more shared than proprietary. Own the enforcement, settlement and audit that sit behind them.
**Signal.** Share of volume initiated by software; straight-through rate on agent flows; low dispute
and reversal rates; customers widening mandates over time.
**Risk.** Committing early to a standard that loses; or moving late and letting a network or platform
become the default. Liability allocation is genuinely unresolved (see [open questions](04-open-questions.md)).

---

## How the bets relate

- **Bet 1 is the foundation.** Without it, 2 through 6 are priced at fragmentation cost.
- **Bet 3 needs Bet 4 and 5.** Orchestration alone erodes margin; paired with financing and
  decisioning it grows the relationship.
- **Bet 6 needs Bet 5.** Trust rails for software are only safe once decisions are governed, priced
  and auditable.
- **No participant needs all six.** The strategic act is choosing which to own outright, which to
  partner for, and which to help standardise so the whole market, including competitors, can build on
  them.

## Three pillars a product leads with

The six bets are the map for where to invest. A product built on them communicates as three:

- **Intelligent money movement.** Every payment optimises *rail × funding × timing* together, as one
  governed, explainable decision rather than a static rule. Rolls up Bets 1, 3 and 5.
- **Network.** Suppliers, customers, banks and financial infrastructure connected through reusable,
  verified identity, so platform value compounds as buyers × suppliers rather than buyers + suppliers.
  Rolls up Bets 2 and 4.
- **Autonomous finance.** Software executes whole finance workflows within explicit mandates, policies
  and limits, every action logged and reversible. Bet 6, made safe by Bet 5.

The pillars are how the strategy is *narrated*; the bets are how it is *resourced*. They describe the
same thing at two altitudes.
