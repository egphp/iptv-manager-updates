# IPTV Manager Feature Inventory

Generated for the public documentation refresh on 2026-04-29.

This inventory is based on the IPTV Manager source tree around `v3.5.599` plus the active local documentation/screenshot review. Items marked **Released** are part of the current public v3.5 line. Items marked **Local pending** were visible in the local working tree during the documentation pass and should not be treated as installed on clients until published in a later release.

## Product Surface

| Area | Status | What Exists |
|---|---|---|
| Dashboard | Released | Section tabs, status tabs, movie/series grid, cards, posters, ratings, counts, filters, search, live toolbar |
| Decisions | Released | Accept, reject, force accept, reject group, watched+removed, chosen variants, custom episode ranges |
| Sections | Released | Add/edit/delete sections, enable toggle, IPTV category sources, scan section, source labels, disk usage |
| Filtering | Released | Global and per-section country/genre/language exclusions, banned keywords, pre-rejected keywords, min year/rating/votes |
| Metadata | Released | TMDB, OMDb, IMDb IDs, ratings, vote counts, posters, cast, plot, release dates, cover upgrades |
| Downloads | Released | aria2c queueing, resume, manual start/stop/kill, daily/monthly limits, speed restart, bandwidth accounting |
| Local playback | Released | Browser playback, local/proxy/remux/transcode tiers, cache guardrails, watch progress endpoints |
| Plex Connect | Released | Local Plex connection, libraries, users, watch activity, section interest, reclaim safety panel |
| Future schedules | Local pending | Accepted card future badges, VOD future rows, S-Watchlist future filter, weekly schedule refresh |
| Disk discovery | Released | Scan local media, link external files, merge discovered media, ignore list, safe duplicate repair |
| Gone inbox | Released | Detect provider entries gone from IPTV, swap replacement, delete-to-trash, ignore |
| Integrity | Released | Detect-only integrity issues, resume partials, active/progress endpoints, dashboard actions |
| Trash | Released | Safe move-to-trash, restore, permanent delete, metadata preservation, cover repair helpers |
| Search | Released | Global search, suggestions, trending, preview, continue watching, IPTV search refresh |
| Actors/trailers/social | Released | Actor search/media/photo, trailer cache, social feed/badge/push dedupe |
| Connected devices | Released | Telemetry, device aliases, versions, health, disconnected thresholds, WS command relay, SSH repair tools |
| Updates/publish | Released | GitHub release update packages, support channels, mirror upload, runtime/toolchain manifests |
| Themes/PWA | Released | Light/dark/auto themes, holiday themes, PWA manifest, service worker, push notifications, install CA |

## Source Tree Map

The application source is in the private/main development repo, while this public repo hosts release assets and documentation. The source tree inspected during this pass contained more than 1,000 tracked files plus generated assets.

| Path | Role |
|---|---|
| `series_manager_web.py` | Flask/Cheroot entry point, static asset serving, remote login compatibility |
| `web/` | Application package: constants, runtime helpers, recurring tasks, diagnostics, Plex tracking, route modules |
| `web/routes/` | Blueprint APIs for series, settings, system, update, PWA, live, remote, discovery, trash, repair, actors, social |
| `admin/routes/` | Admin-only publish/export/update support surfaces excluded from client runtime packages |
| `db/` | SQLite schema, migrations, config_store helpers, media/decisions/sections/trash/download/watch queries |
| `sync/` | IPTV fetch, category handling, metadata enrichment, OMDb/TMDB matching, schedule/catalog stages |
| `downloader/` | aria2c orchestration, queue building, limits, drain phases, integrity/tagging helpers |
| `static/js/modules/` | Modular dashboard frontend: cards, filters, logs, calendar, Plex, integrity, social, holidays, playback hooks |
| `static/js/settings/` | Settings panels: general, filters, keywords, backups, DB, themes, Plex |
| `static/css/dashboard/` | Split dashboard styling: base, search, controls, cards, sync/logs, responsive, calendar, social, Plex |
| `templates/partials/` | Dashboard and settings partials used by the Flask/Jinja views |
| `scripts/` and setup files | Docker/native setup, Codex/bootstrap helpers, runtime/tool publishing support |
| `tests/` | Contract, web, DB, downloader, sync, admin, import-surface, and regression tests |

## Settings Inventory

Settings are loaded through `config_store` as the primary source. Legacy `settings` table compatibility exists, but user-facing settings should read/write through `load_config("settings")` / `save_config("settings", ...)` or the shared config helpers.

| Settings Tab | Controls |
|---|---|
| General / IPTV | Primary IPTV domain, username, password, test button, domain resolver, optional second account |
| API keys | TMDB credential, OMDb key |
| IMDb watchlist | Public IMDb watchlist URL and CSV upload path |
| Download | Download root folder, aria2c connections, trash directory, smart restart toggle and speed threshold, download interval |
| Download limits | Daily files, daily GB, monthly files, monthly GB, live usage status |
| Stale series | Stale-days threshold and section-level stale auto-exclusion toggles |
| Theme mode | Auto, light, dark; holiday theme overlay can temporarily override |
| Exclusions | Global country, genre, and language exclusions |
| Section filters | Per-section min year, min rating, and min vote count |
| Section rules | Per-section banned keywords, pre-rejected keywords, country/genre/language overrides |
| Browse & Exclude | Visual provider browser for rejecting/excluding items without leaving settings |
| Backups | Create, list, download, upload, restore, delete backups |
| Plex Connect | Local Plex connection, libraries, users, section interest, future episode dates toggle |
| Database | Admin table browser, search, pagination, SQL query, row delete, maintenance, repair covers |
| Themes | Theme list, preview, activation |
| Remote | Remote access URL/password/status and connected-device support details |
| Maintenance | Sync/download controls, intervals, auto-maintenance status |
| Publish | Admin release/publish controls, GitHub release status, Docker option |

## Capability Details

### Dashboard And Review

- Multi-section dashboard with live section counts and source category labels.
- Status tabs for Pending, Accepted, Rejected, Excluded, and richer review slices.
- Card grid/list style surfaces with stable responsive sizing.
- Cards show poster, title, year, rating, vote count, runtime, country, genres, source/platform badges, local/online episode counts, and exclusion reasons.
- Global search returns cross-section results with thumbnails and status badges.
- Toolbar exposes live player, logs, Plex, Devices, settings, sync, download, calendar, filter breakdown, and view controls.

### Decisions And Variants

- Accept/reject decisions persist immediately.
- Series acceptance supports everything, new only, and custom season/episode range.
- Duplicate/version detection keeps sibling entries grouped by source/category.
- Chosen variant ID is preserved separately from parent media ID.
- Group rejection can reject all sibling variants.
- Watched+removed can mark media watched and move downloaded files through trash.

### Sections And IPTV Categories

- Sections are user-created source groups with display name, stable ID, location, filter thresholds, and mode flags.
- Categories map IPTV provider category IDs to sections.
- Users can add/remove source categories through the UI.
- Section headers show disk usage, source tags, scan controls, and quick filters.
- Delete info endpoint previews cascade effects before destructive section deletion.

### Filtering And Exclusions

- Global exclusions apply across all sections.
- Section-specific country, genre, language, keyword, pre-reject, min year, rating, and vote thresholds override or refine global behavior.
- Auto-excluded items retain clear reasons so nothing disappears silently.
- Banned keywords exclude; pre-rejected keywords reject.
- Retrospective application updates pending items when rules change.

### Sync And Metadata

- Sync fetches provider content, section categories, series/movie lists, metadata, and covers.
- TMDB/OMDb enrich titles with posters, ratings, votes, release dates, country, language, cast, plot, and IDs.
- IMDb ID authority is preferred where available.
- Provider response shape differences are handled explicitly for movies vs series.
- Cover write path is centralized to prevent broken cover state.

### Downloads And Limits

- aria2c handles multi-connection downloads and resume.
- Queue building respects accepted decisions, selected variants, custom episode ranges, limits, disk state, and known local files.
- Speed monitoring can restart stalled downloads.
- Daily/monthly file and GB limits are read live from settings.
- Bandwidth tables track today/week/month and per-day file details.
- Download state appears in cards, logs, status bars, and dashboard analytics.

### Local Playback

- Browser playback routes serve local files, IPTV streams, remuxed media, and transcode-prepared files.
- Direct playback is used for browser-safe media.
- Remux/proxy paths are used when codecs are safe but the container is not ideal.
- Controlled transcode cache handles legacy formats with CPU guard, concurrency limit, free-space check, TTL, size cap, and orphan cleanup.
- Watch progress, history, continue-watching, stream start/stop, and episode refresh endpoints support the player UI.

### Plex Tracking And Reclaim

- Plex Connect stores local server details and mapped libraries.
- Plex users can be tracked, nicknamed, and marked interested/uninterested per section.
- Watch activity groups media into In Progress, Reclaim Ready, All Linked, Untouched, and Unmatched.
- Reclaim safety requires watched state plus schedule completeness; future or missing episodes block reclaim.
- Reclaim actions are explicit and go through trash, not direct filesystem deletion.

### Disk Discovery, Identity, And Gone Items

- Disk scan finds media files already on disk and can link them to IPTV media.
- Discovery handles local-only files, sibling variants, ignored paths, unknown observations, and manual review.
- Filename/folder normalization supports noisy release names and Arabic titles.
- Gone-from-IPTV inbox lets users choose swap, delete-to-trash, or ignore per item.
- Disk identity safeguards prevent one device/path fix from being treated as universal.

### Integrity And Trash

- Integrity is detect-only until the user chooses action.
- Issues include missing files, partial downloads, corrupt/truncated files, unlinked media, stale artifacts, and mismatched ownership.
- Trash stores metadata for restore, including original decision context where needed.
- Restore recreates decisions/mapping state and moves files back safely.
- Permanent delete is explicit and guarded.

### Remote, Devices, And Repair

- Remote control supports authenticated pending review and downloader control.
- Connected Devices aggregates telemetry, version, OS, health, and device history.
- Device aliases and deleted-device state are stored separately.
- WebSocket command relay and SSH terminal/repair presets exist for admin recovery workflows.
- Tunnel/VPN-related operations have dedicated safety rules and should not be used as general manual repair on clients.

### Updates, Publish, Runtime, Toolchain

- Public clients update from GitHub releases.
- Release ZIPs contain runtime package paths, while admin-only surfaces are excluded.
- Support channels store installer, Python runtime, and external toolchain bundles by content hash.
- Runtime status reports Python executable, managed/runtime hash, platform, and errors.
- Tools status reports managed toolchain state and availability of aria2c, ffmpeg, ffprobe, MKVToolNix, yt-dlp, Chrome/Chromedriver, nginx, openssl, curl, ssh, and ssh-keygen.
- Publish verifies release assets and can mirror release packages.

### Themes, Mobile, And PWA

- Dashboard and settings support auto/light/dark modes.
- Holiday themes cover Ramadan, Eids, Coptic/Christian holidays, national holidays, and seasonal decorations.
- Mobile layouts include responsive grids, overlays, devices panel, connected-device cards, history, repair, and trash paths.
- PWA includes manifest, icons, service worker, push subscription, unsubscribe, and test notifications.
- Auto-generated SSL and local CA install support LAN usage at `https://iptv.local`.

## Background Jobs

| Job | Purpose |
|---|---|
| Sync | Fetch provider content, metadata, filters, covers, categories, and DB updates |
| Download | Build accepted queue, enforce limits, download files, update state |
| Integrity | Detect partial/corrupt/missing/unlinked media and resume safe partials |
| Backup | Create and retain database backups |
| Maintenance | DB stats, cover upgrades, cleanup, cache refresh, theme/holiday checks |
| Telemetry | Connected device heartbeat, status, history, remote command relay |
| Plex sync | Pull local Plex users, libraries, watch states, and linked media state |
| Episode schedule | Refresh season episode availability and future dates where enabled |
| Runtime/tool update | Apply managed Python/toolchain manifests independently from code updates |

## Data And Safety Rules

- `config_store` is the primary settings backend.
- Compare IDs as strings across DB, config, and UI boundaries.
- OMDb is authority when `imdb_id` exists.
- Media deletion must go through trash.
- Do not assume third-party response shapes; inspect actual IPTV/TMDB/OMDb responses before coding against them.
- Do not break destructive guards, API shape helpers, cover-write single path, or publish preflight checks.
- Docker-first is the supported production path.
- Release docs must not expose tokens, credentials, Plex machine IDs, public IPs, SSH data, local filesystem paths, or device identifiers.

## API Inventory

The generated API inventory found 299 route decorators across web and admin modules during this pass. See [`API_ENDPOINTS.md`](API_ENDPOINTS.md) for the complete generated list.

## Release-State Notes

- Latest public source baseline inspected: `v3.5.599`.
- Plex tracking and safe disk discovery are released in the public v3.5 line.
- Managed runtime/toolchain support is part of the recent v3.5 line.
- Accepted future badges and S-Watchlist future filtering were visible in the local working tree during this pass and should be checked against the latest release before advertising them as client-installed behavior.
