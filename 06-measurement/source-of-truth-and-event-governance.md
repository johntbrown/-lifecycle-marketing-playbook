# Source of Truth and Event Governance

## Thesis

Lifecycle strategy breaks down quickly when the team cannot agree on what an event means, where it came from, or which system owns the truth.

Data governance is not just a technical concern. It is a growth operating system.

## For Every Metric or Event, Define

- business definition
- event name
- source system
- destination systems
- owner
- update cadence
- historical availability
- known exclusions
- whether it is profile state, event history, or derived logic

## Common Failure Modes

### Same label, different meaning
Example: “completion” may mean entered, clicked, finished, or earned a reward.

### Event exists but field is missing downstream
The event may arrive while a property never materializes in the warehouse schema.

### State transitions happen late
A customer may be behaviorally churned before the reporting system marks them canceled.

### Vendor and internal definitions diverge
A vendor may report clicks while an internal team assumes the number represents completed subscription changes.

## Reconciliation Process

When numbers disagree:
1. Start from raw user-level events.
2. Use a stable unique identifier.
3. Compare event timestamps.
4. Reconstruct the funnel step by step.
5. Separate views, clicks, completions, and downstream outcomes.
6. Agree on one durable definition.
7. Document it in the source-of-truth inventory.

## Useful Funnel Pattern

**entered experience → viewed module → completed module → clicked offer → downstream action → retained outcome**

Each step should have a distinct event and definition.

## Principle

Never solve a definition problem by adding another dashboard. Fix the underlying contract first.
