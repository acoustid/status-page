---
title: Delayed processing of submitted fingerprints
date: 2026-10-09 07:30:00
resolved: false
severity: disrupted
affected:
  - Import
section: issue
---

Submitted fingerprints are taking about two days to appear, instead of the
usual few minutes. Nothing has been lost — every submission is safely queued
and will be processed in order.

Submission volume rose sharply from 4 to 6 October, peaking at roughly 500,000
in a day against a normal 280,000, which built up a queue of around 618,000. We
have since increased the number of import workers, and the queue is now
draining at about three times the rate submissions arrive. We expect it to clear
during 10 October.

Lookups, the API and the website are unaffected.
