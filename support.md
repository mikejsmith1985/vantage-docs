---
title: Support — Vantage for Jira
layout: default
---

# Support

We're committed to helping you get the most out of Vantage.

---

## How to Get Help

### GitHub Issues *(Recommended)*
For bug reports, feature requests, and detailed technical questions:

**[Open an issue on GitHub](https://github.com/mikejsmith1985/Vantage/issues)**

When reporting a bug, please include:
- Your Jira Cloud plan (Free, Standard, Premium, Enterprise)
- Which Vantage feature you were using
- The error message or unexpected behavior
- Steps to reproduce (if known)

### Email Support
For account or billing questions, or if you prefer direct contact:

**mikejsmith1985@yahoo.com**

---

## Response Time

> **Support requests are addressed within 3–5 business days (Monday–Friday, UTC-6).**

Critical bugs (app fails to load, data loss) are prioritized and typically addressed within 1 business day.

---

## Frequently Asked Questions

**Q: Does Vantage store my Jira data on external servers?**  
A: No. Vantage runs entirely on Atlassian Forge infrastructure. Your Jira data is never sent to third-party servers. ServiceNow API calls are made directly from Forge's secure backend functions.

**Q: Are my ServiceNow credentials safe?**  
A: Yes. ServiceNow credentials are stored using Forge's encrypted Secret Storage, which is separate from regular app storage. Even Atlassian employees cannot read these values.

**Q: Can I use Vantage with Jira Data Center or Server?**  
A: Vantage is a Forge app designed exclusively for **Jira Cloud**. It does not support Jira Data Center or Server.

**Q: What happens to my data if I uninstall Vantage?**  
A: All Vantage configuration (settings, ART configs, credential secrets) is automatically deleted from Forge Storage when you uninstall the app. No data is retained after uninstallation.

**Q: Can I use Vantage with multiple Jira projects?**  
A: Yes. The ART View and Portfolio View are designed for multi-project setups. The Sprint Dashboard and DSU Board are configured per-project in Settings.

**Q: I get a "ServiceNow connection failed" error. What do I do?**  
A: Check that:
1. Your ServiceNow URL is correct (e.g., `https://dev12345.service-now.com`)
2. The user account has Table API read access in ServiceNow
3. The Forge app has egress permission for `*.service-now.com` — this is enabled by default

**Q: Is there a free version?**  
A: Vantage is automatically free for Jira instances with **10 or fewer users** (applied by Atlassian). Larger teams are on the paid plan — see the Marketplace listing for pricing.

---

## Feature Requests

Have an idea for Vantage? [Open a GitHub issue](https://github.com/mikejsmith1985/Vantage/issues/new?labels=enhancement&template=feature_request.md) with the `enhancement` label. We review all feature requests and prioritize based on community votes.

---

## Known Limitations

- Story Pointing sessions support up to 50 issues per session. Remaining issues carry to the next session.
- The ART Program Board with "Custom JQL" linkage strategy supports up to 20 features per board (to avoid Jira API rate limits).
- ServiceNow sync currently supports Incidents and Problem Records. Change Request sync is planned for a future release.
