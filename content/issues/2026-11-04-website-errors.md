---
title: Intermittent errors on the website
date: 2026-11-04 19:40:00
resolved: false
severity: disrupted
affected:
  - Website
section: issue
---

**Ongoing and getting worse.** Since about 19:40 UTC on 4 November the website
has been returning errors instead of loading pages. It began as separate
episodes with normal service in between, but has become much more frequent
overnight — around half of page loads are currently failing.

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
