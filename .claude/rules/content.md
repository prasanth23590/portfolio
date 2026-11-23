---
name: Portfolio Content Sources
description: Data sources, SAP Community blog URLs, stats used in the portfolio
type: project
---

SAP Community author login: **PrasanthPadmanabhan** (user-id/824)
Profile: https://community.sap.com/t5/user/viewprofilepage/user-id/824

Total: 19 blog posts, 141,429 combined views (as of Nov 2026, from the SAP Community API)

Top posts:
- Extensibility in SAP S/4HANA Cloud — 18,537 views (Sep 2022)
- Key User Extensibility: Custom Code List with CDS View — 13,625 views (Oct 2021)
- How to use REST API to post data into S/4HANA Cloud via SAP IRPA 2.0 — 13,488 views (Apr 2021)
- Release Assessment and Scope Dependency: 2024 Edition — 13,101 views (Apr 2024)
- Convert number to words in S/4HANA Cloud — 11,963 views (Jul 2020)
- Latest: Object Release State in Cloudification Repository Viewer (Mar 2026) — 3,655 views

To refresh: open the SAP Community profile in a normal browser (Cloudflare blocks headless/automated access), then in the DevTools console run a fetch to /api/2.0/search with the LiQL query
SELECT subject, view_href, post_time, metrics.views FROM messages WHERE author.id = '824' AND depth = 0 ORDER BY post_time DESC LIMIT 100

Claude Code insights (from /insights, captured May 2026):
- 68 sessions, 649 messages, 38 commits, 228 files, 26 active days
- Primary workflows: SAP Clean Core compliance reports, competitive analysis, skill ecosystem
- Power user pattern: delegates full multi-phase workflows, corrects iteratively

GitHub Pages URL: https://prasanth23590.github.io/portfolio/
Repo: https://github.com/prasanth23590/portfolio (github.com identity: prasanth23590)
