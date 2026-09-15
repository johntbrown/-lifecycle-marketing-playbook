# Customer State Model

## Thesis

Lifecycle personalization works best when customer state is explicit.

A customer should not be treated as a collection of unrelated campaign memberships. The system should know where the customer is in the relationship, what they have done, what they are eligible for, and what problem is most likely to matter next.

## Core Relationship States

Examples:
- Lead
- One-Time Purchaser
- Active Subscriber
- Paused Subscriber
- Former Subscriber
- Lapsed Purchaser

Relationship state should be separate from:
- engagement state
- churn risk
- product ownership
- eligibility
- acquisition source
- consent status

This prevents one field from trying to answer five different business questions.

## Example Precedence

When multiple states are possible, define precedence so the customer resolves consistently.

A typical precedence could be:
1. Active Subscriber
2. Paused Subscriber
3. Former Subscriber
4. One-Time Purchaser
5. Lead

## Why This Matters

A durable state model powers:
- mutually exclusive messaging
- suppression logic
- onboarding eligibility
- save and winback routing
- cross-sell
- loyalty
- reporting
- consistent handoffs between acquisition and retention

## Source of Truth

For each state or property, document:
- definition
- source system
- update cadence
- precedence
- owner
- downstream destinations

The lifecycle team should not have to guess whether a property is current, dynamic, or historical.

## Principle

Good personalization starts with good state management. Before adding more campaigns, make sure the business agrees on who the customer is right now.
