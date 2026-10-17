---
title: Some requests are slow
date: 2026-10-17 10:50:00
resolved: false
severity: disrupted
affected:
  - API
  - Website
section: issue
---

One of the machines that serves traffic is running at a small fraction of its
normal network speed. Requests that landed on it were slow and a few timed out.
Roughly one request in seven was affected, and a retry would usually be served
by a different machine and succeed normally.

**Answers are correct and nothing has been lost.** This is slowness, not wrong
results. Lookups that complete are returning accurate answers, and submissions
are being accepted and processed normally.

**Update, 11:05 UTC.** That machine has been taken out of the rotation, so new
requests are no longer being sent to it. Requests already in flight to it may
still be slow for a short while as they finish. We are leaving this open until
we have confirmed normal response times across the board.

The public data file downloads are affected separately and are tracked in their
own entry.
