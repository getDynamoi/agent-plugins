---
name: dynamoi-campaign-review
description: Review a Dynamoi artist's music-promotion campaigns, performance, and platform connection health. Use when the user asks how campaigns are doing, what is live, why a campaign is not ready, or whether Spotify, Meta, or YouTube are connected.
---

# Dynamoi campaign review

1. **Account.** Call `dynamoi_get_account_overview` for account state and recommended next actions.
2. **Campaigns.** Call `dynamoi_list_artists`, then `dynamoi_list_campaigns` with explicit type and status filters.
3. **Details and analytics.**
   - `dynamoi_get_campaign` gives one campaign's details.
   - `dynamoi_get_artist_analytics` gives artist-level results for a date range. If the user gave no range, use the last 30 days and say so.
4. **Connections.** Call `dynamoi_get_platform_status` for Spotify, Meta, and YouTube connection health and setup blockers.
5. **Summarize** in plain language: what is live, what changed, and the next step. Report only the numbers the tools return. Don't estimate or extrapolate.

Launching a paid campaign, changing a budget or live campaign, and billing are separate actions that need confirmation. If this client has those tools, describe the exact change and wait for the user's explicit confirmation before calling the tool. If it doesn't, say: "You can do this in the Dynamoi dashboard at https://dynamoi.com/dashboard."
