<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/01-dashboard-main.jpg" alt="IPTV Manager Dashboard" width="100%">
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
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker" alt="Docker">
  <img src="https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/HTTPS-Auto--SSL-green?style=flat-square&logo=letsencrypt" alt="HTTPS">
  <img src="https://img.shields.io/badge/PWA-Supported-orange?style=flat-square" alt="PWA">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">
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

## Quick Start | البداية السريعة

```bash
# One command to run on any OS
docker run -d \
  --name iptv-manager \
  --restart unless-stopped \
  -p 443:443 \
  -v iptv-data:/app/data \
  -v /path/to/your/media:/media \
  -e TZ=Africa/Cairo \
  iptv-manager

# Open: https://iptv.local
```

**Windows?** Download and run [`setup-docker.bat`](../../releases/latest) — it does everything for you.

---

## Screenshots | صور الشاشة

### Dashboard — لوحة التحكم
The main interface where you browse, review, and manage all your content. Sections organized as tabs with item counts, status filters, and sorting options.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/01-dashboard-main.jpg" alt="Dashboard" width="100%">
</p>

### Accept / Reject — قبول / رفض
Hover over any card to see action buttons. One click to accept for download or reject.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/02-accept-reject.jpg" alt="Accept Reject" width="100%">
</p>

### Statistics Panel — لوحة الإحصائيات
Full system statistics: total series tracked, decisions made, downloads completed, bandwidth usage (daily/weekly/monthly), and a 14-day download chart.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/03-statistics.jpg" alt="Statistics" width="80%">
</p>

### Excluded Tab — تاب المستبعد
Every auto-excluded item shows the reason it was filtered (low rating, low votes, region, genre, language, banned keyword). Nothing disappears — everything is traceable.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/04-excluded-tab.jpg" alt="Excluded Tab" width="100%">
</p>

### Exclusion Rules — قواعد الاستبعاد
Add countries, genres, or languages to the exclusion list. Items matching these rules are automatically filtered out.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/05-exclusions.jpg" alt="Exclusions" width="100%">
</p>

### Section Rules — قواعد لكل قسم
Set banned keywords per section to auto-exclude or auto-reject matching titles. Retroactively applies to all existing pending items.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/06-section-rules.jpg" alt="Section Rules" width="100%">
</p>

### Backup & Restore — النسخ الاحتياطي والاسترجاع
Automatic daily backups with full restore capability. Download, upload, or restore any backup with one click.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/07-backups.jpg" alt="Backups" width="100%">
</p>

### Database Browser — متصفح قاعدة البيانات
Built-in phpMyAdmin-style database browser. View all tables, row counts, run SQL queries, maintenance, and repair covers.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/08-database-browser.jpg" alt="Database Browser" width="100%">
</p>

### Global Search — البحث الشامل
Search across ALL sections by title. Results grouped by section with thumbnails, ratings, and status badges.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/09-search.jpg" alt="Search" width="100%">
</p>

### Mobile PWA — تطبيق الموبايل
Fully responsive design that works as a Progressive Web App. Install it on your phone's home screen for a native app experience with push notifications.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/10-mobile.jpg" alt="Mobile View" width="300">
</p>

### Section Filters — فلاتر الأقسام
Per-section min year, min rating, and min vote count. Fine-tune what gets through the auto-filter for each section independently.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/11-section-filters.jpg" alt="Section Filters" width="100%">
</p>

### Live Logs — السجلات المباشرة
Real-time sync and download logs with progress bars. Monitor what's happening right now — sync enrichment, download speed, file status.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/12-live-logs.jpg" alt="Live Logs" width="100%">
</p>

### Kill All — إيقاف كل العمليات
Emergency stop for all running downloads and sync operations. Confirms before killing to prevent accidental interruption.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/13-kill-all.jpg" alt="Kill All" width="100%">
</p>

### Live Status — حالة السيستم
Live dashboard showing sync progress, download queue, active jobs, and system health in real-time.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/14-live-status.jpg" alt="Live Status" width="100%">
</p>

### Bandwidth Statistics — إحصائيات الباندويدث
Track download volume: today, this week, this month. 14-day bar chart with per-day breakdown.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/15-bandwidth-stats.jpg" alt="Bandwidth Stats" width="80%">
</p>

### Filter Breakdown — تفصيل الفلاتر
See exactly how many items are in each status (pending, accepted, rejected, excluded) per section. Understand your filter pipeline at a glance.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/16-filter-breakdown.jpg" alt="Filter Breakdown" width="80%">
</p>

### Accept Dialog — نافذة القبول
When accepting a series, choose exactly what to download: Everything (all episodes), New only (future episodes), or Custom range (pick season & episode). Shows total episode count per season.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/17-accept-dialog.jpg" alt="Accept Dialog" width="80%">
</p>

### Add Section — إضافة قسم جديد
Create new content sections with IPTV category IDs, download folder, and custom filters. Visual folder picker — no manual path typing needed.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/18-add-section.jpg" alt="Add Section" width="80%">
</p>

### Section Settings — إعدادات القسم
Edit section name, manage IPTV categories, change download folder, toggle strict filters. Quick access from the gear icon on the dashboard.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/19-section-settings.jpg" alt="Section Settings" width="100%">
</p>

### Dark Mode — الوضع الليلي
Full dark theme that auto-switches at night (6pm-6am). Manual toggle with the theme button. Saves preference in localStorage.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/20-dark-mode.jpg" alt="Dark Mode" width="100%">
</p>

### Light Mode — الوضع النهاري
Clean light theme for daytime use. All UI elements, cards, and modals adapt to the current theme.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/21-light-mode.jpg" alt="Light Mode" width="100%">
</p>

### Download Settings — إعدادات التحميل
Configure download root folder, aria2c connections (parallel download streams), daily download limit, trash folder location, and auto-restart on slow speed.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/22-settings-download.jpg" alt="Download Settings" width="100%">
</p>

### Advanced Settings — إعدادات متقدمة
GitHub auto-update configuration, VAPID keys for push notifications, remote control password, and publish settings.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/23-settings-advanced.jpg" alt="Advanced Settings" width="100%">
</p>

### Browse & Exclude — تصفح واستبعد
Browse all content from your IPTV provider visually. Reject items directly from the browse view without waiting for sync.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/24-browse-exclude.jpg" alt="Browse & Exclude" width="100%">
</p>

---

## Architecture | البنية

```
┌──────────────────────────────────────────┐
│         Docker Container (Alpine)        │
│                                          │
│  ┌──────────────┐  ┌──────────────────┐  │
│  │  Cheroot      │  │   dcron          │  │
│  │  HTTPS :443   │  │  sync/dl/check   │  │
│  │  (auto-SSL)   │  │  (Alpine cron)   │  │
│  └──────────────┘  └──────────────────┘  │
│                                          │
│  /app         (code — read-only layer)   │
│  /app/data    (DB, covers, certs)  ← VOL │
│  /media       (download target)    ← MNT │
└──────────────────────────────────────────┘

Access: https://iptv.local  (mDNS — no hosts file needed)
```

| Component | Technology |
|-----------|-----------|
| **Runtime** | Docker (Alpine Linux + Python 3.12) |
| **Web Server** | Cheroot WSGI (native SSL, thread-pooled) |
| **Framework** | Flask |
| **Database** | SQLite (normalized v2 schema) |
| **Downloads** | aria2c (multi-connection, resume, 40 MB/s+) |
| **Metadata** | TMDB API + OMDb API |
| **Push** | Web Push (VAPID) via pywebpush |
| **Discovery** | mDNS (iptv.local — zero-config LAN access) |
| **Frontend** | Vanilla JS + CSS3 (no frameworks) |
| **Compression** | Pre-gzipped static files (75% smaller) |

---

## Features | المميزات

### Dashboard & UI | لوحة التحكم

| Feature | Description |
|---------|-------------|
| **Web Dashboard** | Modern responsive UI with light/dark theme (auto switches day/night) |
| **PWA Support** | Install as native app on mobile/desktop with push notifications |
| **Global Search** | Search across all sections by title — results grouped by section |
| **Multi-Section Tabs** | Organize content by category (English Movies, Foreign Series, Turkish, Ramadan, Arabic, etc.) |
| **5 Status Tabs** | Pending, Accepted, Rejected, Excluded — each with item count badge |
| **Sort & Filter** | Sort by newest, highest rated. Filter by genre, country |
| **Grid / List View** | Toggle between card grid and compact list |
| **Keyboard Shortcuts** | `S` to search, `1-9` to switch sections, `Esc` to close |
| **New Items Badge** | Pulsing gold dot on section tabs when new pending items appear |
| **Section Settings Gear** | Quick-edit section name, categories, download folder from dashboard |

### Content Cards | بطاقات المحتوى

| Feature | Description |
|---------|-------------|
| **IMDb Rating Badge** | Color-coded IMDb rating on every card (links to IMDb page) |
| **Vote Count** | Formatted vote count (e.g. 36.7K, 1.2M) |
| **Genres & Country** | Full metadata under each title |
| **Exclusion Reason** | Clear badge showing why an item was auto-excluded |
| **Accept / Reject** | One-click action buttons on card hover |
| **Episode Picker** | For series: choose starting season & episode from live dropdown |
| **Accept Modes** | **Everything** (all episodes), **New only** (future), **Custom** (pick range S01E01-S03E05) |
| **Force Accept** | Override filters and accept excluded items manually |
| **Reject Group** | Reject all duplicate/sibling entries at once |
| **Groups Only** | Choose which IPTV variant/quality version to download |

### Smart Filters | الفلاتر الذكية

| Filter | Description |
|--------|-------------|
| **Year Filter** | Minimum release year per section |
| **Rating Filter** | Minimum IMDb rating threshold per section |
| **Vote Count Filter** | Minimum vote count to filter unknown titles |
| **Country Exclusion** | Auto-exclude content from specific countries |
| **Genre Exclusion** | Auto-exclude specific genres (Animation, Documentary, etc.) |
| **Language Exclusion** | Auto-exclude by language ISO code |
| **Banned Keywords** | Per-section auto-exclude titles containing specific words |
| **Pre-Rejected Keywords** | Auto-reject (stronger than exclude) per section |
| **Arabic Detection** | In English sections: auto-excludes titles with >30% Arabic chars |
| **Stale Series** | Auto-excludes series with no new episodes in N days |
| **Retroactive Apply** | New exclusion rules immediately apply to all pending items |

### Discovery & Metadata | الاكتشاف والبيانات

| Feature | Description |
|---------|-------------|
| **Auto-Sync** | Discovers new series/movies from IPTV provider every 6 hours |
| **TMDB Integration** | Fetches ratings, posters, genres, countries, release dates |
| **OMDb / IMDb** | Cross-references for IMDb ratings and additional data |
| **IMDb Watchlist** | Auto-marks titles from your IMDb watchlist (public URL or CSV) |
| **Cover Downloads** | Auto-downloads and caches high-quality posters + thumbnails |
| **Duplicate Detection** | Keeps 4K version when both 4K and SD exist |
| **Push Notifications** | Get notified when new series are added or downloads complete |

### Download Manager | مدير التحميل

| Feature | Description |
|---------|-------------|
| **aria2c Engine** | Fast multi-connection downloads with automatic resume |
| **aria2c Connections** | Configurable parallel connections per download (default 16) |
| **Smart Scheduling** | Automatic download every 40 minutes via cron |
| **Dashboard Controls** | Start / Stop / Kill All buttons in toolbar |
| **Auto-Restart** | Automatically restarts downloads that stall below speed threshold |
| **Integrity Check** | Every 12 hours — verifies files, resumes partials, detects corruption |
| **Bandwidth Tracking** | Daily, weekly, monthly volume with 14-day chart |
| **Season/Episode Filter** | Download only chosen ranges (e.g. Season 3+ or S5E1-E5) |
| **Variant Selection** | Pick preferred quality when duplicates exist |
| **Trash Folder** | Deleted media goes to configurable trash before permanent removal |
| **Download Root** | Parent folder containing all section media folders |

### Monitoring & Logs | المراقبة والسجلات

| Feature | Description |
|---------|-------------|
| **Live Logs** | Real-time sync & download logs with auto-scroll |
| **Sync Progress** | Stage-by-stage sync status (fetching, enriching, filtering, saving) |
| **Download Progress** | Speed, size, ETA, and visual progress bar per file |
| **Full Log Export** | Export all logs as JSON (up to 500 lines per source) |
| **System Statistics** | Total series, decisions, downloads, bandwidth, DB size |
| **Bandwidth Charts** | 14-day download chart + today/week/month breakdown |
| **Filter Breakdown** | Per-section count of pending/accepted/rejected/excluded items |
| **Disk Usage** | Per-section folder size on disk |
| **Smart Polling** | Fast polling when active, slow when idle, paused when tab hidden |

### Theme System | نظام المظهر

| Feature | Description |
|---------|-------------|
| **Auto Mode** | Light during day (6am-6pm), dark at night — automatic |
| **Manual Toggle** | Click theme button to cycle: Auto → Dark → Light |
| **Full Coverage** | All cards, modals, settings, and pages adapt to theme |
| **Persistence** | Theme preference saved in localStorage |

### Settings Panel | لوحة الإعدادات

| Tab | What it controls |
|-----|-----------------|
| **General** | IPTV connection, API keys (TMDB/OMDb), download root, IMDb watchlist |
| **Exclusions** | Global excluded countries, genres, languages with tag UI |
| **Section Filters** | Per-section min year, min rating, min vote count |
| **Section Rules** | Per-section banned keywords and pre-rejected keywords |
| **Browse & Exclude** | Browse all IPTV content visually and reject directly |
| **Backups** | Create, restore, upload, download, delete backups |
| **Database** | phpMyAdmin-style browser, maintenance, SQL query, repair covers |

### Backup System | نظام النسخ الاحتياطي

| Feature | Description |
|---------|-------------|
| **Automatic Daily** | Background cron creates one backup per day |
| **Manual Backup** | Create instant backups with one click |
| **Restore** | Restore any previous backup (safety backup created first) |
| **Upload & Restore** | Upload a `.db` file from your computer |
| **Download** | Download any backup file to your computer |
| **Auto-Retention** | Keeps last 3 backups, deletes older ones |

### Remote Control | التحكم عن بعد

| Feature | Description |
|---------|-------------|
| **Password Protected** | Separate password for remote access |
| **24h Token** | Auth tokens expire after 24 hours |
| **Pending List** | View and approve/reject items remotely |
| **Download Control** | Start/stop downloader from any device |
| **CORS Enabled** | Safe cross-origin access from external pages |

### Security | الأمان

| Feature | Description |
|---------|-------------|
| **HTTPS Only** | Auto-generated SSL certificate (valid 10 years) |
| **Local CA** | Install root CA on devices for green lock (no browser warnings) |
| **Credential Scanning** | Publish blocks if secrets detected in code |
| **Parameterized SQL** | All queries use parameters (no injection) |
| **Path Validation** | Backup names, file paths validated against traversal |
| **Token Expiry** | Remote tokens expire after 24h |

---

## Installation | التسطيب

### Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Windows/macOS) or Docker Engine (Linux)
- A media/download folder on your disk

### Windows (One-Click)

```
1. Install Docker Desktop from docker.com
2. Download setup-docker.bat from Releases
3. Right-click → Run as Administrator
4. Enter your media folder path (e.g. D:\Media)
5. Done! Open https://iptv.local
```

The setup script:
- Pulls the Docker image
- Creates a persistent data volume
- Starts the container with auto-restart
- Auto-migrates data from old native installations
- Cleans old startup entries and processes

### macOS

```bash
# Install Docker Desktop from docker.com, then:
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 \
  -v iptv-data:/app/data \
  -v /Volumes/YourDisk/Media:/media \
  -e TZ=Africa/Cairo \
  iptv-manager
```

### Linux

```bash
# Install Docker
curl -fsSL https://get.docker.com | sh
sudo usermod -aG docker $USER && newgrp docker

# Run
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 \
  -v iptv-data:/app/data \
  -v /mnt/media:/media \
  -e TZ=Africa/Cairo \
  iptv-manager
```

### Docker Compose

```yaml
services:
  iptv-manager:
    image: iptv-manager:latest
    container_name: iptv-manager
    restart: unless-stopped
    ports:
      - "443:443"
    volumes:
      - iptv-data:/app/data
      - /path/to/your/media:/media   # CHANGE THIS
    environment:
      - TZ=Africa/Cairo

volumes:
  iptv-data:
```

### First Run

1. Open **https://iptv.local** in your browser
2. Accept the self-signed certificate warning (one-time)
3. Go to **Settings** → enter your IPTV credentials
4. (Optional) Add TMDB/OMDb API keys for richer metadata
5. Create sections → assign IPTV categories → set download folders
6. Click **Sync** → new content appears in Pending tab
7. Accept what you want → downloads start automatically

---

## iPhone / iPad — Install CA Certificate | تركيب الشهادة

To get the green lock (no "Not Secure" warning):

1. Open **Safari** (not Chrome — iOS ignores certs from Chrome)
2. Go to `https://iptv.local/install-ca`
3. Tap **Allow** to download the profile
4. Go to **Settings → General → VPN & Device Management**
5. Find **IPTV Manager CA** → tap **Install**
6. Go to **Settings → General → About → Certificate Trust Settings**
7. Enable **IPTV Manager CA**
8. Go back to Safari → open `https://iptv.local` → green lock!

---

## Docker Details | تفاصيل الدوكر

### Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `TZ` | `UTC` | Timezone (e.g. `Africa/Cairo`, `America/New_York`) |
| `IPTV_DATA_DIR` | `/app/data` | Data directory inside container |
| `PORT` | `443` | HTTPS port |

### Cron Jobs (Automatic)

| Schedule | Job | Description |
|----------|-----|-------------|
| Every 40 min | `iptv_downloader.py` | Download accepted series |
| Every 6 hours | `series_manager_sync.py` | Sync new content from IPTV API |
| Every 12 hours | `iptv_downloader.py --check` | File integrity verification |
| Daily midnight | Backup | Auto-backup database |

### Volumes

| Mount | Purpose |
|-------|---------|
| `iptv-data:/app/data` | Persistent: DB, covers, certs, backups, logs, trash |
| `/path/to/media:/media` | Your media disk for downloads |

### Health Check

```
Interval: 30s | Timeout: 5s | Retries: 3
Endpoint: https://localhost:443/api/series/hash
```

### Auto-SSL

On first start, the container automatically:
1. Generates a local **Root CA** (`rootCA.pem`)
2. Signs a server certificate (valid 10 years)
3. Serves the CA at `/install-ca` for device trust
4. All traffic is HTTPS — no HTTP

### mDNS Discovery

The container advertises itself as **iptv.local** on your LAN via mDNS. No `/etc/hosts` editing needed. Works on:
- macOS (built-in Bonjour)
- iOS (built-in)
- Windows (if Bonjour/iTunes installed)
- Linux (if avahi-daemon running)

---

## How It Works | كيف يعمل

```
┌─────────────────┐     ┌──────────────┐     ┌────────────────┐
│   IPTV Provider  │────>│   Auto Sync  │────>│  TMDB / OMDb   │
│  (Series + VOD)  │     │  (Every 6h)  │     │  (Enrich Data) │
└─────────────────┘     └──────────────┘     └────────────────┘
                                                      │
                              ┌────────────────────────┘
                              ▼
                    ┌──────────────────┐
                    │  Smart Filters   │
                    │  Year, Rating,   │
                    │  Country, Genre  │
                    │  Keywords, Lang  │
                    └──────────────────┘
                              │
              ┌───────────────┼───────────────┐
              ▼               ▼               ▼
     ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
     │   Pending    │ │   Excluded   │ │   Excluded   │
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

## Migration from Old Installation | الترقية من النسخة القديمة

If you have an existing native installation (Windows/macOS/Linux):

**Windows:** Just run `setup-docker.bat` — it auto-detects and migrates your database and covers.

**macOS/Linux:**
```bash
# 1. Copy your data to Docker volume
docker volume create iptv-data
docker run --rm -v iptv-data:/data -v /path/to/old/install:/src alpine sh -c "
    cp /src/iptv_manager.db /data/
    cp -r /src/covers /data/
"

# 2. Start container — paths auto-migrate to /media/*
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 -v iptv-data:/app/data -v /mnt/media:/media iptv-manager
```

The entrypoint automatically converts old paths (e.g. `/Volumes/3TB/Plex/Movies` or `D:\Media\Movies`) to `/media/Movies`.

---

## Keyboard Shortcuts | اختصارات لوحة المفاتيح

| Key | Action |
|-----|--------|
| `S` or `/` | Focus search bar |
| `1` - `9` | Switch to section 1-9 |
| `Escape` | Close any open modal |

---

## API Reference | مرجع الـ API

<details>
<summary><strong>Click to expand full API list (60+ endpoints)</strong></summary>

### Series & Decisions
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/series` | Paginated series list with counts |
| GET | `/api/series/hash` | Lightweight polling (data hash) |
| POST | `/api/series/{id}/accept` | Accept series/movie |
| POST | `/api/series/{id}/reject` | Reject series/movie |
| POST | `/api/series/{id}/watched_removed` | Mark watched + delete files |
| GET | `/api/series/{id}/episodes` | Live episode list from IPTV |
| GET | `/api/series/{id}/siblings` | Duplicate entries |
| POST | `/api/series/{id}/reject_group` | Reject all siblings |

### Sections
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/categories` | All IPTV categories |
| POST | `/api/sections` | Create/update section |
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
| POST | `/api/settings/section_exclusions` | Section-specific rules |
| POST | `/api/settings/section_filter` | Section filters (year/rating/votes) |
| GET | `/api/known_values` | All unique genres/countries/languages |
| GET | `/api/section_breakdown` | Count per status per section |
| GET | `/api/browse-dirs` | File browser |
| POST | `/api/upload-csv` | Bulk import CSV decisions |

### System Control
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/sys/start_dl` | Start downloads |
| POST | `/api/sys/stop_dl` | Pause downloads |
| POST | `/api/sys/kill` | Force-stop all processes |
| POST | `/api/sys/sync` | Full IPTV sync |
| POST | `/api/sys/sync_section` | Sync single section |
| GET | `/api/sys/sync_status` | Current sync progress |
| POST | `/api/sys/integrity` | Run integrity check |
| GET | `/api/sys/status` | Server status |
| POST | `/api/shutdown` | Graceful shutdown |
| POST | `/api/restart-server` | Restart server |

### Logs & Statistics
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/logs` | Last N lines sync + download |
| GET | `/api/logs/full` | Full log export (JSON) |
| GET | `/api/stats` | System statistics |
| GET | `/api/bandwidth` | Download stats (today/week/month) |
| GET | `/api/bandwidth/history` | Daily history (date range) |
| GET | `/api/bandwidth/day` | Detailed day breakdown |
| GET | `/api/disk_usage` | Per-section disk usage |
| GET | `/api/download-folders` | Available download locations |

### Search & Trash
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/search?q=...` | Global search (all sections) |
| GET | `/api/trash` | List trashed items |
| POST | `/api/trash/delete` | Permanently delete |
| POST | `/api/trash/restore` | Restore from trash |
| POST | `/api/repair-covers` | Fix missing covers |

### Backups
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/backups` | List all backups |
| POST | `/api/backups/create` | Create backup now |
| POST | `/api/backups/restore` | Restore from backup |
| POST | `/api/backups/delete` | Delete backup |
| GET | `/api/backups/download/{name}` | Download backup file |
| POST | `/api/backups/upload` | Upload & restore |

### Database Browser
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/db/tables` | List all tables |
| GET | `/api/db/table/{name}` | Paginated table data |
| POST | `/api/db/query` | Execute SQL query |
| POST | `/api/db/row/delete` | Delete row |
| POST | `/api/db/maintenance` | Optimize/vacuum DB |

### Push Notifications
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/push/vapid-key` | Public VAPID key |
| POST | `/api/push/subscribe` | Register device |
| POST | `/api/push/unsubscribe` | Unregister device |
| POST | `/api/push/test` | Send test notification |

### Publishing & Updates
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/publish-update` | Push update to GitHub releases |
| GET | `/api/heartbeat` | Current version hash |
| POST | `/api/check-update` | Check for new version |

### Remote Control
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/remote/auth` | Authenticate (get token) |
| GET | `/api/remote/pending` | Pending items (auth required) |
| POST | `/api/remote/decide` | Accept/reject remotely |
| POST | `/api/remote/download` | Control downloader remotely |

### PWA & Assets
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/covers/{file}` | Cover images |
| GET | `/thumbs/{file}` | Thumbnails (auto-generated) |
| GET | `/manifest.json` | PWA manifest |
| GET | `/sw.js` | Service worker |
| GET | `/install-ca` | Download root CA certificate |

</details>

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
