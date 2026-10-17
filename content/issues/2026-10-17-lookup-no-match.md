---
title: Some lookups incorrectly returned no match
date: 2026-10-17 07:10:00
resolved: true
resolvedWhen: 2026-10-17 07:31:00
severity: disrupted
affected:
  - API
  - Website
section: issue
---

**Resolved.** Between roughly 07:10 and 07:31 UTC, about **one in four**
fingerprint lookups returned "no match" for recordings that are in fact in the
database, and some requests returned errors. Submissions were slow to be
accepted during the same window.

**Nothing has been lost.** No submitted fingerprints or metadata were dropped,
and the database is intact. The incorrect answers were served to lookups only.

**If you were looking up fingerprints during that window, results you received
may be wrong.** A "no match" answer returned between 07:10 and 07:31 UTC is not
reliable — at roughly one in four, it is worth re-checking anything you cached
or stored from that period rather than assuming it was a genuine miss. Lookups
that returned a match were correct, and lookups made since 07:31 are correct.

Unaffected: any lookups outside that window.

One of the machines serving the database fell behind, which slowed writes across
most of the service. The component that matches fingerprints answered "no match"
rather than returning an error when it could not reach the data it needed.

**Update, 10:00 UTC.** The cause was a network fault on that machine, which cut
its throughput to a fraction of normal. It is out of service. Lookups and
submissions are working normally.

The public data file downloads are also affected and are tracked separately.
