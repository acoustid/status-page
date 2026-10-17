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

Some requests are slow and a few time out, affecting roughly one request in
seven. A retry normally succeeds.

Lookups that complete return correct results. Submissions are unaffected.

**Update, 11:05 UTC.** The machine responsible is out of the rotation. Requests
already in flight to it may still be slow for a short while.
