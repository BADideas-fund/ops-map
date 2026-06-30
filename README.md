# BADideas Operations Map

Internal operations dashboard for **BADideas Fund** — a Latvian venture capital fund (AIFP licensed). This tool is used by the operations team to track, manage, and stay on top of all fund processes across seven operational areas.

> **Live app:** [badideas-fund.github.io/ops-map](https://badideas-fund.github.io/ops-map/)  
> **Access:** Password-protected (internal team only)

---

## What it does

The platform is a single-file HTML dashboard that covers the full operational lifecycle of the fund — from deal management and compliance to LP reporting and team administration. It serves as the team's central reference for who owns what, how well each process is mastered, and what deadlines are coming up.

### Four views

| View | Purpose |
|------|---------|
| **Dashboard** | High-level stats — op count, priority breakdown, upcoming deadlines, proficiency coverage, owner workload |
| **Visual Map** | Operational flow diagram showing how work moves between the 7 categories, with live data per card |
| **All Operations** | Full list of 83 operations with filters, search, proficiency tracking, and notes |
| **Compliance Calendar** | Timeline of all regulatory and reporting deadlines — list and month views |

---

## Operations coverage

83 operations across 7 categories:

- **Finance & Accounting** — monthly closing, budget files, drawdowns, annual reports, BIFI financials
- **LP Relations & Reporting** — quarterly LP report, alignment calls, management fee notices, investor queries
- **Investment Deals** — deal management, IC lineup, KYC/AML screening, SPV round management
- **Compliance & Regulatory** — CFLA, Latvijas Banka, AML policy, EU sanctions, annual reviews
- **Portfolio Monitoring** — KPI collection, valuations, CLA tracking, portfolio company reviews
- **Syndicate Operations** — SPV management, syndicate LP communications, IPEV valuations
- **Team & Admin** — standups, sprint tracking, travel, tooling

---

## Features

- **Proficiency tracking** per operation: Mastered / In progress / Started / Not started / Irrelevant
- **Priority levels**: High / Medium / Low — shown on every card and aggregated in the dashboard
- **Compliance Calendar** with 72+ dated events, urgency indicators, and `.ics` export
- **Cloud sync** via JSONBin — all settings, notes, and statuses sync across devices
- **Editable everything** — operation names, descriptions, frequencies, owners, and calendar entries can all be edited in-place
- **Personal notes** per operation — saved locally
- **Custom operations** — add your own beyond the built-in 83
- **Category filter + search** — instant filtering across all operations

---

## Tech

- Single `.html` file — no build step, no dependencies, no framework
- All data embedded inline (operations, calendar, categories)
- User state stored in `localStorage` key `badi_v2`
- Cloud sync to JSONBin.io (private bin, API key scoped to internal use)
- Password authentication via SHA-256 hash (Web Crypto API — no plaintext stored)
- Hosted via GitHub Pages from this repository

---

## Repository

This repository contains a single file: `index.html`. It is the entire application.

The repo is **public** (required for GitHub Pages hosting) but the application is password-protected. No sensitive data is stored in the HTML — all user state lives in the browser or the private JSONBin.

---

*BADideas Fund · Internal tool · Not for public use*
