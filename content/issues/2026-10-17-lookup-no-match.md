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

Unaffected: the public data files at data.acoustid.org, and any lookups outside
that window.

One of the machines serving the database fell behind in a way that slowed
writes across most of the service, and the component that matches fingerprints
answered "no match" rather than reporting an error when it could not reach the
data it needed. That machine has been taken out of service and the remaining
capacity is handling traffic normally. We are still investigating why it
degraded.

**Update, 10:00 UTC.** We have found the cause. A network fault on that machine
had cut its data throughput to a tiny fraction of normal while leaving it
looking healthy to our automated checks, so it kept being given work it could
not carry. It stays out of service until the fault is fixed, and we have removed
the remaining pieces of the service that were still relying on it. Lookups and
submissions are working normally.
