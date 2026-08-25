# Incident Reporting for QA

**Read time:** 3 min

---

A production incident is different from a defect found in testing —
it's already affecting real users, timing and communication matter more
than the eventual root-cause fix, and QA's role in an incident is
usually different from QA's role in normal defect triage.

*(Note: this covers QA's role in incident communication/reporting
specifically. The deeper on-call/incident-response discipline —
runbooks, escalation, postmortems as an SRE practice — lives in the
[Observability & Monitoring repo](https://github.com/abhibatsa/architecting-software),
consistent with this repo's [scope](../start-here/scope.md).)*

## QA's actual role during an incident

- **Rapid reproduction** — confirming the issue, understanding scope
  (which users, which environments, which flows), often faster than a
  developer can because QA already knows the system's test coverage and
  edge cases
- **Regression risk assessment** — if a hotfix is being considered, QA's
  fast judgment on "what else could this touch" matters more in the
  moment than a full regression suite run, which there usually isn't
  time for
- **Verification of the fix** — same retest discipline as any defect,
  compressed into incident timescales

## What a good incident report captures, after the fact

- **Timeline** — when it started, when it was detected, when it was
  resolved (these are often three different, informative numbers)
- **Impact** — who/what was affected, and how severely
- **Root cause** — the actual technical cause, not just the symptom
- **How it reached production** — this is the question that actually
  prevents recurrence; "we fixed the bug" without "here's the process
  gap that let it ship" misses the more valuable lesson
- **Action items with owners** — a postmortem without assigned follow-up
  is a document nobody acts on

## The blameless framing that actually works

Incident reports that focus on "who missed this" instead of "what
process gap allowed this" produce worse outcomes — people become
defensive and start hiding near-misses instead of reporting them. The
goal is a system that catches the *next* version of this problem, not
finding who to blame for this one.

## Best Practices

- Capture the timeline in real time during the incident, not
  reconstructed from memory afterward — memory of exact timing degrades
  fast once the pressure is off
- Keep the incident report blameless in language and framing — "the
  deployment process lacked a check for X" not "engineer Y forgot to check X"
- Actually follow up on action items — an incident report whose action
  items are never revisited teaches the org that postmortems don't matter

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [Defect & Test Management](./README.md)*
