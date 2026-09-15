# Dunning and Involuntary Churn

## Thesis

Not every churn event is a customer choosing to leave. Failed payments, broken event logic, delayed state transitions, and migration issues can create retention loss that is partly operational.

That means involuntary churn should be managed as its own lifecycle system.

## Core Funnel

Track:

**payment failure → dunning entry → recovery attempts → payment update → successful rebill OR cancellation**

The critical requirement is a clean exit state. Customers should not remain stuck in dunning indefinitely because a downstream cancellation event never fires.

## Operating Questions

For every dunning program, know:
- what event starts dunning
- what attempts are made and on what cadence
- which channels are used
- what event marks recovery
- what event marks terminal failure
- how the customer state changes afterward
- whether failed attempts create duplicate messaging or support contacts

## Measurement

Primary:
- dunning entry rate
- recovery rate
- time to recovery
- terminal involuntary churn rate

Secondary:
- support contacts
- payment-method update rate
- downstream retention after recovery
- refund / dispute behavior

## Data Quality Warning

A sudden churn spike may be real customer loss but distorted timing.

Example pattern:
- customers fail payment
- they complete the dunning experience
- no terminal exit event fires
- accounts remain in limbo
- a later bulk update moves them all to canceled

The churn is real, but the reporting date is not the actual date the relationship broke.

## Principle

Treat involuntary churn as both a lifecycle problem and an operational systems problem. The best email copy cannot fix a broken subscription-state machine.
