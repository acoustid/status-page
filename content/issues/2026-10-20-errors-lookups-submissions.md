---
title: Errors on lookups and submissions
date: 2026-10-20 06:40:00
resolved: true
resolvedWhen: 2026-10-20 07:20:00
severity: disrupted
affected:
  - API
  - Website
  - Import
section: issue
---

**Resolved.** Between about 06:40 and 07:20 UTC a portion of requests to the API
and the website returned errors. The heaviest few minutes were around 07:15.

Affected requests failed outright rather than returning wrong answers, so there
is nothing to re-check: anything that received a response was correct. Most
requests during the window still succeeded.

A small number of submissions failed with an error and were not saved. If you
sent a submission in that window and got an error back, please send it again.
Everything that was accepted is queued and is being processed normally.

No stored data was lost, and nothing already in the database was affected.
Backups continued and have been verified since.

The cause was a failure on one of the machines running the service, which for a
few minutes disrupted the internal lookups that let the different parts of the
service find each other. Databases moved to other machines automatically.
Service recovered once the affected machine was brought back.

Public data file downloads at data.acoustid.org were unaffected throughout.
