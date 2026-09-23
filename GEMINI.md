# Dynamoi

The `dynamoi` MCP server (https://dynamoi.com/mcp) connects this session to the user's Dynamoi account for music promotion. The first time you use it, run `/mcp auth dynamoi` and sign in to Dynamoi in the browser.

- **Getting started:** start account work with `dynamoi_get_account_overview`, then use the smallest tool that fits the request. Resolve artists with `dynamoi_list_artists` or `dynamoi_search` instead of guessing IDs.
- **Smart Links** are free.
  - For a Spotify track or album URL, use `dynamoi_create_smart_link_from_spotify`.
  - For a Spotify artist URL, use `dynamoi_create_smart_links_from_spotify_artist`.
  - Playlist URLs are not supported.
- **Paid campaigns:** managed advertising campaigns are a separate paid service. Before you launch a campaign, change a live campaign, or create a checkout, say exactly what will happen and wait for the user's explicit confirmation in this conversation.
- **Distribution:** check `dynamoi_get_distribution_application` first, and call `dynamoi_apply_for_distribution` only after explicit confirmation. Applying submits the application for manual review. It does not approve distribution or deliver music.
- **Missing permissions or connections:** if a tool reports one, relay the next step it returns. Anything not available here can be done in the Dynamoi dashboard at https://dynamoi.com/dashboard.
- **Accuracy:** never invent campaign results, budgets, or eligibility numbers. Report only what the tools return.
