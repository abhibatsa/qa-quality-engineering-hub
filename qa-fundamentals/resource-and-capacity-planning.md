# Resource Estimation & Capacity Planning

**Read time:** 3 min

---

Test estimation ([covered separately](./test-estimation.md)) answers "how
much work is there." Resource and capacity planning answers a different
question: **do we actually have enough people, with the right skills,
available at the right time, to do that work?** Both can be right
independently and the project still slips if the second one is ignored.

## What capacity planning actually involves

- **Headcount vs. workload** — how many testers, at what percentage
  allocation (someone at 50% on this project isn't a full resource for it)
- **Skill matching** — a manual-only tester can't absorb automation work
  just because they're available; matching skill to task is as important
  as matching hours
- **Parallel vs. sequential work** — some testing can be parallelized
  across testers, some can't (e.g., one person needs to own end-to-end
  regression for consistency) — this affects how much adding headcount
  actually helps
- **Ramp-up time** — a new team member added mid-project doesn't
  contribute at full capacity immediately; budget onboarding time
  explicitly rather than assuming day-one full output

## The mistake that costs the most

Treating "add more testers" as a linear fix for a timeline problem.
Brooks's Law ("adding manpower to a late project makes it later") applies
to testing too — a tester unfamiliar with the feature, the environment,
and the existing test suite doesn't multiply capacity in their first
days; they consume the existing team's time in onboarding.

## Best Practices

- Plan capacity at the *actual allocation percentage*, not headcount —
  three people at 30% each is not one full-time equivalent's worth of
  reliable throughput, due to context-switching costs
- Account for ramp-up time explicitly when adding someone mid-project,
  rather than assuming immediate full contribution
- Flag skill gaps early, not at execution time — "we need someone who
  knows API testing for this phase" is a staffing conversation to have
  during planning, not a surprise discovered mid-sprint

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [QA & Testing Fundamentals](./README.md)*
