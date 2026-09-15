# Case Study: From A/B Testing to Decision-Oriented Testing

> Portfolio-safe example. Company-specific data and names are intentionally omitted.

## The Problem

A testing program had accumulated many experiments but very few decisions. Tests were often framed as “Version A vs Version B” without a clear business question or next action.

The result was test volume without organizational learning.

## Weak Test

**Question:** Which subject line wins?

Problems:
- no defined business implication
- often optimized a diagnostic metric
- winner could be too small to matter
- learning rarely changed the roadmap

## Better Test

**Business question:** Does adding a second channel create incremental conversion in the first 30 days?

**Hypothesis:** Customers receiving coordinated Email + SMS will convert at a higher rate than Email-only without unacceptable unsubscribe or complaint pressure.

**Primary metric:** lead-to-first-order conversion

**Guardrails:** unsubscribe, spam complaint, contact pressure

**Decision rule:**
- positive incremental lift → expand coordinated channel strategy
- no lift → keep Email-only as default and reserve SMS for high-intent behavior
- negative guardrails → reduce pressure or change trigger logic

## Operating Change

Every test brief now requires:
- business question
- hypothesis
- control
- treatment
- primary metric
- guardrails
- decision rule
- what changes next

## Lesson

A test is valuable only when the organization knows what decision the result will inform.
