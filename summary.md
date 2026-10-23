# Checkout API v2 Migration — Design Review Digest

Source: `gateway_migration_review.docx` (Draft 3, design review copy). Margin notes were stripped by the document pipeline, so the document's "Reviewer comment log" section is the source of truth for this digest.

## Priority breakdown

| Metric | Value |
| --- | --- |
| Reviewers | 3 |
| Comments | 6 |
| High priority | 3 |
| Medium priority | 2 |
| Low priority | 1 |

## Comments and actions

One line per comment: author, priority, the part of the plan it targets, and the action to take.

1. **Dana Kim** — *High* — **Traffic ramp** — Hold the 5% ramp for four weeks (one full billing cycle) before raising exposure any further. → *Action:* Extend stage 2 from two weeks to four weeks so the 5% exposure window covers a full billing cycle before any further ramp.
2. **Dana Kim** — *Medium* — **Rollback plan** — Document the v1-to-v2 data mapping in the runbook. → *Action:* Add a v1-to-v2 data mapping section to the rollback runbook.
3. **Marco Reyes** — *High* — **Rollback plan** — Rehearse the v1 rollback in staging before the 50% ramp. → *Action:* Schedule and complete a v1 rollback rehearsal in staging and make it a blocking gate before stage 3.
4. **Marco Reyes** — *Medium* — **Monitoring** — Add a latency SLO dashboard tile for the v2 endpoint. → *Action:* Add a latency SLO tile for the v2 endpoint to the monitoring dashboards.
5. **Priya Nair** — *High* — **Monitoring** — Wire an error-budget alert to PagerDuty before traffic goes past 5%. → *Action:* Configure an error-budget alert routed to PagerDuty and verify it fires before stage 2 traffic ramps up.
6. **Priya Nair** — *Low* — **Known gaps** — Note the partner-API deprecation date in the customer FAQ. → *Action:* Add the partner-API deprecation date to the customer FAQ as part of the known-gaps cleanup.

## Playwright latest release (e2e suite tracking)

Latest release of `microsoft/playwright` as shown on GitHub: **v1.64.1** (published 2026-10-14).
https://github.com/microsoft/playwright/releases/tag/v1.64.1
