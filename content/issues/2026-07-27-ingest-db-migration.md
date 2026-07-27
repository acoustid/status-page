---
title: Ingest database migration
date: 2026-07-27 13:45:00
resolved: false
severity: notice
affected:
  - Import
section: issue
---

With the submission backlog nearly cleared, we are taking the opportunity to
move the ingest database to a new cluster.

New submissions are accepted and processed as usual. Anything still queued at
the moment of the switchover is copied across and reprocessed afterwards, so the
number of queued submissions may rise briefly before draining again. Nothing is
lost.

Lookups and the website are not affected.
