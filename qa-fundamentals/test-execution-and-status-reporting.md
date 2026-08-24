# Test Execution & Status Reporting

**Read time:** 4 min

---

Execution is where the plan meets reality. Status reporting is how
everyone *not* in the execution weeds — stakeholders, other teams,
leadership — stays informed without needing to ask.

## Executing well

- **Log results as you go, not in a batch afterward** — memory of exact
  behavior fades fast, and batch-logging hours later produces vaguer,
  less useful defect reports
- **Follow the test case, but don't ignore what you notice outside it**
  — a scripted test case that says "verify X" doesn't mean ignore the
  unrelated glitch you spotted while doing it; log it separately
- **Track execution status granularly**: Passed, Failed, Blocked,
  Not Run, Skipped — "Blocked" (can't execute due to an external
  dependency/environment issue) is a distinct, important status, not
  the same as "Failed" — conflating them hides real environment
  problems inside what looks like a feature-quality problem

## What a status report actually needs to answer

Whoever reads a status update — daily standup, weekly steering
committee, or a one-off "how's testing going" ask — needs the same core
answers, at different levels of detail:

- **Where are we against the plan?** (% executed, % passed)
- **What's blocking progress right now?**
- **What's the current defect picture** (open count by severity, any
  new Critical/High since last update)
- **Are we still tracking to the exit criteria and timeline, and if
  not, by how much and why?**

## Matching detail to audience

- **Daily (team-internal):** granular — specific blockers, specific
  failing tests, specific next actions
- **Weekly (cross-team/stakeholder):** summarized — trend lines (are we
  converging or diverging from the plan), key risks, no need for
  every test case's individual status
- **Milestone/release-level (leadership):** outcome-focused — go/no-go
  readiness against exit criteria, headline risk if any, not process detail

Sending the daily-detail version to a leadership audience (or the
leadership-summary version to the team doing the work) is a common,
avoidable mistake — match the report to what the specific audience
actually needs to act on.

## Best Practices

- Report bad news as clearly as good news — a status report that only
  ever says "on track" until the day it suddenly isn't has failed at
  its actual job, which is early warning
- Use the same status categories consistently across reports so trend
  lines are actually comparable week to week
- Automate what can be automated (pass/fail counts from a test
  management tool) and reserve human judgment for what can't (risk
  assessment, "why" behind a trend)

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [QA & Testing Fundamentals](./README.md)*
