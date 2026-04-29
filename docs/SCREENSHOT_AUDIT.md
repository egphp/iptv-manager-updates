# Screenshot Audit

Documentation refresh date: 2026-04-29.

Every screenshot used by the public README should be safe for a public repository. The review rule is conservative: do not publish passwords, tokens, IPTV provider URLs, stream URLs, API keys, Plex machine IDs, public IPs, SSH data, tunnel ports, local filesystem paths, device hashes, or personal device identifiers.

## Audit Summary

| Result | Count | Notes |
|---|---:|---|
| Existing public screenshots retained | 40 | Existing tour images already in the public repo |
| New screenshots added | 6 | New v3.5 surfaces for schedule, Plex, devices, gone inbox |
| Redacted/cropped before publish | 2 | Plex machine ID redacted; Connected Devices cropped to overview only |
| Omitted from public docs | Many local candidates | Full device cards, SSH/WS panels, Plex user-detail screenshots, and raw local tmp captures were not published |
| OCR secret-pattern hits | 0 | Tesseract pass over new screenshots and log screenshots found no token/path/key/stream patterns |

## Published Screenshot List

| File | Public Use | Sensitive Review |
|---|---|---|
| `01-dashboard-movie-grid.jpg` | README hero and dashboard tour | Public media titles/posters only |
| `02-status-filter-bar.jpg` | Status tabs and filters | No credentials |
| `03-accept-reject-hover.jpg` | Accept/reject overlay | No credentials |
| `04-series-card-versions.jpg` | Variant badge | No credentials |
| `05-accept-version-picker.jpg` | Version picker | Source names only |
| `06-accept-episode-range.jpg` | Episode range picker | No credentials |
| `07-accepted-series-tracking.jpg` | Accepted tracking | Public media metadata only |
| `08-accepted-series-progress.jpg` | Episode start/progress | Public media metadata only |
| `09-section-sources-labeled.jpg` | Section source labels | Category labels only |
| `10-section-header-details.jpg` | Section header | No credentials |
| `11-add-new-section.jpg` | Add section modal | Example section data only |
| `12-edit-section.jpg` | Edit section modal | Example section data only |
| `13-add-category-source.jpg` | Category browser | Provider category names only |
| `14-filter-dropdowns.jpg` | Filter dropdowns | No credentials |
| `15-genres-dropdown.jpg` | Genre counts | No credentials |
| `16-countries-dropdown.jpg` | Country counts | No credentials |
| `17-sort-dropdown.jpg` | Sort dropdown | No credentials |
| `18-groups-only-filter.jpg` | Groups-only filter | No credentials |
| `19-cross-section-search.jpg` | Global search | Public media titles/posters only |
| `20-filter-breakdown-countries.jpg` | Country analytics | No credentials |
| `21-filter-breakdown-genres.jpg` | Genre analytics | No credentials |
| `22-system-statistics.jpg` | System statistics | Aggregate counts only |
| `23-bandwidth-monthly.jpg` | Monthly bandwidth | Aggregate data only |
| `24-bandwidth-daily-detail.jpg` | Daily bandwidth detail | Public media titles only |
| `25-sync-download-logs-live.jpg` | Live logs | Reviewed as non-secret operational text |
| `26-system-logs-downloader.jpg` | Downloader logs | Reviewed as non-secret sample log text |
| `27-sync-log-full.jpg` | Sync log | Reviewed as non-secret sample log text |
| `28-download-log-full.jpg` | Download log | Reviewed as non-secret sample log text |
| `29-sync-download-run-buttons.jpg` | Manual run buttons | No credentials |
| `30-settings-download.jpg` | Download settings | No credential values |
| `31-settings-exclusions.jpg` | Global exclusions | Rule examples only |
| `32-settings-section-filters.jpg` | Section filters | Threshold examples only |
| `33-settings-banned-keywords.jpg` | Banned keywords | Rule examples only |
| `34-settings-pre-rejected.jpg` | Pre-rejected keywords | Rule examples only |
| `35-settings-section-countries.jpg` | Per-section country rules | Rule examples only |
| `36-settings-browse-exclude.jpg` | Browse & exclude | Public media titles/posters only |
| `37-settings-backups.jpg` | Backups | Backup names only, no paths |
| `38-settings-database-browser.jpg` | DB browser | Table names/counts only |
| `39-dark-theme.jpg` | Dark theme | Public media metadata only |
| `40-status-bar-series.jpg` | Series status bar | Aggregate counts only |
| `41-accepted-future-schedules.jpg` | Accepted future schedule badges | Public media metadata only |
| `42-vod-future-episodes.jpg` | VOD local/online/future episode list | Public episode titles/dates only |
| `43-watchlist-future-filter.jpg` | S-Watchlist future filter | Public media metadata only |
| `44-plex-connect-schedule-redacted.jpg` | Plex Connect schedule setting | Machine ID redacted before publish |
| `45-connected-devices-overview.jpg` | Connected Devices overview | Cropped before device names, hosts, ports, and per-device details |
| `46-gone-from-iptv-inbox.jpg` | Gone-from-IPTV inbox | Public media titles/posters only |

## Explicitly Not Published

- Full Connected Devices cards with device names, hostnames, performance stats, SSH/WS buttons, and port details.
- Mobile connected-device repair/history/SSH screenshots.
- Raw Plex tracking screenshots containing Plex usernames, nicknames, internal IDs, machine ID, or personal watch rows.
- Any screenshot containing visible API keys, IPTV credentials, GitHub/publish tokens, remote passwords, SSH command output, or local filesystem paths.

## Redaction Notes

- `44-plex-connect-schedule-redacted.jpg`: cropped above the Plex user activity list and masked the Plex machine ID value.
- `45-connected-devices-overview.jpg`: cropped to overview metrics only, before the device card area where names, hostnames, and action buttons appear.
- New screenshots were re-saved as JPEGs without source metadata.

## Recheck Checklist

Before any future screenshot push:

1. Inspect the full-resolution image manually.
2. Run OCR where available and scan for secret-like text.
3. Strip metadata.
4. Confirm the README references only sanitized filenames.
5. Keep raw captures in local `tmp/` or private artifacts, not in the public repo.
