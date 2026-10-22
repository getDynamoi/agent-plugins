---
name: dynamoi-smart-links
description: Create, inspect, and update free Dynamoi Smart Links for a Spotify release or artist. Use when the user wants a shareable pre-save or release link, an artist link hub, Smart Link analytics, or a Smart Link theme change.
---

# Dynamoi Smart Links

Smart Links are free public landing pages on play.dynamoi.com. There is no per-link charge and no subscription gate.

1. **Identify the artist.** Call `dynamoi_list_artists` (or `dynamoi_search`) unless the user already named an artist Dynamoi returned earlier.
2. **Create a link.**
   - For a Spotify track or album URL, use `dynamoi_create_smart_link_from_spotify`. The call is idempotent: if the link already exists, return the existing public URL and say it already existed.
   - For a Spotify artist URL, use `dynamoi_create_smart_links_from_spotify_artist`. It builds an artist hub and imports the catalog in the background.
   - Playlist URLs are not supported. Say so rather than retrying.
3. **Inspect.** Call `dynamoi_list_smart_links`, then `dynamoi_get_smart_link`. Set `includeAnalytics` or `includeArtistSettings` only when the user asks for them.
4. **Update.** Call `dynamoi_update_smart_link` only for the specific change the user asked for: description, theme, or pixel settings.
   - Themes: Classic, Brutalist, Aurora, Cinematic.
   - `dynamoi_preview_smart_link_themes` shows the themes without changing anything.
5. **Always return the public Smart Link URL.** Don't expose internal workflow or record identifiers.
