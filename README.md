<div align="center">

# IPTV Manager

### A Complete IPTV Series & Movies Management System

[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-blue?style=for-the-badge)]()
[![Python](https://img.shields.io/badge/Python-3.10+-green?style=for-the-badge&logo=python&logoColor=white)]()
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)]()
[![Auto Update](https://img.shields.io/badge/Auto%20Update-Enabled-brightgreen?style=for-the-badge)]()

**Automatically discovers, organizes, and downloads series & movies from your IPTV provider with a beautiful dark-themed web dashboard.**

</div>

---

## Features

| Feature | Description |
|---------|-------------|
| **Web Dashboard** | Modern dark-themed UI with movie posters, ratings, and metadata |
| **Auto-Discovery** | Automatically finds new series and movies from your IPTV provider |
| **Smart Downloads** | Downloads new episodes automatically via aria2c (16 connections) |
| **Metadata & Posters** | Fetches covers, ratings, and info from TMDB and OMDb APIs |
| **Accept/Reject System** | Review content and decide what to download |
| **Multi-Section Support** | Organize by categories: Arabic, Turkish, English, Ramadan, etc. |
| **Auto-Update** | Windows/Linux installs auto-update from this repo every 5 minutes |
| **System Tray (Windows)** | Tray icon with server controls, watchdog, and auto-restart |
| **Push Notifications** | Browser notifications when downloads complete (PWA) |
| **Search & Filter** | Search by name or genre, filter by status (Pending/Accepted/Rejected) |
| **Download Monitor** | Real-time sync and download logs with progress tracking |
| **IMDB Integration** | Import watchlist from IMDB for automatic matching |

---

## Dashboard Preview

The dashboard features a dark-themed interface with:
- **Header**: Logo, navigation buttons (Stats, Logs, System, Settings)
- **Live Logs**: Real-time sync and download status panels
- **Section Tabs**: Switch between content categories with item counts
- **Status Filters**: Pending, Accepted, Rejected, Watched, Excluded
- **Movie Grid**: Poster cards with ratings, genres, country info, and IMDB badges
- **Search Bar**: Filter content by name or genre

---

## Installation

### Windows (Recommended)

1. Download `IPTV_Manager_Windows.zip` from [**Latest Release**](../../releases/latest)
2. Extract and right-click `IPTV_Manager_Setup.bat` > **Run as Administrator**
3. Follow the setup wizard:

| Step | Description |
|------|-------------|
| **Welcome** | Click "Start Setup" |
| **IPTV Account** | Enter username, password, and server URL |
| **API Keys** | Enter TMDB and OMDb keys (optional - can add later) |
| **Install** | Automatic: installs packages, configures firewall, sets up auto-start |
| **Done** | Click "Launch Dashboard" |

#### After Installation
- A **system tray icon** appears next to the clock
- **Green circle** = Server running | **Red circle** = Server stopped
- **Double-click** tray icon to open dashboard
- **Right-click** for menu: Start/Stop/Restart, Settings, Watchdog toggle
- **Watchdog** auto-restarts the server if it crashes
- **Auto-start** with Windows via startup entry

#### Auto-Updates
The installation checks this GitHub repo every 5 minutes. New releases are downloaded and applied automatically - no user action needed.

---

### Linux

1. Download `IPTV_Manager_Linux.zip` from [**Latest Release**](../../releases/latest)
2. Extract and run:

```bash
cd IPTV_Manager
chmod +x setup.sh
./setup.sh
```

---

### macOS

```bash
cd /path/to/IPTV_Manager
pip3 install flask requests
python3 series_manager_web.py
# Open https://localhost:8888
```

---

## Requirements

| Component | Purpose | Auto-Install |
|-----------|---------|:---:|
| Python 3.10+ | Core runtime | Windows: Yes |
| Flask | Web server | Yes |
| requests | HTTP client | Yes |
| aria2c | Fast multi-connection downloads | Windows: Yes |
| pystray + Pillow | System tray icon (Windows) | Yes |
| TMDB API key | Movie/series metadata | Manual |
| OMDb API key | Ratings and extra info | Manual |

---

## Project Structure

```
IPTV Manager/
|-- series_manager_web.py    # Main web server + dashboard
|-- series_manager_sync.py   # IPTV catalog sync engine
|-- iptv_downloader.py       # Episode/movie downloader (aria2c)
|-- db.py                    # SQLite database layer (WAL mode)
|-- setup_gui.pyw            # Windows setup wizard (tkinter)
|-- tray_manager.pyw         # Windows system tray + watchdog
|-- fix_covers.py            # Cover image repair utility
|-- fix_missing_covers.py    # Missing poster fetcher
|-- repair_posters.py        # Poster validation & repair
|-- refresh_omdb_data.py     # OMDb metadata refresher
|-- iptv_manager.db          # SQLite database (auto-created)
|-- pwa-icon-192.png         # PWA icon
|-- favicon.ico              # Browser favicon
+-- sw.js                    # Service Worker for notifications
```

---

## How It Works

1. **Sync**: Connects to your IPTV provider and discovers all available series/movies
2. **Organize**: Groups content by sections (Arabic, English, Turkish, etc.)
3. **Review**: You accept or reject content through the dashboard
4. **Download**: Accepted content is automatically downloaded via aria2c
5. **Monitor**: Real-time progress in the dashboard with download/sync logs
6. **Update**: Windows installs auto-update from this GitHub repo

---

## API Keys Setup

### TMDB (The Movie Database)
1. Create account at [themoviedb.org](https://www.themoviedb.org/)
2. Go to Settings > API > Create > Developer
3. Copy the **Bearer Token** (starts with `eyJ...`)

### OMDb
1. Get a free key at [omdbapi.com/apikey.aspx](https://www.omdbapi.com/apikey.aspx)
2. Check your email for the API key

---

---

<div dir="rtl">

# IPTV Manager - عربي

### نظام إدارة IPTV كامل لتحميل المسلسلات والأفلام أوتوماتيك

---

## المميزات

| الميزة | الوصف |
|--------|-------|
| **داشبورد ويب** | واجهة حديثة وأنيقة مع بوسترات وتقييمات ومعلومات |
| **اكتشاف تلقائي** | يلاقي المسلسلات والأفلام الجديدة أوتوماتيك |
| **تحميل ذكي** | يحمّل الحلقات الجديدة أوتوماتيك (16 اتصال متزامن) |
| **بيانات وبوسترات** | يجيب الأغلفة والتقييمات من TMDB و OMDb |
| **قبول/رفض** | راجع المحتوى وقرر إيه اللي يتحمّل |
| **أقسام متعددة** | عربي، تركي، إنجليزي، رمضان، أفلام عربي |
| **تحديث تلقائي** | بيتحدث من GitHub كل 5 دقائق |
| **أيقونة جمب الساعة** | تحكم كامل في السيرفر + مراقبة تلقائية |
| **إشعارات** | تنبيهات لما يخلص تحميل |

---

## التسطيب (ويندوز)

1. حمّل `IPTV_Manager_Windows.zip` من [**آخر إصدار**](../../releases/latest)
2. فك الضغط واعمل كليك يمين على `IPTV_Manager_Setup.bat` > **تشغيل كمسؤول**
3. اتبع المعالج:

| الخطوة | المطلوب |
|--------|---------|
| **ترحيب** | دوس "Start Setup" |
| **حساب IPTV** | حط اسم المستخدم وكلمة المرور ورابط السيرفر |
| **مفاتيح API** | حط مفاتيح TMDB و OMDb (اختياري) |
| **تسطيب** | أوتوماتيك - بيسطب كل حاجة |
| **تم** | دوس "Launch Dashboard" |

### بعد التسطيب
- أيقونة بتظهر **جمب الساعة**
- **أخضر** = شغال | **أحمر** = واقف
- **دبل كليك** = فتح الداشبورد
- **كليك يمين** = تشغيل / إيقاف / إعادة تشغيل / إعدادات
- **المراقب** بيعيد تشغيل السيرفر لو وقع
- **بيشتغل أوتوماتيك** مع تشغيل الويندوز

### التحديث التلقائي
النسخة بتتشيك على GitHub كل 5 دقائق. لو في تحديث جديد بيتحمّل ويتطبّق لوحده.

---

## التسطيب (لينكس)

```bash
cd IPTV_Manager
chmod +x setup.sh
./setup.sh
```

---

## التسطيب (ماك)

```bash
pip3 install flask requests
python3 series_manager_web.py
# افتح https://localhost:8888
```

</div>

---

## License

MIT License - Free to use and modify.
