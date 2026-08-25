# Daily/Weekly/Monthly Status Reporting

**Read time:** 3 min

---

Three different cadences, three different jobs. Using the wrong cadence
for the wrong audience is a common, avoidable communication failure —
covered briefly in
[Test Execution & Status Reporting](../qa-fundamentals/test-execution-and-status-reporting.md);
this doc goes deeper specifically on cadence structure.

## Daily — team-internal, tactical

**Job:** unblock today's work. Format: brief, spoken or async
(standup, Slack update) — what got tested yesterday, what's blocked,
what's planned today. Not a document anyone outside the immediate team
needs to read.

## Weekly — cross-team, trend-focused

**Job:** keep stakeholders who aren't in the daily details informed of
direction and risk. Format: a short written summary — % complete against
plan, defect trend (not raw count), key risks, anything needing a
decision from someone outside QA. This is where the
[defect trend](./qa-project-management.md) becomes the headline metric,
not a footnote.

## Monthly/Milestone — leadership, outcome-focused

**Job:** answer "are we on track for the bigger picture," not "what
happened this week." Format: high-level — release readiness against exit
criteria, quality trend across the longer arc of the project, any
escalations that need leadership-level decisions. Process detail that
matters daily is noise at this level.

## The structural mistake to avoid

Writing one report and sending the same version to all three audiences.
It technically saves time once, and costs more time repeatedly — the
daily-detail version overwhelms leadership with noise they'll ignore
(training them to skim or skip future reports), and the leadership-
summary version starves the team of the specific blocker information
they actually need day to day.

## Best Practices

- Write each cadence's report for its actual audience's decision-making
  needs, not as a copy-paste of another cadence's report
- Keep the weekly report's headline metric consistent week over week
  (same defect-trend framing, same %-complete calculation) so trend
  comparisons are actually valid, not apples-to-oranges
- Escalate outside the normal cadence when something genuinely can't
  wait for the next scheduled report — cadence discipline doesn't mean
  rigid silence between reports when a real risk emerges

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [Defect & Test Management](./README.md)*
