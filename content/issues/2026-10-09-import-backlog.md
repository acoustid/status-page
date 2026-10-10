---
title: Delayed processing of submitted fingerprints
date: 2026-10-09 07:30:00
resolved: false
severity: disrupted
affected:
  - Import
section: issue
---

Submitted fingerprints have been taking longer than usual to appear. Nothing
has been lost — every submission was queued and is being processed in order.

Submission volume rose sharply from 4 to 6 October, peaking at roughly 500,000
in a day against a normal 280,000, which built up a queue of around 618,000. We
have since increased the number of import workers, and the queue has been
draining steadily.

Progress:

- **20:25 UTC, 10 October** — about 18,000 remaining; new submissions are
  appearing within about 90 minutes.
- **08:50 UTC, 10 October** — about 436,000 remaining.
- **07:15 UTC, 9 October** — about 619,000 remaining, around two days behind.

Lookups, the API and the website were not affected at any point.
