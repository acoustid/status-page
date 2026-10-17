---
title: Public data file downloads are offline
date: 2026-10-17 11:05:00
resolved: false
severity: down
affected:
  - Data export
section: issue
---

The public data files at data.acoustid.org are **temporarily offline on
purpose**. Requests to them currently return an error.

**Nothing has been lost and nothing is corrupted.** Every file is complete and
correct; they are simply not being served for the moment.

They are served from a machine whose network link is running far below its
normal speed. Serving large downloads from it was taking capacity away from the
API and the website, so we have stopped serving them until that is fixed —
better to have the lookup service healthy and the downloads briefly
unavailable than both degraded.

**We expect to restore downloads during 18 October.** We are also moving these
files to separate hosting so that they no longer share capacity with the
service, which means a problem like this should not take them down again.

If you have a job that fetches these files on a schedule, it will fail until
then; the files it missed will still be there afterwards.
