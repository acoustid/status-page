---
title: Public data file downloads were offline
date: 2026-10-17 11:05:00
resolved: true
resolvedWhen: 2026-10-18 12:00:00
severity: down
affected:
  - Data export
section: issue
---

**Resolved.** The public data files at data.acoustid.org are available again and
downloading at normal speed.

No data was lost and every file is complete.

Downloads returned an error from about 11:05 UTC on 17 October until about
12:00 UTC on 18 October. Scheduled jobs that fetch these files would have
failed during that window; the files they missed are all present now.
