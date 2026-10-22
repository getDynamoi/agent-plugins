---
name: dynamoi-distribution
description: Check an artist's eligibility for Dynamoi music distribution and, only with explicit confirmation, submit an application for manual review. Use when the user asks about distributing music through Dynamoi or about distribution requirements.
---

# Dynamoi distribution applications

Distribution is optional. Campaigns, Smart Links and analytics work with any distributor, so never suggest the artist must switch. Below the bar, report progress against each requirement and mention that Smart Campaigns can build listeners, without promising when or whether the bar is reached.

1. Resolve the artist with `dynamoi_list_artists`.
2. Call `dynamoi_get_distribution_application`. Report each of the five requirements with its current evidence and threshold exactly as returned, plus any existing application status.
3. Eligibility means the artist can apply. It does not guarantee approval.
4. Call `dynamoi_apply_for_distribution` only when both of these are true:
   - The user has explicitly confirmed they want to apply.
   - The user has supplied every required field: the applicant, tax-residency, and payout countries, plus the adult-signer attestation. Never infer these fields.
5. After submitting, explain that the application goes to manual review. Submitting does not approve distribution, accept an agreement, submit releases, or deliver music to stores.
