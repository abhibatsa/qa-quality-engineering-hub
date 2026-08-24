# Test Estimation Techniques

**Read time:** 4 min

---

"How long will testing take?" is asked on every project, usually before
enough information exists to answer it precisely — the actual skill is
producing a *defensible* estimate, not a perfectly accurate one.

## Common estimation techniques

- **Work Breakdown Structure (WBS)** — break testing into discrete
  tasks (test case design, execution, regression, reporting), estimate
  each, sum up. Most intuitive, most commonly used.
- **Test Case Point (TCP) / Function Point-based estimation** — estimate
  based on the complexity and count of functional points/test cases,
  useful when requirements are well-defined early
- **Three-point estimation** — estimate optimistic, pessimistic, and
  most-likely durations, then use a weighted average (commonly
  `(optimistic + 4×most-likely + pessimistic) / 6`) — useful specifically
  because it forces you to think about the pessimistic case explicitly,
  not just hope for the most-likely one
- **Historical/comparative estimation** — "the last similar feature took
  X days to test" — often the most accurate technique available, when
  you actually have comparable history to draw on

## What actually makes an estimate defensible

Not precision — **stated assumptions**. "Testing will take 5 days,
assuming the build is stable at handoff and no more than 2 environment
blockers" is a defensible estimate. "Testing will take 5 days" with no
stated assumptions is a number that will be wrong and blamed on QA when
it is, even though the actual cause was an unstable build or environment
issues nobody accounted for.

## The estimation trap to know by name

**Anchoring** — once a number is said out loud (even informally, even as
a guess), it becomes very hard to revise upward later, regardless of new
information. Protect against this by not giving a number until you've
actually done at least a rough WBS — a fast, informal guess said in a
hallway conversation has a way of becoming "the estimate" whether you
meant it to or not.

## Best Practices

- Always attach assumptions to an estimate, not just a number
- Build in explicit buffer for defect-fixing and re-testing cycles —
  first-pass execution time is not the same as total testing time, and
  conflating them is the most common estimation error
- Track estimated vs. actual after each project — this is the only way
  historical/comparative estimation actually improves over time

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [QA & Testing Fundamentals](./README.md)*
