# IPTV Manager

**Smart IPTV content manager — browse what's new, pick what you want, download automatically, and watch on Plex with full control.**

**مدير IPTV ذكي — تصفح الجديد، اختار اللي عايزه، التحميل أوتوماتيك، وشاهد على Plex بتحكم كامل.**

---

## Why? | ليه؟

After subscribing to multiple IPTV services, the experience was frustrating:
- Constant buffering and interruptions due to network or server quality
- No thumbnails when seeking through a video
- No resume, no watch history, no proper media management

**Plex solves all of this** — smooth playback, thumbnails, resume, multi-device sync. The idea was simple: browse everything new on IPTV, pick only what I want, download it automatically, and enjoy watching on Plex.

---

بعد الاشتراك في أكتر من IPTV، التجربة كانت محبطة:
- تقطيع مستمر بسبب جودة النت أو السيرفرات
- مفيش صور أثناء التنقل للأمام في الفيديو
- مفيش استكمال، مفيش تاريخ مشاهدة، مفيش إدارة محتوى حقيقية

**Plex بيحل كل ده** — مشاهدة سلسة، صور مصغرة، استكمال، مزامنة بين الأجهزة. الفكرة بسيطة: أتصفح كل جديد في الـ IPTV، أختار اللي أحتاجه بس، يتحمّل أوتوماتيك، وأشاهد بحرية على Plex.

---

## Features | المميزات

### Core | الأساسي
- **Web Dashboard** — Modern dark-themed responsive UI | داشبورد ويب حديث متجاوب
- **PWA Support** — Install as app on mobile/desktop with push notifications | تطبيق ويب تقدر تسطّبه على الموبايل والديسكتوب مع إشعارات
- **Multi-Section** — Organize by category (Arabic, Turkish, English, Movies, etc.) | أقسام متعددة حسب النوع
- **Accept/Reject** — Review each title, accept what you want, reject the rest | راجع كل عنوان، وافق أو ارفض

### Discovery & Metadata | الاكتشاف والبيانات
- **Auto-Sync** — Discovers new series/movies from your IPTV provider automatically | اكتشاف تلقائي من مزود الـ IPTV
- **TMDB + OMDb** — Fetches ratings, posters, genres, countries, and more | بيانات كاملة من TMDB و OMDb
- **IMDb Watchlist** — Auto-accept titles from your IMDb watchlist | موافقة تلقائية من قائمة مشاهدتك في IMDb
- **Smart Filters** — Auto-exclude by rating, votes, region, language, genre | فلاتر ذكية للاستبعاد التلقائي

### Downloads | التحميل
- **aria2c Engine** — Fast multi-connection downloads with resume support | محرك تحميل سريع مع استكمال
- **Progress Bar** — Real-time terminal progress with speed in Mb/s | بروجرس بار لحظي بالسرعة
- **Integrity Check** — Verifies downloaded files, resumes partial downloads | فحص سلامة الملفات
- **Daily Limits** — Configurable daily download limits | حد تحميل يومي قابل للتعديل

### Management | الإدارة
- **Excluded but Rich** — Highlights high-quality excluded titles for review | عرض العناوين المستبعدة عالية الجودة
- **Browse Folders** — Visual folder picker for download directories | اختيار مجلدات التحميل بالتصفح
- **Backup & Restore** — Automatic daily backups with restore capability | نسخ احتياطي يومي تلقائي مع استرجاع
- **Settings Panel** — Full control: IPTV, APIs, filters, exclusions, banned keywords | لوحة إعدادات شاملة
- **Statistics** — Dashboard stats, disk usage per section | إحصائيات واستهلاك القرص

### Platform Support | المنصات
- **Windows** — Setup wizard + system tray + auto-update + watchdog | معالج تسطيب + أيقونة النظام + تحديث تلقائي
- **macOS** — Native .app bundle with menu bar | تطبيق macOS أصلي
- **Linux** — .deb / .rpm packages with systemd service | حزم لينكس مع خدمة systemd
- **Auto-Update** — Windows clients auto-update from GitHub releases | تحديث تلقائي للويندوز من GitHub

---

## Installation | التسطيب

### Windows

1. Download `IPTV_Manager_Windows.zip` from [Releases](../../releases/latest)
2. Extract and right-click `IPTV_Manager_Setup.bat` → **Run as Administrator**
3. Follow the setup wizard (IPTV credentials + optional API keys)
4. The system tray icon appears — double-click to open Dashboard

### macOS

1. Download `.zip` from [Releases](../../releases/latest)
2. Extract and move `IPTV Manager.app` to Applications
3. Launch from Applications — menu bar icon appears
4. Open `https://localhost:8888` in your browser

### Linux

```bash
# Ubuntu/Debian
sudo dpkg -i iptv-manager_*.deb
sudo systemctl start iptv-manager

# AlmaLinux/RHEL
sudo rpm -i iptv-manager-*.rpm
sudo systemctl start iptv-manager

# Or manual:
pip3 install flask requests
python3 series_manager_web.py
```

---

## Requirements | المتطلبات

| Component | Purpose | مطلوب |
|-----------|---------|-------|
| Python 3.10+ | Core runtime | نعم |
| Flask | Web server | نعم |
| aria2c | Fast downloads | نعم |
| TMDB API key | Metadata & posters | اختياري |
| OMDb API key | Ratings | اختياري |

---

## License
MIT License - Free to use and modify.
