# Screenshot Audit

Documentation refresh date: 2026-04-29. All 46 published screenshots are referenced individually from the README. The README no longer groups multiple images into side-by-side galleries.

## Audit Summary

| Result | Count | Notes |
|---|---:|---|
| Existing screenshots retained and re-documented | 40 | Restored into the README tour as individual sections |
| New screenshots added | 6 | Accepted future schedules, VOD future rows, S-Watchlist future filter, Plex Connect, Connected Devices, Gone inbox |
| Screenshots with metadata stripped in this pass | 46 | `exiftool -all= -overwrite_original screenshots/*.jpg` |
| OCR public-safety scan | 46 | Tesseract text extraction plus pattern scan returned no hits for private operational values |
| Cropped/redacted newer captures | 2 | Plex Connect and Connected Devices public captures were reduced before publishing |

## Published Screenshot List

| # | File | README Section | Review Note |
|---:|---|---|---|
| 1 | `01-dashboard-movie-grid.jpg` | Dashboard Movie And Series Grid | Public UI state only |
| 2 | `02-status-filter-bar.jpg` | Status Tabs And Filter Bar | Public UI state only |
| 3 | `03-accept-reject-hover.jpg` | Accept And Reject Overlay | Public UI state only |
| 4 | `04-series-card-versions.jpg` | Multiple Versions Detection | Public UI state only |
| 5 | `05-accept-version-picker.jpg` | Version Picker | Public UI state only |
| 6 | `06-accept-episode-range.jpg` | Episode Range Picker | Public UI state only |
| 7 | `07-accepted-series-tracking.jpg` | Accepted Series Tracking | Public UI state only |
| 8 | `08-accepted-series-progress.jpg` | Accepted Episode Progress | Public UI state only |
| 9 | `09-section-sources-labeled.jpg` | Section Source Labels | Public UI state only |
| 10 | `10-section-header-details.jpg` | Section Header Details | Public UI state only |
| 11 | `11-add-new-section.jpg` | Add New Section | Public UI state only |
| 12 | `12-edit-section.jpg` | Edit Section | Public UI state only |
| 13 | `13-add-category-source.jpg` | Add Category Source | Public UI state only |
| 14 | `14-filter-dropdowns.jpg` | Filter Dropdown Controls | Public UI state only |
| 15 | `15-genres-dropdown.jpg` | Genre Dropdown With Counts | Public UI state only |
| 16 | `16-countries-dropdown.jpg` | Country Dropdown With Counts | Public UI state only |
| 17 | `17-sort-dropdown.jpg` | Sort Dropdown | Public UI state only |
| 18 | `18-groups-only-filter.jpg` | Groups Only Filter | Public UI state only |
| 19 | `19-cross-section-search.jpg` | Cross Section Search | Public UI state only |
| 20 | `20-filter-breakdown-countries.jpg` | Country Filter Breakdown | Public UI state only |
| 21 | `21-filter-breakdown-genres.jpg` | Genre Filter Breakdown | Public UI state only |
| 22 | `22-system-statistics.jpg` | System Statistics | Public UI state only |
| 23 | `23-bandwidth-monthly.jpg` | Monthly Bandwidth | Public UI state only |
| 24 | `24-bandwidth-daily-detail.jpg` | Daily Bandwidth Detail | Public UI state only |
| 25 | `25-sync-download-logs-live.jpg` | Live Sync And Download Logs | OCR-reviewed operational sample text |
| 26 | `26-system-logs-downloader.jpg` | Downloader System Logs | OCR-reviewed operational sample text |
| 27 | `27-sync-log-full.jpg` | Full Sync Log | OCR-reviewed operational sample text |
| 28 | `28-download-log-full.jpg` | Full Download Log | OCR-reviewed operational sample text |
| 29 | `29-sync-download-run-buttons.jpg` | Manual Sync And Download Buttons | Public UI state only |
| 30 | `30-settings-download.jpg` | Download Settings | Public UI state only |
| 31 | `31-settings-exclusions.jpg` | Global Exclusions | Public UI state only |
| 32 | `32-settings-section-filters.jpg` | Per Section Filters | Public UI state only |
| 33 | `33-settings-banned-keywords.jpg` | Banned Keywords | Public UI state only |
| 34 | `34-settings-pre-rejected.jpg` | Pre Rejected Keywords | Public UI state only |
| 35 | `35-settings-section-countries.jpg` | Section Country Rules | Public UI state only |
| 36 | `36-settings-browse-exclude.jpg` | Browse And Exclude | Public UI state only |
| 37 | `37-settings-backups.jpg` | Backups | Public UI state only |
| 38 | `38-settings-database-browser.jpg` | Database Browser | Public UI state only |
| 39 | `39-dark-theme.jpg` | Dark Theme | Public UI state only |
| 40 | `40-status-bar-series.jpg` | Series Status Bar | Public UI state only |
| 41 | `41-accepted-future-schedules.jpg` | Accepted Future Schedule Badges | Public UI state only |
| 42 | `42-vod-future-episodes.jpg` | VOD Episode List With Future Rows | Public UI state only |
| 43 | `43-watchlist-future-filter.jpg` | S Watchlist Future Filter | Public UI state only |
| 44 | `44-plex-connect-schedule-redacted.jpg` | Plex Connect And Future Dates | Cropped/redacted public feature view |
| 45 | `45-connected-devices-overview.jpg` | Connected Devices Overview | Cropped to overview metrics only |
| 46 | `46-gone-from-iptv-inbox.jpg` | Gone From IPTV Inbox | Public UI state only |

## Recheck Process Used

1. Restored every old screenshot reference into the README feature tour.
2. Added the six new v3.5 screenshots as standalone sections.
3. Re-saved all screenshot files without embedded metadata.
4. Ran OCR over all 46 images and scanned the extracted text for private operational values and address-like patterns.
5. Kept raw or more detailed admin/device captures out of the public docs.

## Future Screenshot Rule

Publish only curated public views. When a capture comes from an admin, Plex, device, repair, update, or settings surface, crop or redact it before adding it to this repository, then update this audit file with the filename and review result.
