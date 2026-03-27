<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/01-dashboard-movie-grid.jpg" alt="IPTV Manager Dashboard" width="100%">
</p>

<h1 align="center">IPTV Manager v3.5</h1>

<p align="center">
  <strong>Self-hosted IPTV content manager for Plex &amp; Jellyfin</strong><br>
  Auto-discover new content from your IPTV provider. Accept or reject with one click.<br>
  Downloads run automatically. Watch on Plex with full metadata, thumbnails, and resume.
</p>

<p align="center">
  <strong>مدير IPTV ذكي لـ Plex و Jellyfin</strong><br>
  اكتشاف تلقائي للمحتوى الجديد من مزود IPTV. قبول أو رفض بضغطة واحدة.<br>
  التحميل يعمل أوتوماتيك. شاهد على Plex بـ metadata كاملة وصور مصغرة واستكمال.
</p>

<p align="center">
  <a href="../../releases/latest"><img src="https://img.shields.io/badge/Download-Latest%20Release-gold?style=for-the-badge&logo=github" alt="Download"></a>
  <a href="https://www.paypal.com/ncp/payment/GYPXYRC3MJ85C"><img src="https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal" alt="Donate"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker" alt="Docker">
  <img src="https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/HTTPS-Auto--SSL-green?style=flat-square&logo=letsencrypt" alt="HTTPS">
  <img src="https://img.shields.io/badge/PWA-Installable-orange?style=flat-square" alt="PWA">
  <img src="https://img.shields.io/badge/mDNS-iptv.local-purple?style=flat-square" alt="mDNS">
  <img src="https://img.shields.io/badge/Theme-Auto%20%7C%20Light%20%7C%20Dark-333?style=flat-square" alt="Theme">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">
</p>

---

## The Story | القصة

After subscribing to multiple IPTV services, the experience was frustrating:
- **Constant buffering** and interruptions due to network or server quality
- **No thumbnails** when seeking through a video
- **No resume**, no watch history, no proper media management

**Plex solves all of this** — smooth playback, thumbnails, resume, multi-device sync. The idea: browse everything new on IPTV, pick only what I want, download it automatically, and watch on Plex with full freedom.

---

بعد الاشتراك في أكتر من IPTV، التجربة كانت محبطة:
- **تقطيع مستمر** بسبب جودة النت أو السيرفرات
- **مفيش صور** أثناء التنقل في الفيديو
- **مفيش استكمال**، مفيش تاريخ مشاهدة، مفيش إدارة حقيقية

**Plex بيحل كل ده** — مشاهدة سلسة، صور مصغرة، استكمال، مزامنة بين الأجهزة. الفكرة: أتصفح كل جديد في الـ IPTV، أختار اللي أحتاجه، يتحمّل أوتوماتيك، وأشاهد بحرية على Plex.

---

## Quick Start | البداية السريعة

```bash
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 \
  -v iptv-data:/app/data \
  -v /path/to/media:/media \
  -e TZ=Africa/Cairo \
  iptv-manager

# Open https://iptv.local — zero-config mDNS, no hosts file needed
```

**Windows?** Download [`setup-docker.bat`](../../releases/latest) — auto-installs everything with one click.

---

## Full Feature Tour | جولة كاملة في المميزات

> Every screenshot below is from the real running app. Click any image to enlarge.
>
> كل الصور من التطبيق الفعلي. اضغط على أي صورة لتكبيرها.

---

### 📺 1. Dashboard — Movie & Series Grid | لوحة التحكم — عرض الأفلام والمسلسلات

The main interface. Browse all content organized into customizable sections (English Movies, Foreign Series, Turkish, Ramadan 2026, Arabic Movies, etc.). Each card shows:
- **High-quality poster** auto-downloaded from TMDB
- **IMDb rating badge** (color-coded: green = good, yellow = average, red = low)
- **Vote count** (e.g., 10.4K, 2.8K) — tells you how popular the title is
- **Year**, **genres**, **country** — full metadata at a glance
- **Section categories** — which IPTV source categories feed this section

الواجهة الرئيسية. تصفح كل المحتوى مرتب في أقسام قابلة للتخصيص. كل كارت بيعرض بوستر عالي الجودة من TMDB، تقييم IMDb ملون، عدد الأصوات، السنة، الأنواع، والبلد.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/01-dashboard-movie-grid.jpg" width="100%"></p>

---

### 🔢 2. Status Tabs & Filter Bar | تابات الحالة وشريط الفلاتر

Five status tabs with **live counts** that update in real-time:
- **Pending** (307) — Items waiting for your decision
- **Accepted** (14) — Queued for download
- **Rejected** (132) — Items you skipped
- **Excluded** (10,208) — Auto-filtered by your smart rules

Plus three filter dropdowns: **Sort Order**, **Genre Filter** (with counts), **Country Filter** (with counts).

خمس تابات بأعداد حية: معلّق، مقبول، مرفوض، مستبعد. بالإضافة لثلاث قوائم فلاتر: الترتيب، النوع، والبلد.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/02-status-filter-bar.jpg" width="100%"></p>

---

### ✅ 3. Accept / Reject — One-Click Decision | قبول / رفض — قرار بضغطة واحدة

Hover over any card to reveal the action overlay:
- **Accept** ✓ — Adds to download queue, starts automatically
- **Reject** ✗ — Skips this title, moves to Rejected tab

Decision is saved instantly. No page reload needed.

حرّك الماوس فوق أي كارت: **Accept** يضيفه لقائمة التحميل، **Reject** يتخطاه. القرار بيتحفظ فوراً بدون إعادة تحميل.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/03-accept-reject-hover.jpg" width="100%"></p>

---

### 🔄 4. Multiple Versions Detection | اكتشاف النسخ المتعددة

When a series exists on multiple IPTV sources (e.g., Netflix version AND Prime Video version), the card shows a **"2 versions"** badge. You get to choose which source to download from.

لما مسلسل يكون عنده أكتر من مصدر IPTV، الكارت بيعرض علامة **"2 versions"**. تقدر تختار المصدر اللي تحبه.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/04-series-card-versions.jpg" width="100%"></p>

---

### 📋 5. Version Picker — Choose Your Source | اختيار المصدر

A picker dialog shows all available IPTV sources for the series. Each version shows the source name (Prime Video, Netflix, Hulu, etc.). Pick the one you prefer.

قائمة بكل مصادر IPTV المتاحة للمسلسل. كل نسخة بتعرض اسم المصدر. اختار اللي تفضله.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/05-accept-version-picker.jpg" width="100%"></p>

---

### 🎯 6. Episode Range Picker — Control What Downloads | اختيار نطاق الحلقات

After choosing a version, decide exactly which episodes to download:
- 📥 **Everything** — All seasons from S01E01 onwards
- 🆕 **New only** — Only future episodes (skip already aired)
- 🎯 **Custom** — Pick specific range (e.g., start from Season 2 Episode 5)

Shows **total episodes per season** (e.g., S01: 6 ep, S02: 5 ep = 11 total).

بعد اختيار النسخة، حدد الحلقات: **كل شيء** من البداية، **الجديد فقط** (الحلقات المستقبلية)، أو **مخصص** (نطاق معين). بيعرض عدد الحلقات لكل موسم.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/06-accept-episode-range.jpg" width="100%"></p>

---

### 📊 7. Accepted Series — Download Tracking | المسلسلات المقبولة — تتبع التحميل

Accepted series cards show real-time download status:
- Source platform badge (HBO, StarzPlay, Prime Video)
- Episode count and which episodes are queued
- Download progress indicators

كروت المسلسلات المقبولة بتعرض حالة التحميل اللحظية: منصة المصدر، عدد الحلقات، وحالة التحميل.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/07-accepted-series-tracking.jpg" width="100%"></p>

---

### ▶️ 8. Episode Progress — Where You Started | تقدم الحلقات — من أين بدأت

Each accepted series shows the exact starting point: "S01E09 onwards", "S01E11 onwards". IMDb ratings displayed. You always know exactly where each show stands.

كل مسلسل مقبول بيعرض نقطة البداية بالظبط وتقييم IMDb.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/08-accepted-series-progress.jpg" width="100%"></p>

---

### 📡 9. Section Sources — IPTV Categories | مصادر القسم — كاتيجوريز IPTV

Each section pulls content from specific IPTV categories. The header shows all source categories with **descriptive names** (e.g., "Box Office", "Top 100 IMDB", "English 2022-2026", "Netflix", etc.). You can **add or remove** sources at any time with the **Add Source +** button.

كل قسم بيسحب المحتوى من كاتيجوريز IPTV معينة. الهيدر بيعرض كل المصادر بأسمائها. تقدر تضيف أو تشيل مصادر في أي وقت.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/09-section-sources-labeled.jpg" width="100%"></p>

---

### 📁 10. Section Header — Full Details | هيدر القسم — التفاصيل الكاملة

The section header bar shows everything at a glance:
- **Section name** with enable/disable toggle
- **Disk usage** (e.g., 64.1 GB)
- **Hide** — Collapse section sources view
- **Edit** — Open section settings modal
- **Scan** — Re-scan this section from IPTV provider
- **Source categories** — All IPTV category IDs
- **Quick filters** — Folder path, min year, min rating

هيدر القسم بيعرض كل شيء: الاسم، حجم الديسك، أزرار إخفاء/تعديل/مسح، مصادر الكاتيجوريز، والفلاتر السريعة.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/10-section-header-details.jpg" width="100%"></p>

---

### ➕ 11. Add New Section — Full Configuration | إضافة قسم جديد

Create a new section with complete configuration:
- **Section Name** — Display name (e.g., "English Movies", "Turkish Series")
- **Section ID** — Unique identifier
- **IPTV Category IDs** — Comma-separated IDs from your provider
- **Browse IPTV Categories** — Visual browser to find and add categories
- **Download Folder** — Where files are saved (with Browse button)
- **Min Year** — Only include content from this year onwards
- **Min Rating** — Minimum IMDb rating threshold
- **VOD (Movies)** checkbox — Treat as movies (not series)
- **Use IMDb Data** — Enrich with IMDb metadata
- **Skip Strict Filters** — Bypass metadata/region/votes filtering
- **IPTV-Only Reset** — Use IPTV covers instead of TMDB
- **4K Source** — Mark as 4K quality section

أنشئ قسم جديد بإعدادات كاملة: الاسم، المصادر، فولدر التحميل، الفلاتر، وخيارات متقدمة مثل VOD و4K.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/11-add-new-section.jpg" width="100%"></p>

---

### ✏️ 12. Edit Section — Modify Anytime | تعديل القسم

Edit any existing section: change name, download folder, year/rating thresholds, and toggle advanced options (VOD, IMDb, strict filters, IPTV-only mode).

عدّل أي قسم في أي وقت: غيّر الاسم، الفولدر، الحدود، والخيارات المتقدمة.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/12-edit-section.jpg" width="100%"></p>

---

### 📺 13. Add Category Source — Browse IPTV Categories | إضافة مصدر — تصفح كاتيجوريز IPTV

Browse all available categories from your IPTV provider in a searchable dropdown. Each category shows its **ID** and **full name** (e.g., "338 — رمضان مصر 2026 (Series)"). Click **Add** to include it as a source.

تصفح كل كاتيجوريز IPTV المتاحة في قائمة قابلة للبحث. كل كاتيجوري بيعرض الرقم والاسم الكامل. اضغط **Add** لإضافته.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/13-add-category-source.jpg" width="100%"></p>

---

### 🔽 14-17. Smart Filters — Sort, Genre, Country | الفلاتر الذكية

**Sort Options** — Three sort modes:
- 🕐 **Newest** — Most recently added first
- ⭐ **Highest Rating** — Best IMDb rating first
- 🗳️ **Most Rated** — Most votes first

**Genre Filter** — Every genre in the current section with exact counts (Drama 152, Crime 73, Comedy 56, etc.)

**Country Filter** — Every country with counts (US 113, UK 58, Canada 10, etc.)

**Groups Only** — Special filter showing only series with multiple IPTV source versions (duplicates)

ثلاث طرق ترتيب + فلتر حسب النوع مع الأعداد + فلتر حسب البلد مع الأعداد + فلتر "مجموعات فقط" للنسخ المكررة.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/17-sort-dropdown.jpg" width="24%">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/15-genres-dropdown.jpg" width="24%">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/16-countries-dropdown.jpg" width="24%">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/18-groups-only-filter.jpg" width="24%">
</p>

---

### 🔍 18. Global Search — Cross-Section Results | البحث الشامل عبر الأقسام

Type in the search bar and results appear from **ALL sections simultaneously**. Shows "Also found across sections" with results grouped by section, including **status badges** (EXCLUDED, REJECTED, ACCEPTED). Each result shows thumbnail, rating, year, country, and section name.

اكتب في البحث والنتائج بتظهر من **كل الأقسام** في نفس الوقت. النتائج مجمعة حسب القسم مع حالة كل عنصر.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/19-cross-section-search.jpg" width="100%"></p>

---

### 📊 19-20. Filter Breakdown — Visual Analytics | تحليل الفلاتر — رسوم بيانية

**Countries Breakdown** — Bar chart showing content distribution by country. Excluded countries appear with ~~strikethrough~~. See exactly how your filters affect content: US 44%, UK 11%, France 6%, etc.

**Genres Breakdown** — Same for genres: Drama 24%, Action 11%, Comedy 10%. Excluded genres (Documentary, Animation, Sport) clearly marked.

رسوم بيانية توضح توزيع المحتوى حسب البلد والنوع. البلاد والأنواع المستبعدة بتظهر بخط عليها.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/20-filter-breakdown-countries.jpg" width="49%">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/21-filter-breakdown-genres.jpg" width="49%">
</p>

---

### 📈 21. System Statistics | إحصائيات النظام

Full system overview in one panel:

| Metric | Value |
|--------|-------|
| Total Series | 15,492 tracked |
| Total Decisions | 15,491 made |
| Downloads | 1,600 completed |
| This Week | 387.3 GB |
| This Month | 416.8 GB |
| Files Tracked | 1,066 |
| DB Size | 42.1 MB |

Plus: **Series by Section** breakdown, **Decisions by Status** (69 accepted, 14,592 auto-excluded, 536 pending, 292 rejected), and a **14-day Daily Downloads chart**.

لوحة إحصائيات شاملة: عدد المسلسلات، القرارات، التحميلات، الباندويث، حجم الداتابيز، ورسم بياني لآخر 14 يوم.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/22-system-statistics.jpg" width="80%"></p>

---

### 📊 22-23. Bandwidth Statistics — Monthly + Daily Detail | إحصائيات الباندويث

**Monthly View** — Total download volume with daily bar chart. Example: **416.8 GB** this month across **191 files**.

**Daily Detail** — Click any day to expand: see every file downloaded with name and size. Example: 2026-03-25 = 50.6 GB, 16 files (The Regime episodes, etc.).

تتبع تفصيلي للباندويث الشهري مع رسم بياني يومي. وسّع أي يوم وشوف كل ملف اتحمل بالاسم والحجم.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/23-bandwidth-monthly.jpg" width="49%">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/24-bandwidth-daily-detail.jpg" width="49%">
</p>

---

### 📋 24. Live Logs — Sync & Download Status | لوجات مباشرة

Two live log panels on the dashboard streaming real-time progress:
- **Sync Log** — Shows sync progress (fetching categories, enriching metadata, IMDB re-scan)
- **Download Log** — Shows download matching, space cleanup, metadata tagging

Toggle with the **Live** button in the header. When idle, shows "IDLE" status.

لوحتين لوجات مباشرة: المزامنة والتحميل. بتعرض التقدم اللحظي أو "IDLE" لما يكون فاضي.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/25-sync-download-logs-live.jpg" width="100%"></p>

---

### 📜 25-26. Full Logs — Detailed System Activity | لوجات كاملة

**System Logs Panel** — Full detailed downloader activity: sync matching, episode verification, space cleanup, metadata tagging across all media folders.

**Sync Log (100 lines)** — Full sync completion log with total series count, IMDB re-scan progress, verification stats.

**Download Log (100 lines)** — Matching accepted items to IPTV sources, space cleanup, rebuild progress, metadata tagger completion.

لوجات النظام الكاملة: نشاط المحمّل التفصيلي، لوج المزامنة الكامل (100 سطر)، ولوج التحميل الكامل.

<p align="center">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/27-sync-log-full.jpg" width="49%">
  <img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/28-download-log-full.jpg" width="49%">
</p>

---

### ▶️ 27. Manual Trigger — Sync & Download | تشغيل يدوي

Quick-action popover with **Sync** and **Download** run buttons. Click **"شغّل/Run"** to trigger either process manually at any time — no need to wait for the automatic cron schedule (sync every 6h, download every 40min).

زر تشغيل سريع: اضغط **"شغّل"** لتشغيل المزامنة أو التحميل يدوياً في أي وقت بدون انتظار الجدول التلقائي.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/29-sync-download-run-buttons.jpg" width="100%"></p>

---

### ⚙️ 28. Settings — Download Configuration | الإعدادات — إعدادات التحميل

Full download and system configuration:
- **Download Root Folder** — Parent folder containing all media (with Browse button). Example: `/media`
- **aria2c Connections** — Number of parallel connections per download (default: 16 for max speed)
- **Daily Download Limit** — Maximum downloads per day (default: 50)
- **Trash Folder** — Where deleted media is stored before permanent removal
- **Auto-restart on slow speed** — Automatically restarts downloads that drop below a speed threshold
- **🎨 Theme Mode** — Three options: **Auto** (light during day 6am-6pm, dark at night), **Light** (always light), **Dark** (always dark)

إعدادات التحميل: فولدر التحميل الرئيسي (مع زر Browse)، عدد اتصالات aria2c (16 افتراضي)، حد التحميل اليومي (50)، فولدر المهملات، إعادة التشغيل التلقائي عند بطء السرعة، ووضع الثيم (أوتو/فاتح/داكن).

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/30-settings-download.jpg" width="100%"></p>

---

### 🚫 29. Settings — Global Exclusions | الإعدادات — الاستبعاد العام

Three types of global exclusion rules applied to **ALL sections**:

**🌍 Excluded Countries** — Auto-exclude content from specific countries. Example: india, china, korea, japan, hong kong, taiwan, vietnam, thailand, pakistan, indonesia, philippines, italy, brazil, saudi arabia.

**🎭 Excluded Genres** — Auto-exclude specific genres. Example: documentary, animation, musical, sport, cartoon, fantasy, music, short, game-show.

**🗣️ Excluded Languages** — Auto-exclude by ISO language code. Example: hi (Hindi), zh (Chinese), ko (Korean), ja (Japanese), ta (Tamil), te (Telugu), etc.

Items matching ANY of these rules are automatically moved to the Excluded tab with a **clear reason badge** explaining why.

ثلاث أنواع قواعد استبعاد عامة: بلاد، أنواع، لغات. العناصر المطابقة بتتنقل تلقائياً للمستبعد مع **سبب واضح**.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/31-settings-exclusions.jpg" width="100%"></p>

---

### 🎚️ 30. Settings — Per-Section Filters | الإعدادات — فلاتر لكل قسم

Each section has **independent** filter thresholds:
- **Min Year** — e.g., English Movies: 2020, Foreign Series: 2022, Turkish: 2025
- **Min Rating** — e.g., 6.0 minimum IMDb rating
- **Min Rating Count** — e.g., 2000 minimum votes (filters out unknown/obscure titles)

Changes are saved per-section and take effect immediately.

كل قسم له فلاتر مستقلة: الحد الأدنى للسنة والتقييم وعدد الأصوات. التغييرات تنطبق فوراً.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/32-settings-section-filters.jpg" width="100%"></p>

---

### 🔤 31. Settings — Banned Keywords per Section | كلمات محظورة لكل قسم

Set keywords that auto-**exclude** matching titles per section. Example: "مدبلج" (dubbed) is banned in English Movies, Foreign Series, and Turkish sections — any title containing this word is automatically excluded.

Keywords apply retroactively to all pending items.

حدد كلمات محظورة لكل قسم. أي عنوان فيه الكلمة بيتم استبعاده تلقائياً. بينطبق على كل العناصر المعلقة.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/33-settings-banned-keywords.jpg" width="100%"></p>

---

### ⛔ 32. Settings — Pre-Rejected Keywords | كلمات مرفوضة مسبقاً

**Stronger** than banned keywords. Pre-rejected keywords automatically **REJECT** (not just exclude) matching titles — they go straight to the Rejected tab. Used for content you absolutely don't want.

Example: Ramadan 2026 section with specific Arabic show titles pre-rejected.

أقوى من الكلمات المحظورة. الكلمات المرفوضة مسبقاً بترفض العناصر تلقائياً (مش بس استبعاد) — بتروح مباشرة للمرفوض.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/34-settings-pre-rejected.jpg" width="100%"></p>

---

### 🌐 33. Settings — Per-Section Country Exclusions | استبعاد بلاد لكل قسم

Override global country exclusions per section. Example: English Movies section has **80+ countries excluded** (allowing only US, UK, Canada, Australia, etc.). Each section has its own independent country exclusion list.

Also supports per-section **Genre** and **Language** exclusions in separate sub-tabs.

تخصيص استبعاد البلاد لكل قسم بشكل مستقل. أيضاً بيدعم استبعاد الأنواع واللغات لكل قسم في تابات فرعية.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/35-settings-section-countries.jpg" width="100%"></p>

---

### 📂 34. Settings — Browse & Exclude | تصفح واستبعد

Visual browser for IPTV content. Select a section, search, and browse items directly. Reject unwanted content visually without switching to the dashboard.

متصفح مرئي لمحتوى IPTV. اختار القسم وتصفح واستبعد العناصر مباشرة.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/36-settings-browse-exclude.jpg" width="100%"></p>

---

### 💾 35. Settings — Backups | النسخ الاحتياطي

Full database backup management:
- **Create Backup Now** — Instant manual backup
- **Upload & Restore** — Upload a `.db` file from your computer and restore
- **Automatic Daily Backups** — Cron job keeps last 3 days
- **Download** any backup to your computer
- **Safety backup** created automatically before every restore operation

إدارة النسخ الاحتياطي: إنشاء فوري، رفع واسترجاع، نسخ يومي تلقائي (آخر 3 أيام)، تحميل، ونسخة أمان قبل كل استرجاع.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/37-settings-backups.jpg" width="100%"></p>

---

### 🗄️ 36. Settings — Database Browser | متصفح قاعدة البيانات

Built-in phpMyAdmin-style database browser showing all **26 tables** with row and column counts (e.g., media: 15,492 rows × 28 cols, decisions: 15,491 rows × 6 cols). Features:
- **Maintenance** — Optimize/vacuum the database
- **Repair Covers** — Re-download missing or broken cover images
- **SQL Query** — Execute custom SQL queries (advanced users)
- Click any table to **browse data** with pagination, search, and sort
- **Delete rows** individually

متصفح قاعدة بيانات مدمج يعرض كل الـ 26 جدول. صيانة، إصلاح الأغلفة، استعلامات SQL، وتصفح البيانات بالتفصيل.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/38-settings-database-browser.jpg" width="100%"></p>

---

### 🌙 37. Dark Theme — Full Support | الوضع الداكن

Complete dark theme with three modes:
- **🌓 Auto** — Light during day (6am–6pm), dark at night (automatic)
- **☀️ Light** — Always light theme
- **🌙 Dark** — Always dark theme

Toggle via the moon/sun icon in the header bar. ALL pages, modals, cards, charts, and inputs support both themes perfectly.

وضع داكن كامل بثلاث أوضاع: أوتو (حسب الوقت)، فاتح دائماً، داكن دائماً. كل الصفحات والنوافذ بتدعم الوضعين.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/39-dark-theme.jpg" width="100%"></p>

---

### 🏷️ 38. Excluded Tab — Clear Reasons | تاب المستبعد — أسباب واضحة

Every auto-excluded item shows exactly **why** it was filtered:
- 🔴 **Votes 0 < 2000** — Too few votes
- 🔴 **Year < 2020** — Too old
- 🔴 **Country: excluded** — From an excluded country
- 🔴 **Genre: excluded** — Excluded genre
- 🔴 **Keyword match** — Matched a banned keyword

Nothing disappears — **everything is traceable**.

كل عنصر مستبعد بيعرض بالظبط **ليه** اتفلتر: عدد أصوات قليل، سنة قديمة، بلد مستبعد، نوع مستبعد، أو كلمة محظورة.

<p align="center"><img src="https://raw.githubusercontent.com/egphp/iptv-manager-updates/main/screenshots/05-accept-version-picker.jpg" width="100%"></p>

---

## Architecture | البنية

```
┌──────────────────────────────────────────┐
│         Docker Container (Alpine)        │
│                                          │
│  ┌──────────────┐  ┌──────────────────┐  │
│  │  Cheroot      │  │   dcron          │  │
│  │  HTTPS :443   │  │  Sync (6h)      │  │
│  │  auto-SSL     │  │  Download (40m) │  │
│  │  mDNS         │  │  Check (12h)    │  │
│  └──────────────┘  └──────────────────┘  │
│                                          │
│  /app         (code — read-only)         │
│  /app/data    (DB, covers, certs) ← VOL  │
│  /media       (downloads)         ← MNT  │
└──────────────────────────────────────────┘

Access: https://iptv.local (mDNS — zero-config)
```

| Component | Technology |
|-----------|-----------|
| **Container** | Docker (Alpine Linux + Python 3.12) |
| **Web Server** | Cheroot WSGI (native SSL, thread-pooled, production-grade) |
| **Framework** | Flask |
| **Database** | SQLite (normalized v2, 26 tables, WAL mode, 16MB cache) |
| **Downloads** | aria2c (multi-connection, resume, 40+ MB/s) |
| **Metadata** | TMDB API + OMDb API + IMDb Watchlist integration |
| **Notifications** | Web Push (VAPID) via pywebpush |
| **Discovery** | mDNS (iptv.local — zero-config LAN access) |
| **SSL** | Auto-generated CA + server cert (10-year validity) |
| **Frontend** | Vanilla JS + CSS3 (zero frameworks, gzipped static) |
| **Theme** | Auto/Light/Dark with time-based switching |
| **PWA** | Installable, offline-capable, push notifications |

---

## Automatic Cron Jobs | المهام التلقائية

| Schedule | Job | What It Does |
|----------|-----|-------------|
| Every **40 min** | Download | Downloads accepted series/movies via aria2c with resume support |
| Every **6 hours** | Sync | Fetches new content from IPTV API, enriches with TMDB/OMDb, applies all filters |
| Every **12 hours** | Integrity Check | Verifies downloaded files, resumes partials, detects corruption |
| **Daily** midnight | Auto-Backup | Creates database backup, keeps last 3 days |

---

## Installation | التسطيب

### Windows (One-Click)

```
1. Install Docker Desktop from docker.com
2. Download setup-docker.bat from Releases
3. Right-click → Run as Administrator
4. Enter your media folder path (e.g. D:\Media)
5. Done! Open https://iptv.local
```

The setup script auto-migrates data from old native installations and cleans old startup entries.

### macOS

```bash
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 -v iptv-data:/app/data \
  -v /Volumes/YourDisk/Media:/media \
  -e TZ=Africa/Cairo iptv-manager
```

### Linux

```bash
curl -fsSL https://get.docker.com | sh
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 -v iptv-data:/app/data \
  -v /mnt/media:/media -e TZ=Africa/Cairo iptv-manager
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
      - /path/to/media:/media   # ← CHANGE THIS
    environment:
      - TZ=Africa/Cairo
volumes:
  iptv-data:
```

### First Run | أول تشغيل

1. Open **https://iptv.local** (mDNS — no hosts file needed)
2. Accept the self-signed certificate (one-time)
3. **Settings** → Enter IPTV credentials (server URL, username, password)
4. (Optional) Add **TMDB Bearer Token** and **OMDb API Key** for richer metadata
5. Create sections → assign IPTV categories → set download folders
6. Click **Sync** → new content appears in Pending tab
7. Accept what you want → downloads start automatically every 40 minutes

---

## iPhone / iPad — Install CA Certificate | تركيب الشهادة

For green lock (no "Not Secure" warning):

1. Open **Safari** (not Chrome — iOS ignores certs from Chrome)
2. Go to `https://iptv.local/install-ca`
3. Tap **Allow** to download the profile
4. **Settings → General → VPN & Device Management** → Install "IPTV Manager CA"
5. **Settings → General → About → Certificate Trust Settings** → Enable
6. Done! Green lock on `https://iptv.local`

---

## How It Works | كيف يعمل

```
┌─────────────────┐     ┌──────────────┐     ┌────────────────┐
│   IPTV Provider  │────▶│   Auto Sync  │────▶│  TMDB / OMDb   │
│  (Series + VOD)  │     │  (Every 6h)  │     │  (Enrich Data) │
└─────────────────┘     └──────────────┘     └────────────────┘
                                                      │
                              ┌────────────────────────┘
                              ▼
                    ┌──────────────────┐
                    │  Smart Filters   │
                    │  Year, Rating,   │
                    │  Country, Genre, │
                    │  Keywords, Lang  │
                    └──────────────────┘
                              │
              ┌───────────────┼───────────────┐
              ▼               ▼               ▼
     ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
     │   Pending    │ │   Excluded   │ │   Excluded   │
     │  (Your call) │ │  (Filtered)  │ │   but Rich   │
     └──────────────┘ └──────────────┘ └──────────────┘
              │
     ┌────────┼────────┐
     ▼        ▼        ▼
  Accept   Reject   Watched
     │
     ▼
┌──────────────┐     ┌──────────────┐
│   aria2c     │────▶│    Plex      │
│  (Download)  │     │   (Watch!)   │
└──────────────┘     └──────────────┘
```

---

## Migration from Old Installation | الترقية من النسخة القديمة

**Windows:** Run `setup-docker.bat` — auto-detects and migrates your database, covers, and settings.

**macOS/Linux:**
```bash
docker volume create iptv-data
docker run --rm -v iptv-data:/data -v /path/to/old/install:/src alpine sh -c \
  "cp /src/iptv_manager.db /data/ && cp -r /src/covers /data/"
docker run -d --name iptv-manager --restart unless-stopped \
  -p 443:443 -v iptv-data:/app/data -v /mnt/media:/media iptv-manager
```

Paths auto-migrate (e.g., `/Volumes/3TB/Plex/Movies` → `/media/Movies`) on first run.

---

## Keyboard Shortcuts | اختصارات لوحة المفاتيح

| Key | Action |
|-----|--------|
| `S` or `/` | Focus search bar |
| `1` – `9` | Switch to section 1–9 |
| `Escape` | Close any open modal |

---

<details>
<summary><strong>📡 API Reference — 60+ Endpoints (click to expand)</strong></summary>

### Series & Decisions
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/series` | Paginated series list with counts |
| GET | `/api/series/hash` | Data hash for lightweight polling |
| POST | `/api/series/{id}/accept` | Accept series/movie for download |
| POST | `/api/series/{id}/reject` | Reject series/movie |
| POST | `/api/series/{id}/watched_removed` | Mark watched + delete files |
| GET | `/api/series/{id}/episodes` | Live episode list from IPTV |
| GET | `/api/series/{id}/siblings` | Duplicate entries from other sources |
| POST | `/api/series/{id}/reject_group` | Reject all siblings at once |

### Sections
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/categories` | All IPTV categories from provider |
| POST | `/api/sections` | Create/update section |
| POST | `/api/sections/{id}/toggle` | Enable/disable section |
| POST | `/api/sections/{id}/update` | Edit section settings |
| POST | `/api/sections/{id}/add_category` | Add IPTV source category |
| POST | `/api/sections/{id}/remove_category` | Remove IPTV source category |
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
| POST | `/api/remote/auth` | Authenticate (get 24h token) |
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

لو المشروع أفادك، فكّر في دعم التطوير:

<p align="center">
  <a href="https://www.paypal.com/ncp/payment/GYPXYRC3MJ85C">
    <img src="https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal&logoColor=white" alt="Donate via PayPal" height="40">
  </a>
</p>

---

## License

MIT License — Free to use, modify, and distribute.

---

<p align="center">
  <sub>Built with passion for a better viewing experience 🎬</sub>
</p>
