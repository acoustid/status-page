---
title: Some requests are slow, and data file downloads are capped
date: 2026-10-17 10:50:00
resolved: false
severity: disrupted
affected:
  - API
  - Website
section: issue
---

One of the machines that serves traffic is currently running at a small
fraction of its normal network speed. Requests that happen to land on it are
slow and a few may time out. Roughly one request in seven is affected, and a
retry will usually be served by a different machine and succeed normally.

**Answers are correct and nothing has been lost.** This is slowness, not wrong
results. Unlike the earlier incident today, lookups that complete are returning
accurate answers, and submissions are being accepted and processed normally.

**Downloads of the public data files are deliberately capped for now.** Those
files are served from the same machine, and we have limited them on purpose so
that the little available capacity goes to the API and the website instead.
Large files will be very slow to download until this is resolved. The files
themselves are complete and correct. We are moving these downloads to separate
hosting so they no longer compete with the service.

We are working on two things: restoring that machine's network speed, and
taking it out of rotation in the meantime so that requests stop being sent to
it at all.
