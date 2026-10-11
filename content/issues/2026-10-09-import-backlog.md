---
title: Delayed processing of submitted fingerprints
date: 2026-10-09 07:30:00
resolved: true
resolvedWhen: 2026-10-11 14:30:00
severity: disrupted
affected:
  - Import
section: issue
---

**Resolved.** The queue is empty and submitted fingerprints are again being
processed within minutes. Nothing was lost — every submission was queued and
has been processed.

Submission volume rose sharply from 4 to 6 October, peaking at roughly 500,000
in a day against a normal 280,000, which built up a queue of around 619,000 and
left new submissions taking about two days to appear. We increased the number of
import workers and the queue drained steadily from there.

Progress during the incident:

- **14:30 UTC, 11 October** — queue empty, back to normal.
- **20:25 UTC, 10 October** — about 18,000 remaining; around 90 minutes behind.
- **08:50 UTC, 10 October** — about 436,000 remaining.
- **07:15 UTC, 9 October** — about 619,000 remaining, around two days behind.

Lookups, the API and the website were not affected at any point.
