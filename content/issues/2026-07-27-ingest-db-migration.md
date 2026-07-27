---
title: Ingest database migration
date: 2026-07-27 13:45:00
resolved: true
resolvedWhen: 2026-07-27 15:10:00
severity: notice
affected:
  - API
  - Import
  - Website
section: issue
---

**Complete.** The ingest database has been moved to a new cluster. Submissions
are being accepted and processed normally and the queue is clear.

Submissions made during the maintenance window were queued rather than
processed, and have since all been processed — if you submitted fingerprints
this afternoon and they did not appear straight away, they are indexed now.
Nothing was lost.

**One brief interruption, at 14:53 UTC**, affected about eight requests across
the API and the website while the database was restarted. Service was restored
within a minute.
