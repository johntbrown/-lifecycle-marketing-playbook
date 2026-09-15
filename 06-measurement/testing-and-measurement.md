# Testing and Measurement

## Principle

A lifecycle test should exist to make a decision.

Testing for activity's sake creates noise, slows teams down, and produces results that are difficult to apply. A strong test starts with a clear business question and ends with a clear action.

## Test Design

Every meaningful test should define:

- **Business question**: what are we trying to understand?
- **Hypothesis**: what do we believe will happen, and why?
- **Audience**: who is eligible, and who is excluded?
- **Primary outcome**: what metric determines the decision?
- **Guardrails**: what could improve locally while hurting the business elsewhere?
- **Decision rule**: what will we do if the result is positive, negative, or inconclusive?

## Measurement Hierarchy

Prioritize metrics in this order:

1. **Business outcome**
   - conversion
   - rebill
   - retention
   - LTV / contribution

2. **Customer behavior**
   - product adoption
   - subscription action
   - module completion
   - offer redemption

3. **Channel behavior**
   - click
   - reply
   - site visit

4. **Diagnostic engagement**
   - open
   - view
   - impression

The closer a metric is to the business outcome, the more weight it should carry in the final decision.

## Incrementality

Attributed revenue is not the same thing as incremental revenue.

Use holdouts when the business decision warrants them, especially when evaluating:

- adding a new channel
- increasing contact pressure
- introducing an offer or discount
- loyalty rewards
- billing / renewal communications

## Cohort Thinking

Lifecycle performance should be read by customer cohort whenever possible.

Useful cuts include:

- acquisition source
- first product
- subscription type
- pack / cadence
- lifecycle treatment
- acquisition offer
- customer intent / need-state

## Source of Truth

Before reporting a metric, define:

- the event
- the customer identifier
- the system of record
- the time window
- the inclusion / exclusion logic
- whether the number is event-level, user-level, or order-level

A dashboard is not a source of truth unless its underlying definitions are understood and documented.
