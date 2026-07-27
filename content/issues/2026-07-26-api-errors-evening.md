---
title: Brief burst of API errors during database maintenance
date: 2026-07-26 18:24:00
resolved: true
resolvedWhen: 2026-07-26 18:26:00
severity: disrupted
affected:
  - API
section: issue
---

A brief burst of API requests failed during planned database maintenance,
lasting under a minute. No data was lost — affected requests failed outright and
could be retried.
