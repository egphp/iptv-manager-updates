# IPTV Manager Feature Inventory

Generated for the public documentation refresh on 2026-04-29 after inspecting the active source tree around `v3.5.599`. This file is intentionally detailed: it lists the product surface, settings surface, background jobs, data model, frontend modules, release state, and operational rules.

## Product Surface Register

| Area | Status | Capabilities |
|---|---|---|
| Dashboard review board | Released | Multi-section media grid, status tabs, live counts, posters, rating badges, country/genre/year/source filters, search, sort, group-only view |
| Decisions | Released | Accept, reject, force accept, reject group, watched+removed, chosen variant, custom episode range, new-only mode, decision audit trail |
| Sections | Released | Add/edit/delete, enable toggle, mode selection, source categories, folder selection, disk usage, source labels, scan section |
| Metadata | Released | TMDB/OMDb/IMDb enrichment, posters, cast, director, plot, rating, votes, runtime, country, language, release data, IDs |
| Filtering | Released | Global and per-section country/genre/language exclusions, banned keywords, pre-rejected keywords, min year, min rating, min votes |
| Downloads | Released | aria2c queue, resume, smart restart, daily/monthly limits, per-file history, bandwidth stats, process control, logs |
| Local playback | Released | Direct local serving, proxy/remux tiers, guarded transcode preparation, watch progress, continue watching, history |
| Plex tracking | Released | Plex connection, library mapping, user watch state, user interest per section, reclaim readiness, safety checks |
| Future episode schedules | Recent v3.5 work | Future badges, VOD future rows, S-Watchlist future filter, schedule refresh, reclaim blocking for not-yet-aired episodes |
| Disk discovery | Released | Scan local media, link external files, merge discovered items, ignored paths, folder identity, Arabic/noisy filename matching |
| Gone inbox | Released | User-driven review for provider-missing items: swap, trash, ignore; replaces silent destructive flows |
| Integrity | Released | Detect-only scanner, partial/corrupt/missing/unlinked issues, resume action, progress endpoints, dashboard banner |
| Trash | Released | Safe move, restore metadata, permanent delete with explicit action, cover repair cooperation, identity preservation |
| Search | Released | FTS/autocomplete, cross-section results, suggestions, recent searches, preview, IPTV search refresh, trending |
| Live TV | Released | Live channel browse/playback, HLS/proxy routes, mobile fullscreen, session lock, live logs, category exclusions, stats |
| Actors and rich detail | Released | Actor search, actor media, actor photo route, cast/detail overlay, trailers, gallery, hover detail |
| Social Watch | Released | Device-grouped feed, dedupe, allowlist, badges, push events, monthly stats, featured cards |
| Connected devices | Released | Telemetry, aliases, version grouping, active/disconnected summaries, history, update state, admin repair workflows |
| Updates and publish | Released | GitHub release packages, update checks, managed runtime/toolchain, support channels, mirror upload, package preflight |
| Themes and PWA | Released | Light/dark/auto, holiday themes, service worker, manifest, icons, local certificate install, push notifications |

## Detailed Capability Register

### Dashboard And Cards

- Section tabs, status tabs, sub-tabs, count badges, and dashboard navigation memory.
- Movie and series cards with poster, title, source, year, rating, votes, runtime, country, genres, local/online/future counts, badges, and action overlay.
- Lazy card fallback, hover background, card scroll behavior, group modal, grid view, empty-state watchdog, and responsive mobile card grids.
- Rich Flex detail: poster, gallery, trailers, cast/director/plot, awards, runtime, and media profile.

### Decision Engine

- Accept, reject, force accept, reject group, watched+removed, untrack, dismiss season, and undo match.
- Chosen source/variant is preserved independently of parent grouping.
- Accept flow supports entire series, new-only series, and custom season/episode starts.
- Rejected/excluded/accepted state appears in cards, search, logs, trash, and DB rows.

### Sync Pipeline

- Provider bootstrap, category fetch, VOD/series fetch, shape helpers, shared request gates, catalog snapshots, and stage-based processing.
- Stage flow covers config, prefilter, repair, watchdog, watched state, override, bulk handling, enrichment, section loops, heal, maintenance, purge, and summary.
- TMDB/OMDb work includes poster caching, image prefetch, trailer data, IMDb watchlist integration, and authority rules when IMDb IDs exist.
- Covers use a central write path to avoid broken or stale cover state.

### Downloader Pipeline

- Queue build for movies and series, section cooldown, limits, accepted range filtering, disk state checks, and duplicate avoidance.
- aria2c orchestration with resume, retry/backoff, smart restart, per-file result handling, and download history.
- Phase A/Phase B flows for drain verification, incomplete file handling, and final download execution.
- Tagging/integrity cooperation avoids infinite re-tag loops and broken Matroska cases.

### Playback And Watch State

- Local playback chooses direct, proxy, remux, or transcode-prepared routes based on browser/container/codecs.
- Transcode preparation has guardrails for CPU, concurrent jobs, free disk, TTL, cache size, and orphan cleanup.
- Watch progress supports movies and series, current episode selection, continue watching, history tab, and dismiss actions.
- iOS/Safari flows have dedicated HLS/remux fixes and resume behavior.

### Plex Tracking And Reclaim

- Plex Connect discovers local server libraries and users, then maps libraries to IPTV sections.
- Watch state groups content into in-progress, reclaim-ready, linked, untouched, and unmatched views.
- Per-user section interest affects reclaim suggestions.
- Reclaim is blocked when future/missing aired episodes make removal unsafe; actions route through Trash.

### Disk Discovery And Identity

- Disk scan finds existing movie/series files, detects folder identity, handles sibling variants, and supports manual link/merge.
- Path state is scoped by device to avoid treating one machine's disk state as universal.
- File fingerprinting and folder-aware episode keys reduce rename drift and duplicate loops.
- Ignored paths, local-only files, and discovered variants remain visible for review.

### Gone Inbox And Trash

- Gone inbox records accepted items no longer found in the provider catalog and asks the user to swap, trash, or ignore.
- Trash stores metadata needed for restore: media ID, section ID, chosen variant, original reason, and location context.
- Restore rebuilds mapping/decision state and moves files back safely.
- Permanent delete is explicit and separate from normal cleanup.

### Integrity

- Scanner detects missing, partial, corrupt/truncated, stale-artifact, and unlinked conditions.
- Integrity issues remain detect-only until the user chooses Resume, Trash, or Ignore.
- Dashboard banner, count endpoint, detail list, progress endpoint, action endpoint, and active-state endpoint all support the review loop.
- Downloader respects integrity state and avoids operating on unlinked media.

### Operations

- Live log cards, full log tabs, system statistics, bandwidth charts, maintenance actions, and process control.
- Connected Devices tracks heartbeat, version, OS, history, aliases, disconnected thresholds, reports, and update state.
- Release publishing builds ZIP/update assets, verifies required files, handles runtime/toolchain manifests, and can publish support packages.
- Managed runtime and external media tools reduce client drift.

## Settings Register

| Settings Area | Concrete Controls | Source Surface |
|---|---|---|
| IPTV connection | Domain/server field, account fields, second account, test buttons, domain resolver, IMDb watchlist URL | `templates/partials/settings/general/iptv_connection.html`, `static/js/settings/general.js`, `static/js/settings/iptv_resolver.js` |
| Metadata services | TMDB field, OMDb field | `templates/partials/settings/general/api_keys.html` |
| Download settings | Root folder, folder browser, aria2c connections, IMDb CSV file, trash folder, smart restart, speed threshold, download interval | `templates/partials/settings/general/download_settings.html` |
| Download limits | Daily file count, daily GB, monthly file count, monthly GB, live usage box | `templates/partials/settings/general/download_limits.html` |
| Stale series | Stale days and selected sections | `templates/partials/settings/general/series_stale.html` |
| Theme mode | Auto, light, dark | `templates/partials/settings/general/theme_mode.html` |
| Global exclusions | Countries, genres, languages | `templates/partials/settings/exclusions_panel.html`, `web/routes/settings/section_config.py` |
| Section filters | Min year, min rating, min votes per section | `templates/partials/settings/filters_panel.html`, `static/js/settings/filters.js` |
| Section rules | Banned keywords, pre-rejected keywords, section countries, genres, languages | `templates/partials/settings/keywords_panel.html`, `static/js/settings/keywords.js` |
| Browse/exclude | Section selector, search, visual content review | `templates/partials/settings/browse_panel.html`, `static/js/settings/browse.js` |
| Backups | Create, upload/restore, list, download, delete | `templates/partials/settings/backups_panel.html`, `web/routes/backups.py` |
| Plex Connect | Connect, re-test, disconnect, library list, users, future episode dates | `templates/partials/settings/plex_panel.html`, `static/js/settings/plex.js`, `web/routes/system/plex.py` |
| Themes | Holiday list, preview, activation | `templates/partials/settings/themes_panel.html`, `static/js/settings/themes_browser.js` |
| Remote | Access status and admin support controls | `templates/partials/settings/remote_panel.html` |
| Maintenance | Sync interval, manual sync/download/stop/kill, auto-maintenance status | `templates/partials/settings/maintenance_panel.html`, `static/js/settings/maintenance.js` |
| Publish | Release ZIP/Docker publish controls and log | `templates/partials/settings/publish_panel.html`, `static/js/settings/publish.js`, `admin/routes/publish.py` |
| Database | Table list, table browser, search, pagination, maintenance, SQL | `templates/partials/settings/database_panel.html`, `static/js/settings/database.js`, `admin/routes/database_ops.py` |

## Database And Storage Inventory

| Table/Store | Purpose |
|---|---|
| `sections`, `categories` | User sections and provider category membership |
| `media`, `mediafiles`, `decisions`, `movie_mapping` | Core catalog, variants/files, decision state, stream/file mapping |
| `media_fts` | Full-text search over media names and metadata |
| `exclusion_rules` | Global and section-specific filter rules |
| `config_store`, `settings` | JSON settings source and compatibility rows |
| `api_cache` | Provider/API response cache |
| `daily_stats`, `daily_downloads`, `download_history`, `download_runtime` | Bandwidth, file history, and downloader runtime state |
| `integrity_issues`, `integrity_tracker`, `watchdog` | Integrity scanner state and failed-item tracking |
| `gone_items`, `trash metadata on disk` | Gone inbox and restore context |
| `watch_progress`, `watch_log` | Local playback progress and history |
| `series_tracker`, `episode_catalog`, `series_episode_schedule` | Series progress, local/provider episode catalog, future dates |
| `plex_users`, `plex_items`, `plex_watch_state`, `plex_reclaim_log`, `plex_user_section_interest` | Plex tracking, reclaim, user interest |
| `disk_ignores`, `disk_path_state` | Disk discovery ignore and device-scoped path state |
| `push_subscriptions`, `social_feed`, `social_monthly` | Push and social-watch surfaces |
| `holiday_dates`, `actors`, `media_cast` | Holiday activation and actor/cast cache |

## Background Jobs And Recurring Work

| Job | Work Performed |
|---|---|
| Sync | Provider fetch, metadata, filters, categories, covers, schedule/catalog refresh, DB updates |
| Download | Accepted queue build, limits, aria2c execution, resume, tagging, history |
| Integrity | Detect partial/corrupt/missing/unlinked media and prepare user actions |
| Backup | Create and retain DB backups |
| Maintenance | DB stats, cache cleanup, cover repair, stale locks, theme/holiday checks |
| Telemetry | Device heartbeat, version/history, support relay state |
| Plex sync | Libraries, users, watch state, linked media, reclaim state |
| Episode schedule | Future date refresh and schedule cache update |
| Runtime/tool update | Managed Python and external media/download tool updates |

## Release-State Notes

- Latest source baseline inspected: `v3.5.599`.
- The documentation repo is public release/documentation surface; the development source tree is separate.
- Plex tracking, disk discovery, trash, integrity, connected devices, and managed runtime/toolchain are part of recent v3.5 work.
- Future episode badges and S-Watchlist future filtering were included because they are visible in the inspected v3.5 source and screenshots; users should update to the latest release before expecting every recent surface.

## Operational Rules Reflected In The Docs

- `config_store` is the primary settings backend.
- Compare DB/config/UI IDs as strings.
- OMDb is authority when an IMDb ID exists.
- Media removal routes through Trash.
- Third-party response shapes are inspected before assuming structure.
- Docker-first is the supported production path.
- Public screenshots show curated views only; private operational values are not intentionally displayed.
