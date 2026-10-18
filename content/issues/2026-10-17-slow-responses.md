---
title: Some requests were slow
date: 2026-10-17 10:50:00
resolved: true
resolvedWhen: 2026-10-18 12:00:00
severity: disrupted
affected:
  - API
  - Website
section: issue
---

**Resolved.** Some requests were slow and a few timed out, affecting roughly one
request in seven. A retry would normally succeed.

Lookups that completed returned correct results, and submissions were
unaffected throughout.

The cause was a network fault on one machine, which had cut its speed to a
fraction of normal. It was taken out of the rotation on 17 October at 11:05 UTC,
and on 18 October the fault was repaired and the machine returned to full speed.
