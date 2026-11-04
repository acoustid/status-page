---
title: Errors on the website
date: 2026-11-04 19:40:00
resolved: true
resolvedWhen: 2026-11-04 20:20:00
severity: disrupted
affected:
  - Website
section: issue
---

**Resolved.** For about forty minutes, from roughly 19:40 to 20:20 UTC, a large
share of pages on the website returned an error instead of loading.

**The API was not affected.** Fingerprint lookups and submissions continued to
work normally throughout, so applications such as Picard were unaffected. This
was limited to browsing the website itself.

Affected pages failed outright rather than showing wrong information, so there is
nothing to re-check — anything that loaded was correct. Reloading now works.

No data was lost and nothing in the database was affected.

The cause was an internal limit on how many pages the website can look up at
once being reached, which made further requests fail until the load eased.
