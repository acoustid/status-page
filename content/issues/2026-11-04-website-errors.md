---
title: Intermittent errors on the website
date: 2026-11-04 19:40:00
resolved: true
resolvedWhen: 2026-11-06 04:45:00
severity: disrupted
affected:
  - Website
section: issue
---

**Resolved.** The website has been loading normally since about 05:00 UTC on
6 November. No data was lost and nothing in the database was affected.

**The API was never affected.** Fingerprint lookups and submissions worked
normally throughout, so applications such as Picard were unaffected at every
point during this. It was limited to browsing the website itself.

The cause was automated scraping by an AI crawler. One of our pages compares two
fingerprints against each other, and because any two fingerprints can be
compared there is a practically unlimited number of those pages. A crawler
worked its way through them, which added up to millions of requests for pages
that nobody actually reads, and more than a terabyte of traffic over the past
month.

Each of those pages has to query the database, and there is a limit on how many
such queries the website can have in flight at once. The crawler used the limit
up, so ordinary page loads had nothing left to use and failed instead. That is
why it came and went in episodes, and why it was worst in the early hours of the
morning when the crawling was heaviest.

Fingerprint comparison pages are now blocked from automated access, so this
traffic cannot build up the same way again. The pages still work normally for
people browsing the site.

Pages failed outright rather than showing wrong information, so there is nothing
to re-check — anything that loaded was correct.

Progress:

- **11:30 UTC, 6 November** — errors stopped at about 04:45 UTC and the site
  has been clear since. The cause has been identified as AI crawler traffic and
  the affected pages are now protected against it.
- **11:00 UTC, 6 November** — errors returned for several hours overnight, from
  about 01:00 to 05:00 UTC, affecting up to roughly one in seven page loads at
  the worst point. The API was unaffected throughout.
- **12:00 UTC, 5 November** — errors returned for about an hour during the
  morning, affecting a small share of page loads — far less than overnight — and
  have cleared again. Traffic is now several times higher than it was overnight
  and the site is keeping up.
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
