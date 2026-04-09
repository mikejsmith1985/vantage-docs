---
title: Setup Guide — Vantage for Jira
layout: default
---

# Setup Guide

This guide walks you through installing Vantage and connecting your first Jira project and (optionally) ServiceNow instance.

**Estimated time:** 5–10 minutes for basic setup. ServiceNow integration adds ~5 minutes.

---

## Step 1: Install Vantage

1. Go to the [Vantage listing on the Atlassian Marketplace](#)
2. Click **Get it now** and follow Atlassian's standard app installation flow
3. Select your Jira Cloud site when prompted
4. Accept the requested permissions (read/write Jira issues, read boards and sprints)

Once installed, Vantage appears as a **Project Page** inside any Jira project.

---

## Step 2: Open Vantage

1. Navigate to any Jira project
2. In the left sidebar, scroll down to **Project pages**
3. Click **Vantage** — the app loads inside the Jira interface

On first launch, Vantage detects that no board is configured and automatically opens the **Settings** tab.

---

## Step 3: Configure Your First Board

In the **Settings** tab:

1. **Select your Jira project** from the project dropdown
2. **Select your board** — Vantage lists all boards associated with the selected project
3. **Choose your persona** — this determines which views appear prominently:
   - *Developer* — Sprint Dashboard + My Issues
   - *Scrum Master* — DSU Board + Sprint Dashboard
   - *Product Owner* — Sprint Dashboard + Story Pointing
   - *Release Train Engineer (RTE)* — ART View + Sprint Dashboard
4. Click **Save Settings**

Vantage reloads and the Sprint Dashboard populates with your active sprint data.

---

## Step 4: Configure Story Pointing *(optional)*

In Settings → **Story Pointing**:

1. **Story Points Field** — pick the field your team uses for estimates (usually "Story Points" or "Story point estimate")
2. **Pointing Scale** — choose Fibonacci, Modified Fibonacci, T-Shirt Sizes, or Custom
3. **Acceptance Criteria Field** — if your team writes AC in a custom Jira field, pick it here so it shows on the pointing card

---

## Step 5: Connect ServiceNow *(optional)*

In the **ServiceNow Hub** tab:

1. Enter your **ServiceNow Instance URL** (e.g., `https://dev12345.service-now.com`)
2. Enter your **ServiceNow Username** and **Password**

   > **Security note:** These credentials are stored using Forge Secret Storage — they are encrypted at rest and never leave Atlassian's infrastructure unencrypted.

3. Click **Save Credentials** — Vantage tests the connection immediately
4. If the connection succeeds, the Incidents and Problem Records tables populate

### Linking SNow Issues to Jira

In the ServiceNow Hub, each incident row has a **🔗 Link to Jira** button. Click it and enter the Jira issue key (e.g., `PROJ-123`). Once linked:
- The Jira key appears as a clickable link
- When the linked Jira issue transitions status, Vantage automatically updates the ServiceNow record via the **Workflow Mapping** rules

---

## Step 6: Configure the ART View *(SAFe teams)*

In the **ART View** tab, click **Set Up Your ART**:

1. **Name your ART** — e.g., "Phoenix ART"
2. **Add teams** — select the Jira boards for each team in your ART
3. **Choose issue types** — pick which Jira issue type represents ART-level work (Feature, Epic, etc.) and which represents team-level work (Story, Task, etc.)
4. **Choose linkage strategy** — how team stories connect back to features:
   - *Parent field* — standard Jira parent/child relationship
   - *Epic Link* — via the Epic Link custom field
   - *Label* — stories tagged with the feature key as a label
   - *Custom Field* — any other Jira field
   - *Custom JQL* — advanced template query
5. **Save** — the Program Board populates automatically

---

## Step 7: Configure the Portfolio View *(multi-ART)*

In the **Portfolio** tab, click **Set Up Your Portfolio**:

1. **Name your portfolio**
2. **Add ARTs** — select from your configured ARTs
3. **Choose portfolio-level issue type** — Initiative, Epic, Theme, etc.
4. **Save** — the ART Health Cards and Initiative Tracker populate

---

## Troubleshooting

### "Board not configured" message
Go to **Settings** and select a board before using Sprint Dashboard or DSU Board.

### ServiceNow connection fails
- Verify the URL includes `https://` and has no trailing slash
- Confirm the username/password are for a ServiceNow user with Table API read access
- Check that your Forge app has egress permission for `*.service-now.com` (included by default)

### Story points show as "—" everywhere
The story points field is not configured. Go to **Settings → Story Pointing** and select your team's points field.

### ART Board shows no features
Check that your **Feature Project Keys** in the ART configuration match the Jira project(s) where features are stored.

---

## Getting Help

See the [Support page](support) for contact options and response time commitments.
