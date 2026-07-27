---
title: Ingest database migration
date: 2026-07-27 13:45:00
resolved: false
severity: notice
affected:
  - API
  - Import
  - Website
section: issue
---

**As of 14:55 UTC:** the migration is complete and everything is running
normally again. Submissions are being accepted and processed, and the queue is
clear.

**A brief interruption at 14:53 UTC** affected a small number of requests — about
eight, across the API and the website — while the database was restarted as part
of the maintenance. Service was restored within a minute. Anyone who saw an
error at that moment can simply retry.

A small number of submissions queued at the moment of the switchover are still
to be transferred from the old database. They will be processed shortly, so the
queued count may move briefly again. Nothing is lost.
