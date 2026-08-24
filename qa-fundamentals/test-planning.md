# Test Planning

**Read time:** 4 min

---

A test plan answers one question for everyone who isn't you: **how will
we know this is ready to ship, and what could still go wrong?** Skipping
it doesn't skip the thinking — it just means the thinking happens
ad hoc, undocumented, and inconsistently across the team.

## What a real test plan actually contains

- **Scope** — what's being tested, and explicitly, what's *not* (out-of-
  scope is as important to state as in-scope — it's what prevents "wait,
  why didn't QA catch that?" after launch)
- **Test approach/strategy** — manual vs automated split, which test
  levels apply (unit/integration/system/UAT), risk-based prioritization
- **Entry and exit criteria** — what has to be true before testing
  starts (build deployed, environment ready) and what has to be true to
  call it done (pass rate threshold, no open Critical/High defects)
- **Resources and timeline** — who's doing what, by when (see
  [Resource Estimation & Capacity Planning](./resource-and-capacity-planning.md))
- **Test environment requirements**
- **Risks and assumptions** — what could derail the plan, and what
  you're assuming to be true without verifying

## The part most plans get wrong

**Vague exit criteria.** "Testing is complete when all test cases pass"
sounds fine until a P1 defect is found with one test case left to run —
is that "done"? A real exit criteria section defines pass-rate
thresholds *and* defect-severity thresholds together, so there's no
ambiguity when reality doesn't cooperate with the plan.

## Scaling the plan to the project

A one-page test plan for a small internal feature and a 10-page test
plan for a payments migration are both correct — for their respective
projects. The skill isn't writing an exhaustive document every time,
it's judging how much rigor the actual risk level demands. Over-
planning a low-risk change wastes time; under-planning a high-risk one
is how expensive defects reach production.

## Best Practices

- Write the exit criteria section *before* execution starts, not
  during — deciding "what counts as done" under deadline pressure, mid-
  execution, produces criteria that bend to the deadline instead of the
  actual risk
- State assumptions explicitly — "we assume the staging environment
  matches production configuration" is a sentence that saves a very bad
  day if it turns out to be false
- Revisit the plan when scope changes mid-project — a test plan written
  against week-1 requirements and never updated is worse than no plan,
  because it creates false confidence

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [QA & Testing Fundamentals](./README.md)*
