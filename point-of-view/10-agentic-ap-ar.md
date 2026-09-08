# Worked example: software-run AP/AR inside the system of record

*Illustrates [Horizon 3](../strategy/02-four-horizons.md) and [bet 6](../strategy/03-innovation-bets.md).
A hypothetical. It assumes only that autonomous invoice processing on standard invoices is already
common in finance operations, which it is
([Forrester, 2026](https://www.forrester.com/blogs/top-agentic-ai-use-cases-for-ap-automation-in-2026/)).*

## The setup

A services firm turns on an **AP agent** inside its ERP. The agent operates under a **scoped mandate**
that is issued and enforced outside the agent itself:

- Counterparties: only those on the approved supplier directory.
- Amount: up to a set threshold per invoice without human approval; above it, route to a named
  approver.
- Conditions: 3-way match required; no duplicate invoice numbers; no new bank details without
  out-of-band verification.
- Rails: the agent may choose among approved rails per the routing policy.
- Every action logged, explained, reversible.

## A week in the life

- **Intake.** The agent ingests about 220 invoices from email and EDI, validates fields, matches most
  to POs and receipts automatically.
- **Exceptions.** The unmatched remainder is triaged: the agent clears the ones with a clean
  resolution (receipt now posted, price within tolerance) and escalates the rest with a written
  summary of what is wrong.
- **Scheduling.** Clean invoices are scheduled on due date, with a few pulled forward where an
  early-pay discount beats the cost of the cash.
- **Payment.** Each payment goes through the decisioning layer for rail and funding source. One is
  **blocked**: the supplier's bank details changed this week and the mandate requires out-of-band
  verification, so it is held and flagged.
- **Close.** The agent posts reconciliation entries and a one-page summary: paid, discounts captured,
  exceptions outstanding, and the blocked payment with its reason.

The human AP team handled the handful of genuine judgment calls, not the queue.

## What sits beneath the agent

The agent framework decides. Someone else has to provide the things that make an autonomous payment
safe:

- **Verified agent identity**, aligned to the cross-industry authorization standards now being built.
- **Mandate enforcement at the rails**, scope limits enforced in infrastructure, not only in a prompt.
- **Decision governance**, every agent payment running the same real-time decisioning and fraud and
  identity checks as a human-initiated one.
- **Settlement certainty**, a defined party standing behind the movement.
- **Audit and reversal**, a complete, explainable log; any action can be unwound.

## Why this is a strategic position, not a feature

An agent that can *decide* is becoming common. A decision that is **scoped, enforced, governed,
settled and reversible by a trusted party** is not. That gap is the product. Which archetype fills it
is open: a closed-loop participant can offer enforcement and settlement as one integrated service; a
network can offer identity and standards at reach; a bank can offer the settlement guarantee. The
likely outcome is a division of labour, which is exactly why identity and authority are worth
standardising rather than owning.

**When software moves money autonomously, trust becomes part of the payment product.**

## Signals it's working

Share of invoice volume processed without human touch (up); escalations that are genuine judgment
calls rather than agent errors (up as a proportion); blocked or reversed agent payments (low, and
mostly correct); customers widening mandates over time (the real trust signal).

## Risks

Committing to an authorization standard that does not win; **liability allocation is unresolved** (see
[open questions #3](../strategy/04-open-questions.md)); an over-broad mandate plus a model error moves
real money; trust is fragile, and one bad autonomous payment can set a customer's adoption back a year.
