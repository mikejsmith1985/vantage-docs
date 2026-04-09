---
title: Vantage for Jira
layout: default
---

# Vantage for Jira

**The all-in-one Agile program management panel — built directly into Jira Cloud.**

Vantage turns your Jira project page into a full command center for teams running Scrum, SAFe, or any Agile framework. No context-switching. No separate tools. Everything you need is one click away inside Jira.

[Install on Atlassian Marketplace](#){: .btn} &nbsp; [Setup Guide](setup-guide){: .btn .btn-secondary}

---

## What Vantage Does

### 🏃 Sprint Dashboard
Real-time sprint health at a glance — velocity, completion percentage, blockers, defect rate, and carryover items. Designed for Scrum Masters and Product Owners who need the full picture in under 30 seconds.

### 📋 Daily Standup Board (DSU)
A structured daily standup view organized by person or by workflow status. Click any issue row to update status, priority, assignee, or labels inline — no need to open the Jira issue. Click the issue key to jump to the full detail view.

### 🚂 ART View *(SAFe)*
Multi-team Program Board showing Feature progress across all Agile Release Train teams in the current sprint. Configurable issue hierarchy (Feature → Story, Epic → Story, or any custom mapping), flexible linkage strategies, optional Program Increment overlay, and cross-team blocker tracking. Built for RTEs.

### 📊 Portfolio View *(Executive)*
Roll up multiple ARTs into a single Director-level view. ART Health Cards with composite 0–100 health scores, Initiative progress bars with per-ART breakdowns, and aggregated portfolio metrics. Built for Directors and Senior Leadership.

### 📌 My Issues
All your assigned Jira issues *and* your ServiceNow incidents in one unified list. Add comments, update status, log time, adjust story points, and change priority — all from the same screen. Source tabs let you filter by Jira, ServiceNow, or view all.

### 🎯 Story Pointing
Guided pointing sessions with full issue detail (description, acceptance criteria, comments). Supports Sprint, Release, Backlog, or Custom JQL as the issue source. Configurable scale (Fibonacci, Modified Fibonacci, T-Shirt, or Custom). Configurable story points field and type.

### 🔗 ServiceNow Hub
Live view of your ServiceNow incidents and problem records, with direct Jira issue linking. Status and priority updates made directly from the hub. Bi-directional sync: when a linked Jira issue transitions, the ServiceNow record updates automatically.

### ⚙️ Workflow Mapping
Map your Jira workflow statuses to ServiceNow states at the issue-type level — without writing a single line of code. Granular per-status mapping, not just broad category buckets.

---

## Pricing

Vantage is listed as **Paid via Atlassian**.

- **Free** for Jira instances with 10 or fewer users (automatically applied by Atlassian)
- **Paid** plans for larger teams — see the [Atlassian Marketplace listing](#) for current pricing

Atlassian's 100% revenue share program means your purchase directly supports continued development of Vantage.

---

## Security

- All ServiceNow credentials (username, password) are stored using **Forge Secret Storage** — encrypted at rest, never visible to Atlassian employees or any third party
- All external API calls (to ServiceNow) are made exclusively from **Forge serverless backend functions** — your credentials are never sent through the browser
- Vantage is hosted entirely on **Atlassian Forge infrastructure** — no external servers to manage or trust
- Only the minimum Jira scopes required are requested (read/write issues, read boards/sprints)

---

## Requirements

- **Jira Cloud** (any plan — Free, Standard, Premium, or Enterprise)
- For ServiceNow Hub features: a reachable ServiceNow PDI or production instance
- No additional servers, databases, or infrastructure required
