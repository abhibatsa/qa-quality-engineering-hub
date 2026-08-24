# The QA/QE Career Landscape

Four related but genuinely distinct roles get conflated constantly. Here's
the map, and where to go deeper on each.

## The four roles, plainly

**Manual/Functional QA Tester** — executes test cases, finds and reports
defects, thinks in user flows and edge cases. The foundation every other
role builds on, not a "lesser" version of SDET.

**SDET / Automation Engineer** — writes code to automate testing:
frameworks, CI/CD integration, scaling coverage beyond what manual
execution can reach. Adds software engineering skill on top of QA
judgment, doesn't replace it.

**Quality Engineer (QE) / Quality Manager** — owns quality *strategy*
across a team or org: process design, tooling decisions, metrics,
stakeholder communication, sometimes people management. Less
hands-on-keyboard, more "how do we make quality a system, not a phase."

**AI Test Engineer** — the newest role: testing systems where correctness
isn't a fixed expected value (LLMs, agents, recommendation systems).
Requires SDET-level technical skill plus a genuinely different evaluation
mindset — see [`ai-in-qa/ai-qa-fundamentals.md`](../ai-in-qa/ai-qa-fundamentals.md)
for why this is a distinct skill, not just "SDET plus AI."

## How they relate

```
Manual Tester
   ↓ (adds automation/coding skill)
SDET / Automation Engineer ──────→ Quality Engineer / Quality Manager
   ↓ (adds AI/ML evaluation skill)      (adds strategy, process, people)
AI Test Engineer
```

Not a strict ladder — QE and AI Test Engineer are both legitimate
next steps from SDET, depending on whether you want to go deeper
technical (AI Test Engineer) or broader/strategic (QE). Neither is a
"higher" role than the other; they're different directions.

## Where to go deeper on each

- **This repo** is the shared reference layer underneath all four roles —
  process fundamentals, tooling, and AI-QA concepts apply regardless of
  which direction you're headed
- **Manual → SDET transition and SDET career prep, interview-ready:**
  [SDET / Automation Career Prep](https://github.com/abhibatsa/sdet-automation-career-prep)
- **AI Test Engineer transition and career prep:**
  [AI Test Engineering Career Prep](https://github.com/abhibatsa/ai-test-engineering-career-prep) *(private)*
- **QE/Quality Manager career progression** isn't yet a dedicated repo in
  this family — for now, the [Defect & Test Management](../defect-management)
  and [QA Project Management Fundamentals](../defect-management/qa-project-management.md)
  sections here are the closest coverage

## A note on titles

Titles vary wildly by company — some call every one of these four roles
"QA Engineer." Don't over-index on the exact title in a job posting; read
the actual responsibilities listed and map them against the four roles
above to understand what you're actually being asked to do.

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md)*
