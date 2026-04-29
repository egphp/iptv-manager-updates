<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/01-dashboard-movie-grid.jpg" alt="IPTV Manager dashboard" width="100%">
</p>

<h1 align="center">IPTV Manager v3.5</h1>

<p align="center">
  <strong>Plex-first IPTV content manager, downloader, tracker, and operations dashboard.</strong><br>
  Discover what is new, decide what is worth keeping, download automatically, watch locally or in Plex, and keep every decision traceable.
</p>

<p align="center">
  <strong>مدير IPTV ذكي لـ Plex</strong><br>
  يكتشف الجديد، يفلتر بذكاء، يخليك تقبل أو ترفض، يحمل تلقائيا، ويتابع كل شيء بوضوح.
</p>

<p align="center">
  <a href="../../releases/latest"><img src="https://img.shields.io/badge/Download-Latest%20Release-gold?style=for-the-badge&logo=github" alt="Download"></a>
  <a href="https://www.paypal.com/ncp/payment/GYPXYRC3MJ85C"><img src="https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal" alt="Donate"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker" alt="Docker">
  <img src="https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Flask%20%2B%20Cheroot-HTTPS-green?style=flat-square" alt="Flask and Cheroot">
  <img src="https://img.shields.io/badge/SQLite-WAL-lightgrey?style=flat-square" alt="SQLite WAL">
  <img src="https://img.shields.io/badge/PWA-Installable-orange?style=flat-square" alt="PWA">
  <img src="https://img.shields.io/badge/mDNS-iptv.local-purple?style=flat-square" alt="mDNS">
  <img src="https://img.shields.io/badge/Theme-Auto%20%7C%20Light%20%7C%20Dark-333?style=flat-square" alt="Theme">
</p>

---

## Quick Start | البداية السريعة

```bash
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 \
  -v iptv-data:/app/data \
  -v /path/to/media:/media \
  -e TZ=Africa/Cairo \
  iptv-manager

# Open https://iptv.local
```

Windows users can download `setup-docker.bat` from the latest release for a one-click Docker setup. The Docker path is the recommended production path.

---

## Why It Exists | الفكرة

IPTV subscriptions often have huge catalogs but weak playback, no proper resume, no thumbnails, no watch history, and no clean media ownership. IPTV Manager turns that feed into a controlled local media workflow:

- Browse new movies and series in one dashboard.
- Accept only what you want and reject or auto-exclude the rest.
- Download with aria2c, resume partial files, and track bandwidth.
- Enrich with TMDB, OMDb, IMDb ratings, posters, countries, genres, and release dates.
- Watch through Plex, local playback, or browser VOD routes.
- Keep recovery paths: trash, backups, integrity scanner, disk discovery, and DB repair.

الهدف إن IPTV يبقى مكتبة منظمة: اختيارات واضحة، تحميل تلقائي، ميتاداتا كاملة، متابعة في Plex، واسترجاع آمن بدل الفوضى.

---

## Feature Tour | جولة المميزات

Every screenshot below is from the running app. Sensitive values in newer admin and Plex screenshots were cropped or redacted before publishing. Schedule-aware Accepted/S-Watchlist screenshots are included as current development snapshots; check the inventory release-state notes before assuming they are installed on every client release.

### Dashboard, Cards, And Decisions

Browse sections, status tabs, live counts, global search, sort modes, genre/country filters, and high-information movie/series cards.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/02-status-filter-bar.jpg" width="49%" alt="Status tabs and filters">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/03-accept-reject-hover.jpg" width="49%" alt="Accept reject overlay">
</p>

- Status tabs: Pending, Accepted, Rejected, Excluded, Rich/quality review.
- Cards: posters, IMDb rating, vote count, year, runtime, genre, country, source labels, local/online episode badges.
- One-click Accept, Reject, Force Accept, reject group, and watched/removed flows.
- Push-deep links and dashboard navigation memory without overwriting saved user state.

### Versions, Sources, And Episode Ranges

Duplicate IPTV entries are treated as versions, not random duplicates. Pick the source/quality you want and control exactly which episodes download.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/04-series-card-versions.jpg" width="32%" alt="Version badge">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/05-accept-version-picker.jpg" width="32%" alt="Version picker">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/06-accept-episode-range.jpg" width="32%" alt="Episode range picker">
</p>

- IPTV source categories are visible and editable per section.
- Accept modes: everything, new only, or a custom season/episode range.
- Variant decisions preserve the chosen source ID separately from the parent media ID.
- Same-section safeguards prevent unrelated titles with matching metadata from being merged incorrectly.

### Accepted Library, Local Counts, And Future Episodes

Accepted items show local episode counts, online totals, start points, latest-downloaded ordering, and upcoming episode signals when schedule data is available.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/07-accepted-series-tracking.jpg" width="49%" alt="Accepted tracking">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/41-accepted-future-schedules.jpg" width="49%" alt="Accepted future schedules">
</p>

- Local/TOTAL badges separate disk state from IPTV availability.
- Stale `.aria2` and hidden artifacts are ignored so failed partials do not count as real episodes.
- Accepted-grid ordering can prioritize the most recently downloaded episode.
- Schedule-aware badges show pending future episodes without starting playback for unaired content.

### Plex Connect And Watch Tracking

Plex integration connects to a local server, maps libraries to IPTV sections, reads watch activity, and helps decide what can be reclaimed safely.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/44-plex-connect-schedule-redacted.jpg" width="100%" alt="Plex Connect settings">
</p>

- Local Plex connection test, library discovery, and section mapping.
- Plex user watch activity with nicknames and per-section interest controls.
- In Progress, Reclaim Ready, All Linked, Untouched, and Unmatched views.
- Reclaim safety blocks deletion when future or missing aired episodes still exist.
- Reclaim actions are manual and route through the trash system.

### Watchlist And Browser Playback

The app includes local/browser playback routes, series episode lists, local file serving, remux/proxy support, and controlled transcode preparation for legacy formats.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/42-vod-future-episodes.jpg" width="49%" alt="VOD future episodes">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/43-watchlist-future-filter.jpg" width="49%" alt="Watchlist future filter">
</p>

- Direct playback for browser-safe MP4/WebM-like files.
- Remux/proxy routes for compatible media in non-browser containers.
- Guarded transcode cache for legacy formats with CPU, concurrency, disk-space, TTL, and LRU caps.
- S-Watchlist tracks watched progress, IMDb watchlist coverage, future episodes, and schedule gaps.

### Settings And Filtering

Settings are broad enough to control the full pipeline without editing files by hand.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/30-settings-download.jpg" width="49%" alt="Download settings">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/31-settings-exclusions.jpg" width="49%" alt="Global exclusions">
</p>

- IPTV credentials, second account, domain resolver, API keys, IMDb watchlist URL/CSV.
- Download root, trash directory, aria2c connections, smart restart speed threshold, daily/monthly limits.
- Global and per-section exclusions by country, genre, language, banned keyword, and pre-rejected keyword.
- Section filters: min year, IMDb rating, vote count, stale-series behavior, VOD/movie mode, IPTV-only mode, 4K source flag.
- Theme mode, holiday themes, remote access, maintenance intervals, backups, DB browser, and publish panel.

### Search, Analytics, Logs, And Operations

The dashboard includes search, filter analytics, bandwidth charts, live logs, and operational controls.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/19-cross-section-search.jpg" width="32%" alt="Cross-section search">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/22-system-statistics.jpg" width="32%" alt="System statistics">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/25-sync-download-logs-live.jpg" width="32%" alt="Live logs">
</p>

- Cross-section search with status badges and thumbnails.
- Filter breakdown by country and genre.
- Bandwidth history by day/month, download folder stats, DB size, media counts.
- Live sync/download panels plus full log viewers.
- Manual Sync, Download, Stop, Kill All, integrity trigger, and section-specific scans.

### Disk Discovery, Integrity, Trash, And Gone Items

The system treats local files and destructive actions carefully.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/46-gone-from-iptv-inbox.jpg" width="49%" alt="Gone from IPTV inbox">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/38-settings-database-browser.jpg" width="49%" alt="Database browser">
</p>

- Disk discovery finds existing files, links or merges them manually, and avoids resurrecting rejected/excluded owners.
- Gone-from-IPTV inbox lets you swap, delete-to-trash, or ignore missing provider entries.
- Integrity scanner detects broken, truncated, partial, and mismatched files without deleting automatically.
- Trash stores metadata for restore and is the only path for media deletion.
- Database browser supports table inspection, pagination, search, maintenance, and controlled SQL for admins.

### Connected Devices, Remote Repair, And Update Health

Admin surfaces help monitor client devices, releases, telemetry, and repair channels without requiring manual edits on each client.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/45-connected-devices-overview.jpg" width="100%" alt="Connected devices overview">
</p>

- Device heartbeat, OS/platform/version grouping, cache status, and active/disconnected summaries.
- WebSocket command relay and SSH repair tools for authorized admin workflows.
- Support-channel releases for installers, managed Python runtime bundles, and external toolchains.
- Auto-update preflight checks for dependencies, runtime/tool manifests, and package integrity.

### Themes, Mobile, PWA, And Notifications

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/39-dark-theme.jpg" width="49%" alt="Dark theme">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/40-status-bar-series.jpg" width="49%" alt="Series status bar">
</p>

- Auto, light, and dark themes across dashboard, settings, cards, modals, and charts.
- Egyptian holiday theme system with seasonal visual assets and activation windows.
- Installable PWA with service worker, local icons, auto-SSL, local CA install, and Web Push notifications.
- Mobile card grids, toolbar layout, overlays, settings pages, and admin panels have responsive variants.

---

## Complete Inventory

The README is intentionally readable. The full audit-style inventory lives in docs:

- [`docs/FEATURE_INVENTORY.md`](docs/FEATURE_INVENTORY.md) — every major subsystem, feature, setting group, background job, safety rule, and release state.
- [`docs/API_ENDPOINTS.md`](docs/API_ENDPOINTS.md) — generated API endpoint inventory from the source tree.
- [`docs/SCREENSHOT_AUDIT.md`](docs/SCREENSHOT_AUDIT.md) — image sources, redaction notes, and sensitive-data checks.

---

## Architecture | البنية

```text
Browser / PWA
  -> Flask blueprints on Cheroot HTTPS
  -> SQLite WAL + config_store + normalized media tables
  -> Sync pipeline: IPTV API -> TMDB/OMDb/IMDb -> filters -> DB
  -> Download pipeline: aria2c -> metadata tagging -> Plex/local media folders
  -> Background jobs: sync, download, integrity, backups, telemetry, schedules
```

| Layer | Main Role |
|---|---|
| Docker + setup scripts | Recommended deployment, auto-SSL, mDNS, persistent data volume |
| Flask + Cheroot | Web dashboard, APIs, PWA, local playback, admin operations |
| SQLite WAL | Media, decisions, settings, logs, tracking, discovery, trash, telemetry |
| Sync pipeline | Provider discovery, metadata enrichment, filtering, matching, cover caching |
| Downloader | aria2c queueing, resume, limits, bandwidth, tagging, integrity cooperation |
| Plex tracking | Local Plex status, user watch activity, section interest, reclaim safety |
| Runtime/toolchain manager | Managed Python and external media/download tools for client stability |

---

## First Run

1. Open `https://iptv.local`.
2. Accept the local self-signed certificate once, or install the local CA from `/install-ca`.
3. Open Settings and enter IPTV credentials.
4. Add TMDB and OMDb keys for richer metadata.
5. Create sections, attach IPTV categories, and set download folders.
6. Run Sync.
7. Accept what you want; downloads run automatically.

---

## Security And Safety Notes

- Do not publish screenshots with IPTV credentials, tokens, Plex machine IDs, public IPs, SSH data, local paths, or device identifiers.
- Settings are stored through `config_store`; direct `settings` table reads are legacy fallback only.
- Media deletion goes through trash with restore metadata.
- ID comparisons across DB/config/UI should be string-normalized.
- OMDb is treated as authority when an IMDb ID exists.

---

## Support | الدعم

If the project saves you time, bandwidth, or frustration, support helps continued development:

<p align="center">
  <a href="https://www.paypal.com/ncp/payment/GYPXYRC3MJ85C"><img src="https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal" alt="Donate"></a>
</p>

---

## License

MIT License — free to use, modify, and distribute.
