---
title: Privacy Policy — Vantage for Jira
layout: default
---

# Privacy Policy

**Effective date:** April 8, 2026  
**Last updated:** April 8, 2026  
**App:** Vantage for Jira (Atlassian Forge)  
**Developer:** Mike Smith  
**Contact:** mikejsmith1985@yahoo.com

---

## 1. Overview

Vantage for Jira ("Vantage", "the app", "we") is an Atlassian Forge application that runs on Atlassian's infrastructure. This Privacy Policy explains what data Vantage accesses, how it is used, where it is stored, and your rights regarding that data.

By installing and using Vantage, you agree to this Privacy Policy.

---

## 2. Data We Access

### 2.1 Jira Data
Vantage accesses Jira data through the Atlassian Forge platform's secure API bridge. This includes:

- **Issue data** — issue keys, summaries, descriptions, statuses, priorities, assignees, labels, story points, comments, and worklogs — for display in Sprint Dashboard, DSU Board, My Issues, Story Pointing, ART View, and Portfolio View
- **Board and sprint data** — board names, sprint names, sprint dates, and sprint membership — for Sprint Dashboard and ART Board views
- **Project data** — project names and keys — for Settings configuration
- **User identity** — the authenticated user's Jira account ID and display name — for My Issues filtering and standup board grouping
- **Workflow data** — issue status names and categories — for Workflow Mapping configuration

Vantage **writes** the following Jira data on behalf of the authenticated user:
- Comments posted via the My Issues or DSU Board action panels
- Work log entries posted via the My Issues Log Time feature
- Issue field updates (status transitions, priority, assignee, labels, story points) made via My Issues or DSU Board inline edit

All Jira data access uses Atlassian's `asUser()` API — actions are performed as the authenticated Jira user, not as an app service account.

### 2.2 ServiceNow Data
If you configure the ServiceNow integration, Vantage accesses:

- **Incidents and Problem Records** — number, short description, description, state, priority, assignee, and Jira link field — for display in the ServiceNow Hub and My Issues tabs
- **Work notes** — written on your behalf when you use the "Add Comment" action in the ServiceNow Hub or My Issues

Vantage **writes** the following ServiceNow data:
- The Jira issue key field (`u_jira_issue_key`) on incident records when you use the "Link to Jira" feature
- Work notes appended when you submit a comment via My Issues or SNow Hub
- State and priority field updates made via My Issues or SNow Hub inline actions

---

## 3. How We Store Data

### 3.1 Configuration Data (Forge Storage)
The following configuration data is stored using **Forge Storage** (Atlassian-managed, encrypted in transit, stored within Atlassian's infrastructure):

- Vantage settings (active board ID, project key, persona, sprint cadence, timezone preferences)
- Story pointing configuration (field names and IDs, scale choice)
- ART and Portfolio configurations (team names, board IDs, issue type mappings)
- Workflow mapping rules
- User preferences (persona selection, recently visited views)

### 3.2 ServiceNow Credentials (Forge Secret Storage)
ServiceNow credentials (instance URL, username, and password) are stored exclusively using **Forge Secret Storage** — a separate, encrypted storage tier provided by Atlassian. Secret values:

- Are **encrypted at rest** using Atlassian's key management infrastructure
- Are **never readable** by Atlassian employees, the app developer, or any third party
- Are transmitted **only over HTTPS** from Forge backend functions to your ServiceNow instance
- Are **never sent to the browser** — all ServiceNow API calls originate from Forge serverless backend functions

### 3.3 Data We Do Not Store
Vantage does **not** store or retain:
- Issue content (summaries, descriptions, comments) beyond the current request lifecycle
- Sprint or board data beyond the current request lifecycle
- Any user-identifying information beyond the Jira account ID needed to filter "My Issues"
- Any data in external databases, cloud services, or servers outside Atlassian Forge infrastructure

---

## 4. Data Sharing

Vantage does **not** sell, rent, or share your data with any third parties.

The only external data flows are:
- **Atlassian Jira API** — to read and write Jira data on behalf of the authenticated user (via Forge's secure API bridge)
- **Your ServiceNow instance** — to read and write ServiceNow records using the credentials you provide (via HTTPS from Forge backend functions)
- **GitHub API** — if/when GitHub Dev Workspace features are enabled, to read pull request and deployment data (read-only)

All external API calls are made from **Forge backend functions only** — never from the user's browser.

---

## 5. Data Retention

- **Configuration data** is retained in Forge Storage until you either change it or uninstall the app
- **ServiceNow credentials** are retained in Forge Secret Storage until you clear them in Settings or uninstall the app
- **All app data** (configuration and secrets) is **permanently deleted** when you uninstall Vantage from your Jira site — Atlassian enforces this as part of the Forge platform's lifecycle management

---

## 6. Data Security

Vantage is built on Atlassian Forge, which provides:

- **Encryption in transit** — all communication between the app, Jira APIs, and ServiceNow uses HTTPS/TLS
- **Encryption at rest** — Forge Storage and Forge Secret Storage are encrypted at rest by Atlassian
- **Isolation** — each Forge app installation has isolated storage; data from one Jira site cannot access another site's data
- **No egress from the browser** — all ServiceNow and GitHub API calls are made from Forge backend functions; credentials are never exposed to the browser runtime
- **Least-privilege API scopes** — Vantage requests only the minimum Jira permission scopes needed (read/write issues, read boards and sprints, read projects)

---

## 7. Your Rights

As a user or administrator of Vantage, you have the right to:

- **Access** — request a summary of what configuration data is stored for your installation
- **Rectification** — update or correct your configuration data at any time via the Settings tab
- **Erasure** — uninstalling Vantage permanently deletes all associated data from Forge Storage and Secret Storage
- **Portability** — your configuration data is stored in a structured format; contact us to request an export

To exercise these rights, contact us at: **mikejsmith1985@yahoo.com**

---

## 8. Children's Privacy

Vantage is a professional B2B application designed for use in enterprise Jira environments. It is not directed at or intended for use by individuals under the age of 16. We do not knowingly collect personal data from minors.

---

## 9. Changes to This Policy

We may update this Privacy Policy to reflect changes in Vantage's functionality or applicable law. When we do:
- The "Last updated" date at the top of this page will change
- Significant changes will be noted in the [Vantage CHANGELOG](https://github.com/mikejsmith1985/Vantage/blob/main/CHANGELOG.md)

Continued use of Vantage after a policy update constitutes acceptance of the revised policy.

---

## 10. Contact

For privacy questions, data requests, or concerns:

**Email:** mikejsmith1985@yahoo.com  
**GitHub:** [github.com/mikejsmith1985/Vantage](https://github.com/mikejsmith1985/Vantage)  
**Marketplace listing:** [Atlassian Marketplace — Vantage](#)

Response time: within 5 business days for privacy-related enquiries.
