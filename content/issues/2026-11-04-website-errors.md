---
title: Intermittent errors on the website
date: 2026-11-04 19:40:00
resolved: false
severity: disrupted
affected:
  - Website
section: issue
---

**Ongoing, intermittent.** Since about 19:40 UTC on 4 November the website has
had repeated episodes, each lasting roughly twenty to forty minutes, where a
large share of pages return an error instead of loading. Between episodes the
site works normally.

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

- **23:00 UTC, 4 November** — the episodes are becoming more frequent and more
  severe: three in the last forty minutes, with up to about two in five page
  loads failing at the worst moments. The API remains unaffected.
- **22:00 UTC, 4 November** — quiet for the last half hour, but the problem has
  recurred several times this evening, so this is left open rather than marked
  resolved.
- **19:40 UTC, 4 November** — first episode begins.
