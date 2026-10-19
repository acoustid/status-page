---
title: Website and API briefly unavailable
date: 2026-10-19 22:15:00
resolved: true
resolvedWhen: 2026-10-19 22:25:00
severity: down
affected:
  - API
  - Website
section: issue
---

**Resolved.** For roughly ten minutes, from about 22:15 to 22:25 UTC, the
website and the API returned errors.

Requests during that window failed outright. They did not return wrong answers,
so there is nothing to re-check: anything that got a response before or after
the window was correct.

No data was lost. Submissions are accepted and processed normally again, and
nothing in the database was affected.

The cause was a failure on one of the machines running the service. The database
moved to another machine automatically, which restored service.

Public data file downloads at data.acoustid.org were unaffected throughout.
