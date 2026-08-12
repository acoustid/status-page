---
title: Lookup errors
date: 2026-08-11 22:15:00
resolved: true
resolvedWhen: 2026-08-11 22:21:00
severity: disrupted
affected:
  - API
section: issue
---

Fingerprint lookups returned errors for about five minutes late on 11 August.
Submissions were affected to a much smaller degree over the same window.

The service recovered on its own and lookups have been working normally since
22:21 UTC. Affected requests failed outright rather than returning a wrong
answer, so they can simply be retried. No data was lost.
