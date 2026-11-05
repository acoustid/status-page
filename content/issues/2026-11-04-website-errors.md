---
title: Intermittent errors on the website
date: 2026-11-04 19:40:00
resolved: false
severity: disrupted
affected:
  - Website
section: issue
---

**The website has been working normally since about 02:00 UTC on 5 November.**
This is being left open for now rather than marked resolved, because the
underlying cause has not yet been addressed and the quiet period so far covers
only the overnight hours, when traffic is lowest.

Between about 19:40 and 02:00 UTC the website returned errors instead of loading
pages — at first in separate episodes with normal service in between, then almost
continuously, with around half of page loads failing at the worst point.

**The API is not affected.** Fingerprint lookups and submissions have continued
to work normally throughout, so applications such as Picard are unaffected. This
is limited to browsing the website itself.

Affected pages fail outright rather than showing wrong information, so there is
nothing to re-check — anything that loaded was correct. If a page errors,
reloading it a little later usually works.

No data has been lost and nothing in the database is affected.

The cause is an internal limit on how many pages the website can look up at
once being reached, which makes further requests fail until the load eases. We
are working on raising that limit.

Progress:

- **06:00 UTC, 5 November** — no errors for the last four hours; the website is
  loading normally. Kept open until it has been through a busier part of the day,
  since the cause is not yet fixed.
- **02:00 UTC, 5 November** — substantially worse. Roughly half of all page
  loads failed over the last hour, up from about one in ten earlier in the
  evening, and the errors are now near-continuous rather than coming in
  separate episodes. The API is still completely unaffected.
- **23:00 UTC, 4 November** — the episodes are becoming more frequent and more
  severe: three in the last forty minutes, with up to about two in five page
  loads failing at the worst moments. The API remains unaffected.
- **22:00 UTC, 4 November** — quiet for the last half hour, but the problem has
  recurred several times this evening, so this is left open rather than marked
  resolved.
- **19:40 UTC, 4 November** — first episode begins.
