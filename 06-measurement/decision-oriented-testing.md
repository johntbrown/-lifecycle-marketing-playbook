# Decision-Oriented Testing

## Thesis

The goal of testing is not to generate test volume. It is to produce learning that changes what the business does next.

Every test should begin with a decision, not a variant.

## Test Design Standard

Before launch, document:
- business question
- customer problem
- hypothesis
- primary metric
- guardrails
- audience
- control
- treatment
- expected direction / magnitude
- minimum runtime or sample logic
- decision rule
- owner

## The Decision Question

A strong test can finish this sentence:

> If this works, we will ______. If it does not, we will ______.

If the answer is “we will run another test,” the original test may not be decision-oriented enough.

## When To Use Holdouts

Use holdouts when you need to understand incrementality rather than attribution.

Examples:
- Email-only vs Email + SMS
- lifecycle communication vs no communication
- billing reminder vs existing experience
- loyalty reward vs no reward
- proactive save intervention vs business-as-usual

## Avoid Confounded Tests

If treatment changes multiple things at once, be explicit about what the test can and cannot tell you.

Example:
If treatment receives a reward plus three additional emails while control receives neither, the result measures the package, not the reward alone.

## Test Hierarchy

Prioritize tests that answer meaningful business questions:

1. Customer / product fit
2. Offer and value proposition
3. Journey / timing
4. Segmentation and personalization
5. Channel contribution
6. Creative execution
7. Micro-optimizations

Do not spend disproportionate time optimizing subject lines while larger lifecycle questions remain unanswered.

## Readout Structure

Use:
1. **Answer**: what happened?
2. **Evidence**: what supports that conclusion?
3. **Decision**: what are we doing because of it?
4. **Unknowns**: what still needs to be learned?

## Principle

Testing should create organizational memory. Maintain a durable test repository so the same question is not repeatedly re-tested because prior learning disappeared into slides, Slack, or individual memory.
