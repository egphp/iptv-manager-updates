<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/01-dashboard-main.png" alt="IPTV Manager Dashboard" width="100%">
</p>

<h1 align="center">IPTV Manager</h1>

<p align="center">
  <strong>Smart IPTV content manager for Plex</strong><br>
  Browse what's new. Pick what you want. Download automatically. Watch on Plex with full control.
</p>

<p align="center">
  <strong>مدير IPTV ذكي لـ Plex</strong><br>
  تصفح الجديد. اختار اللي عايزه. التحميل أوتوماتيك. شاهد على Plex بتحكم كامل.
</p>

<p align="center">
  <a href="../../releases/latest"><img src="https://img.shields.io/badge/Download-Latest%20Release-gold?style=for-the-badge&logo=github" alt="Download"></a>
  <a href="https://www.paypal.com/ncp/payment/GYPXYRC3MJ85C"><img src="https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal" alt="Donate"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%20|%20macOS%20|%20Linux-informational?style=flat-square" alt="Platform">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/PWA-Supported-orange?style=flat-square" alt="PWA">
</p>

---

## The Story | القصة

After subscribing to multiple IPTV services, the experience was frustrating:
- **Constant buffering** and interruptions due to network or server quality
- **No thumbnails** when seeking through a video
- **No resume**, no watch history, no proper media management

**Plex solves all of this** — smooth playback, thumbnails, resume, multi-device sync. The idea was simple: browse everything new on IPTV, pick only what I want, download it automatically, and enjoy watching on Plex with full freedom.

---

بعد الاشتراك في أكتر من IPTV، التجربة كانت محبطة:
- **تقطيع مستمر** بسبب جودة النت أو السيرفرات
- **مفيش صور** أثناء التنقل للأمام في الفيديو
- **مفيش استكمال**، مفيش تاريخ مشاهدة، مفيش إدارة محتوى حقيقية

**Plex بيحل كل ده** — مشاهدة سلسة، صور مصغرة، استكمال، مزامنة بين الأجهزة. الفكرة بسيطة: أتصفح كل جديد في الـ IPTV، أختار اللي أحتاجه بس، يتحمّل أوتوماتيك، وأشاهد بحرية على Plex.

---

## Screenshots | صور الشاشة

### Dashboard — لوحة التحكم
The main interface where you browse, review, and manage all your content. Sections organized as tabs with item counts, status filters, and sorting options.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/01-dashboard-main.png" alt="Dashboard" width="100%">
</p>

### Movie & Series Cards — بطاقات الأفلام والمسلسلات
Each card shows the poster, IMDb rating badge, vote count, genres, year, and country. High-quality covers auto-downloaded from TMDB.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/02-movie-cards.png" alt="Movie Cards" width="100%">
</p>

### Accept / Reject / Watched — قبول / رفض / مشاهدة
Hover over any card to see action buttons. One click to accept for download, reject, or mark as watched.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/03-accept-reject-hover.png" alt="Accept Reject Hover" width="100%">
</p>

### Statistics Panel — لوحة الإحصائيات
Full system statistics: total series tracked, decisions made, downloads completed, bandwidth usage (daily/weekly/monthly), disk usage, and a 14-day download chart.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/04-statistics.png" alt="Statistics" width="80%">
</p>

### Settings — الإعدادات
Complete control panel with 6 tabs: General, Exclusions, Section Filters, Banned Keywords, Browse & Exclude, and Backups.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/05-settings-general.png" alt="Settings General" width="100%">
</p>

### Country / Genre / Language Exclusions — استبعاد حسب الدولة والنوع واللغة
Add countries, genres, or languages to the exclusion list. Items matching these rules are automatically filtered out with a clear reason shown in the Excluded tab.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/06-settings-exclusions.png" alt="Exclusions" width="100%">
</p>

### Banned Keywords — الكلمات المحظورة
Set keywords per section to auto-exclude or auto-reject matching titles. Retroactively applies to all existing pending items.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/07-settings-banned-keywords.png" alt="Banned Keywords" width="100%">
</p>

### Backup & Restore — النسخ الاحتياطي والاسترجاع
Automatic daily backups with full restore capability. Download, upload, or restore any backup with one click. Safety backups are created before every restore.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/08-settings-backups.png" alt="Backups" width="100%">
</p>

### Edit Section + Browse Folders — تعديل القسم + تصفح المجلدات
Edit section settings with a visual folder picker. Browse existing download folders directly from the UI instead of typing paths manually.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/09-edit-section-browse.png" alt="Edit Section Browse" width="80%">
</p>

### Excluded Tab — تاب المستبعد
Every auto-excluded item shows the reason it was filtered (low rating, low votes, region, genre, language, banned keyword). Nothing disappears — everything is traceable.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/10-excluded-tab.png" alt="Excluded Tab" width="100%">
</p>

### Mobile PWA — تطبيق الموبايل
Fully responsive design that works as a Progressive Web App. Install it on your phone's home screen for a native app experience with push notifications.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/11-mobile-view.png" alt="Mobile View" width="300">
</p>

---

## Features | المميزات

### Dashboard & UI | لوحة التحكم

| Feature | Description |
|---------|-------------|
| **Web Dashboard** | Modern dark-themed responsive UI with glass morphism design |
| **PWA Support** | Install as native app on mobile/desktop with push notifications |
| **Global Search** | Search across all sections by title, genre, or country |
| **Multi-Section Tabs** | Organize content by category (Arabic, Turkish, English, Movies, Ramadan, etc.) |
| **6 Status Tabs** | Pending, Accepted, Rejected, Watched, Excluded, Excluded but Rich |
| **Sort Options** | Sort by newest, highest rated, or most voted |
| **Infinite Scroll** | Smooth lazy-loading with IntersectionObserver |
| **Keyboard Shortcuts** | `S` to search, `1-9` to switch sections, `Escape` to close |
| **Section Enable/Disable** | Pause downloads for specific sections without losing data |
| **New Items Badge** | Pulsing gold dot on section tabs when new pending items appear |

### Content Cards | بطاقات المحتوى

| Feature | Description |
|---------|-------------|
| **IMDb Rating Badge** | Color-coded IMDb rating displayed on every card (links to IMDb page) |
| **Vote Count** | Formatted vote count (e.g. 36.7K, 1.2M) |
| **Genres & Country** | Full metadata line under each title |
| **Exclusion Reason** | Clear badge showing why an item was auto-excluded |
| **Track Info** | For accepted series: shows starting episode (e.g. S2E5) |
| **Accept / Reject / Watched** | One-click action buttons on card hover |
| **Episode Picker** | For series: choose starting episode from a live dropdown |
| **Force Accept** | Override filters and accept excluded items manually |

### Discovery & Metadata | الاكتشاف والبيانات

| Feature | Description |
|---------|-------------|
| **Auto-Sync** | Automatically discovers new series/movies from your IPTV provider |
| **TMDB Integration** | Fetches ratings, posters, genres, countries, and release dates from TMDB |
| **OMDb / IMDb** | Cross-references with OMDb for IMDb ratings and additional data |
| **IMDb Watchlist** | Auto-marks titles from your IMDb watchlist (public URL or CSV export) |
| **Cover Downloads** | Automatically downloads and caches high-quality poster images |
| **Duplicate Detection** | For movies: keeps 4K version when both 4K and SD exist |

### Smart Filters | الفلاتر الذكية

| Filter | Description |
|--------|-------------|
| **Year Filter** | Only include content from a minimum release year |
| **Rating Filter** | Minimum IMDb rating threshold per section |
| **Vote Count Filter** | Minimum vote count to filter unknown/obscure titles |
| **Country Exclusion** | Auto-exclude content from specific countries |
| **Genre Exclusion** | Auto-exclude specific genres (e.g. Animation, Documentary) |
| **Language Exclusion** | Auto-exclude by language ISO code |
| **Banned Keywords** | Auto-exclude titles containing specific keywords |
| **Pre-Rejected Keywords** | Auto-reject (not just exclude) titles with specific keywords |
| **Arabic Name Detection** | In English sections: auto-excludes titles with >30% Arabic characters |
| **Stale Series Detection** | Auto-excludes series with no new episodes in N days |
| **Skip Strict Filters** | Per-section toggle to bypass metadata/region/votes filtering |
| **Retroactive Apply** | When you add a new exclusion rule, it immediately applies to all pending items |

### Excluded but Rich | المستبعد لكن مهم

| Feature | Description |
|---------|-------------|
| **Smart Detection** | Automatically identifies high-quality excluded items (IMDb >= 6.5 AND >= 20K votes) |
| **Separate Tab** | Dedicated "Excluded but Rich" tab for easy review |
| **One-Click Accept** | Force-accept any rich excluded item with a single click |

### Downloads | التحميل

| Feature | Description |
|---------|-------------|
| **aria2c Engine** | Fast multi-connection downloads with automatic resume support |
| **Terminal Progress Bar** | Beautiful unicode progress bar: `████████░░░░ 65% \| 330/512 MB \| 67.1 Mb/s \| 30s` |
| **Dashboard Progress** | Real-time download progress with speed, size, ETA, and visual bar |
| **Integrity Check** | Verifies downloaded files, resumes partial downloads, detects corruption |
| **Daily Download Limit** | Configurable maximum number of downloads per day |
| **Bandwidth Tracking** | Daily, weekly, and monthly download volume tracking |
| **Smart Resume** | Automatically resumes interrupted downloads on restart |

### Section Management | إدارة الأقسام

| Feature | Description |
|---------|-------------|
| **Add Section** | Create new sections with IPTV category IDs, download folder, and filters |
| **Edit Section** | Modify name, download folder, year/rating filters, strict filter toggle |
| **Delete Section** | Full cascade delete with item count preview and double confirmation |
| **Browse IPTV Categories** | Load live category list from your IPTV provider |
| **Browse Download Folders** | Visual folder picker — no manual path typing needed |
| **Add/Remove Categories** | Dynamically manage IPTV source categories per section |
| **Movies vs Series** | Separate handling for VOD (movies) and series content |

### Backup System | نظام النسخ الاحتياطي

| Feature | Description |
|---------|-------------|
| **Automatic Daily Backups** | Background thread creates one backup per day automatically |
| **Manual Backup** | Create instant backups with one click |
| **Restore from Backup** | Restore any previous backup with safety backup before restore |
| **Upload & Restore** | Upload a `.db` file from your computer and restore from it |
| **Download Backups** | Download any backup file to your computer |
| **Auto-Retention** | Keeps last 3 backups, automatically deletes older ones |
| **Pre-Restore Safety** | Always creates a safety backup before any restore operation |

### Settings Panel | لوحة الإعدادات

| Tab | What it controls |
|-----|-----------------|
| **General** | IPTV connection, API keys (TMDB/OMDb), download root folder, aria2c connections, daily limit, IMDb watchlist/CSV |
| **Exclusions** | Excluded countries, genres, and languages with tag-based UI |
| **Section Filters** | Per-section min year, min rating, min vote count |
| **Banned Keywords** | Per-section banned keywords (auto-exclude) and pre-rejected keywords (auto-reject) |
| **Browse & Exclude** | Browse all IPTV content visually and reject items directly |
| **Backups** | Create, restore, upload, download, and delete backups |

### Monitoring & Logs | المراقبة والسجلات

| Feature | Description |
|---------|-------------|
| **Live Sync Log** | Real-time sync progress with visual progress bar and enrichment status |
| **Live Download Log** | Real-time download progress with speed, size, and ETA |
| **Full Log Viewer** | Scrollable popup with last 100 log lines per source |
| **System Logs Panel** | All logs from sync, downloader, and web in one filterable view |
| **System Check** | One-click file integrity check across all sections |
| **Smart Polling** | Efficient polling: fast when active, slow when idle, paused when tab hidden |

### Statistics | الإحصائيات

| Metric | Description |
|--------|-------------|
| **Total Series** | Number of tracked series/movies across all sections |
| **Total Decisions** | Total accept/reject/exclude decisions made |
| **Downloads Count** | Total number of successfully downloaded files |
| **Bandwidth Today/Week/Month** | Download volume tracking with display in section info bar |
| **Files Tracked** | Number of files in download history |
| **DB Size** | Current database size |
| **Series by Section** | Count breakdown per section |
| **Decisions by Status** | Color-coded status distribution |
| **Daily Download Chart** | 14-day bar chart with daily download counts |
| **Section Disk Usage** | Per-section folder size on disk |

---

## Platform Support | المنصات

### Windows

| Feature | Description |
|---------|-------------|
| **Setup Wizard** | One-click `.bat` installer with auto Python/aria2c installation |
| **System Tray** | Icon next to the clock with right-click menu (Start/Stop/Restart/Settings) |
| **Watchdog** | Auto-restarts the server if it crashes |
| **Auto-Update** | Checks GitHub releases every 5 minutes, auto-applies updates |
| **Startup Launch** | Automatically starts with Windows via startup shortcut |
| **Firewall Rule** | Auto-creates Windows Firewall exception for port 8888 |
| **Uninstaller** | Clean uninstall removes all shortcuts, firewall rules, and files |
| **Cron Scripts** | `run_sync.bat` and `run_downloader.bat` for Task Scheduler |

### macOS

| Feature | Description |
|---------|-------------|
| **HTTPS Support** | Built-in SSL with mkcert certificates |
| **iPhone CA Install** | `/install-ca` endpoint serves root CA for iPhone trust |
| **Menu Bar App** | Native `.app` bundle with menu bar integration |
| **Auto-Update** | Background update from GitHub releases |
| **Cron Scripts** | `run_sync.sh` and `run_downloader.sh` for crontab |

### Linux

| Feature | Description |
|---------|-------------|
| **Setup Script** | `setup.sh` checks Python, installs deps, configures permissions |
| **systemd Service** | Ready-made service template for `iptv-web.service` |
| **Log Rotation** | Auto-rotates logs at 5MB with crash reason logging |
| **Auto-Update** | Background update from GitHub releases or LAN source server |
| **.deb / .rpm** | Package builds for Ubuntu/Debian and RHEL/AlmaLinux |

---

## Installation | التسطيب

### Windows

```
1. Download IPTV_Manager_Windows.zip from Releases
2. Extract and right-click IPTV_Manager_Setup.bat → Run as Administrator
3. Follow the setup wizard (IPTV credentials + optional API keys)
4. System tray icon appears → double-click to open Dashboard
```

### macOS

```
1. Download .zip from Releases
2. Extract and move to Applications
3. Launch from Applications → menu bar icon appears
4. Open https://localhost:8888 in your browser
```

### Linux

```bash
# Ubuntu/Debian
sudo dpkg -i iptv-manager_*.deb
sudo systemctl start iptv-manager

# RHEL/AlmaLinux
sudo rpm -i iptv-manager-*.rpm
sudo systemctl start iptv-manager

# Manual
pip3 install flask requests
python3 series_manager_web.py
```

---

## Requirements | المتطلبات

| Component | Purpose | Required |
|-----------|---------|----------|
| **Python 3.10+** | Core runtime | Yes |
| **Flask** | Web server | Yes |
| **aria2c** | Fast multi-connection downloads | Yes |
| **TMDB API Key** | Movie/series metadata & posters | Optional (recommended) |
| **OMDb API Key** | IMDb ratings & additional data | Optional (recommended) |

---

## How It Works | كيف يعمل

```
┌─────────────────┐     ┌──────────────┐     ┌────────────────┐
│   IPTV Provider  │────>│   Auto Sync  │────>│  TMDB / OMDb   │
│  (Series + VOD)  │     │  (Discover)  │     │  (Enrich Data) │
└─────────────────┘     └──────────────┘     └────────────────┘
                                                      │
                              ┌────────────────────────┘
                              ▼
                    ┌──────────────────┐
                    │  Smart Filters   │
                    │  (Year, Rating,  │
                    │   Country, etc.) │
                    └──────────────────┘
                              │
              ┌───────────────┼───────────────┐
              ▼               ▼               ▼
     ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
     │   Pending    │ │   Excluded   │ │  Excluded    │
     │  (Review)    │ │  (Filtered)  │ │  but Rich    │
     └──────────────┘ └──────────────┘ └──────────────┘
              │
     ┌────────┼────────┐
     ▼        ▼        ▼
  Accept   Reject   Watched
     │
     ▼
┌──────────────┐     ┌──────────────┐
│   aria2c     │────>│    Plex      │
│  (Download)  │     │   (Watch!)   │
└──────────────┘     └──────────────┘
```

---

## Keyboard Shortcuts | اختصارات لوحة المفاتيح

| Key | Action |
|-----|--------|
| `S` or `/` | Focus search bar |
| `1` - `9` | Switch to section 1-9 |
| `Escape` | Close any open modal or blur input |

---

## API Reference | مرجع الـ API

<details>
<summary><strong>Click to expand full API list (40+ endpoints)</strong></summary>

### Data & Decisions
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/series` | All sections, series data, and decisions |
| GET | `/api/series/hash` | Lightweight polling (MD5 hash) |
| POST | `/api/series/{id}/accept` | Accept a series/movie |
| POST | `/api/series/{id}/reject` | Reject a series/movie |
| POST | `/api/series/{id}/watched_removed` | Mark as watched + delete files |
| GET | `/api/series/{id}/episodes` | Live episode list from IPTV |

### Section Management
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/sections` | Add new section |
| POST | `/api/sections/{id}/toggle` | Enable/disable section |
| POST | `/api/sections/{id}/update` | Edit section settings |
| POST | `/api/sections/{id}/add_category` | Add IPTV category |
| POST | `/api/sections/{id}/remove_category` | Remove IPTV category |
| GET | `/api/sections/{id}/delete_info` | Preview deletion cascade |
| POST | `/api/sections/{id}/delete` | Delete section with cascade |

### Settings
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/settings` | Get all settings |
| POST | `/api/settings` | Save settings |
| POST | `/api/settings/excluded_countries` | Update excluded countries |
| POST | `/api/settings/excluded_genres` | Update excluded genres |
| POST | `/api/settings/excluded_languages` | Update excluded languages |
| POST | `/api/settings/excluded_keywords` | Update banned keywords |
| POST | `/api/settings/pre_rejected_keywords` | Update pre-rejected keywords |
| POST | `/api/settings/section_filter` | Update section filters |

### System Control
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/sys/kill` | Kill all processes |
| POST | `/api/sys/stop_dl` | Stop downloads only |
| POST | `/api/sys/start_dl` | Start downloads |
| POST | `/api/sys/sync` | Start sync |
| POST | `/api/sys/sync_section` | Sync single section |
| POST | `/api/sys/integrity` | Run integrity check |

### Logs & Stats
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/logs` | Last 10 lines sync + download |
| GET | `/api/log` | Last N lines by type |
| GET | `/api/logs/full` | Up to 500 rows by source |
| GET | `/api/stats` | System statistics |
| GET | `/api/bandwidth` | Download bandwidth (day/week/month) |
| GET | `/api/disk_usage` | Per-section disk usage |

### Backups
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/backups` | List all backups |
| POST | `/api/backups/create` | Create manual backup |
| POST | `/api/backups/restore` | Restore from backup |
| POST | `/api/backups/delete` | Delete a backup |
| GET | `/api/backups/download/{name}` | Download backup file |
| POST | `/api/backups/upload` | Upload and restore from file |

### Browse & Categories
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/categories` | All IPTV categories |
| GET | `/api/browse/{section_id}` | Browse section content |
| GET | `/api/browse-path` | Directory tree browser |
| GET | `/api/download-folders` | List download folders |

</details>

---

## Tech Stack | التقنيات

| Layer | Technology |
|-------|-----------|
| **Backend** | Python 3 + Flask |
| **Database** | SQLite (via `db.py` abstraction layer) |
| **Frontend** | Vanilla JS + CSS3 (no frameworks, single-file embedded) |
| **Downloads** | aria2c (multi-connection, resume support) |
| **Metadata** | TMDB API + OMDb API |
| **Push** | Web Push (VAPID) via `pywebpush` |
| **Compression** | Gzip for all JSON responses > 1KB |
| **SSL** | mkcert for local HTTPS |
| **System Tray** | pystray + Pillow (Windows) |

---

## Support | الدعم

If you find this project useful, consider supporting its development:

<p align="center">
  <a href="https://www.paypal.com/ncp/payment/GYPXYRC3MJ85C">
    <img src="https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal&logoColor=white" alt="Donate via PayPal" height="40">
  </a>
</p>

---

## License

MIT License - Free to use and modify.

---

<p align="center">
  <sub>Built with passion for a better viewing experience</sub>
</p>
