# YFSP-Bangumi

YFSP scraper module with Bangumi-assisted Chinese title and poster matching.

## Design

- Bangumi API is used only for anime subject search and metadata.
- YFSP remains authoritative for search-result playback URLs, details, episodes, stream signing and HLS playback.
- The original `yfsp/` module is not modified.
- Exact normalized title matching is required before replacing a title/poster. Ambiguous matches (for example, multiple seasons with the same title) are left unchanged.
- If Bangumi is unavailable, native YFSP search results are still returned.

## Install

Manifest:

`https://raw.githubusercontent.com/SakuraYuki56/Sora-Modules/feature/yfsp-bangumi/yfsp-bangumi/yfsp-bangumi.json`

## Scope and limitations

This is a separate Shirox-compatible source. It does not replace the AniList home page, global search provider, or AniList tracking. Chinese search is available when searching within this module.

## Validation status

The module follows the repository's global video-module contract and reuses the existing YFSP detail/episode/stream implementation. Live Shirox runtime validation is still required before removing the `needs_review` marker in `modules.json`.
