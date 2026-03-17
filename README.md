# IPTV Manager

**A complete IPTV Series & Movies management system with automatic downloads, metadata, and a beautiful web dashboard.**

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🌐 **Web Dashboard** | Modern dark-themed UI to manage your IPTV content |
| 🔍 **Auto-Discovery** | Automatically finds new series and movies from your IPTV provider |
| ⬇️ **Smart Downloads** | Downloads new episodes automatically via aria2c |
| 🎬 **Metadata & Posters** | Fetches info and covers from TMDB and OMDb APIs |
| ✅ **Accept/Reject** | Review and decide what to download |
| 📂 **Multi-Section** | Organize by categories (Arabic, Turkish, English, etc.) |
| 🔄 **Auto-Update** | Windows installs auto-update from this repository |
| 🖥️ **System Tray** | Windows tray icon with server controls and watchdog |
| 🔔 **Push Notifications** | Get notified when downloads complete (PWA) |

---

## 📥 Installation (Windows)

### Quick Start
1. Download the latest `IPTV_Manager_Setup.bat` from **[Releases](../../releases/latest)**
2. Right-click → **Run as Administrator**
3. Follow the setup wizard
4. Click **Launch Dashboard** when done

### Setup Wizard Steps
| Step | What to do |
|------|------------|
| 1️⃣ Welcome | Click Next |
| 2️⃣ IPTV Account | Enter your IPTV username, password, and server URL |
| 3️⃣ API Keys | Enter TMDB and OMDb keys (optional - can add later) |
| 4️⃣ Install | Automatic - installs packages, firewall, startup entry |
| 5️⃣ Done | Click Launch Dashboard |

### System Tray Icon
After installation, an icon appears next to the clock:
- **🟢 Green** = Server running | **🔴 Red** = Server stopped
- **Double-click** → Open Dashboard in browser
- **Right-click menu:**
  - Start / Stop / Restart Server
  - Settings (edit credentials & API keys)
  - Watchdog toggle (auto-restart on crash)
  - Exit

### Auto-Updates
This installation **automatically checks for updates every 5 minutes** from this GitHub repository. When a new release is published, it downloads and applies the update with zero user interaction.

---

## 🍎 Installation (macOS/Linux)

```bash
cd /path/to/IPTV_Manager
pip3 install flask requests
python3 series_manager_web.py
# Open https://localhost:8888
```

---

## 📋 Requirements

| Component | Purpose | Required |
|-----------|---------|----------|
| Python 3.10+ | Core runtime | ✅ Yes |
| Flask | Web server | ✅ Yes (auto-installed) |
| aria2c | Fast downloads | ✅ Yes (auto-installed) |
| TMDB API key | Movie/series metadata | ⚡ Optional |
| OMDb API key | Ratings and extra info | ⚡ Optional |

---

## 🖼️ Screenshots

### Dashboard
> Modern dark-themed dashboard with series/movies management, download status, and metadata.

### System Tray
> Tray icon with quick controls - start, stop, restart, settings, and watchdog.

### Setup Wizard
> Step-by-step dark-themed installer with IPTV credentials and API key configuration.

---

## 📂 Project Structure

```
IPTV_Manager/
├── series_manager_web.py    # Main web server + dashboard
├── series_manager_sync.py   # IPTV catalog sync
├── iptv_downloader.py       # Episode/movie downloader
├── db.py                    # SQLite database layer
├── setup_gui.pyw            # Windows setup wizard (tkinter)
├── tray_manager.pyw         # Windows system tray + watchdog
├── fix_covers.py            # Cover image repair utility
├── fix_missing_covers.py    # Missing poster fetcher
├── repair_posters.py        # Poster validation & repair
└── refresh_omdb_data.py     # OMDb metadata refresher
```

---
---

# IPTV Manager - عربي

**نظام إدارة IPTV كامل لتحميل المسلسلات والأفلام أوتوماتيك مع داشبورد ويب حديث.**

---

## ✨ المميزات

| الميزة | الوصف |
|--------|-------|
| 🌐 **داشبورد ويب** | واجهة حديثة وأنيقة لإدارة المحتوى |
| 🔍 **اكتشاف تلقائي** | يلاقي المسلسلات والأفلام الجديدة أوتوماتيك |
| ⬇️ **تحميل ذكي** | يحمّل الحلقات الجديدة أوتوماتيك عن طريق aria2c |
| 🎬 **بيانات وبوسترات** | يجيب المعلومات من TMDB و OMDb |
| ✅ **قبول/رفض** | راجع المحتوى وقرر إيه اللي يتحمّل |
| 📂 **أقسام متعددة** | نظّم المحتوى حسب الفئات (عربي، تركي، إنجليزي) |
| 🔄 **تحديث تلقائي** | نسخة الويندوز بتتحدث من GitHub أوتوماتيك |
| 🖥️ **أيقونة جمب الساعة** | أيقونة في شريط المهام للتحكم في السيرفر |
| 🔔 **إشعارات** | تنبيهات لما يخلص تحميل فيلم أو حلقة |

---

## 📥 التسطيب (ويندوز)

### خطوات سريعة
1. حمّل آخر `IPTV_Manager_Setup.bat` من **[الإصدارات](../../releases/latest)**
2. كليك يمين → **تشغيل كمسؤول (Run as Administrator)**
3. اتبع خطوات المعالج
4. دوس **Launch Dashboard** لما يخلص

### خطوات المعالج
| الخطوة | المطلوب |
|--------|---------|
| 1️⃣ ترحيب | دوس Next |
| 2️⃣ حساب IPTV | حط اسم المستخدم وكلمة المرور ورابط السيرفر |
| 3️⃣ مفاتيح API | حط مفاتيح TMDB و OMDb (اختياري) |
| 4️⃣ تسطيب | أوتوماتيك - بيسطب الحزم والفايروول |
| 5️⃣ تم | دوس Launch Dashboard |

### أيقونة شريط المهام
بعد التسطيب، أيقونة بتظهر جمب الساعة:
- **🟢 أخضر** = السيرفر شغال | **🔴 أحمر** = السيرفر واقف
- **دبل كليك** → فتح الداشبورد
- **كليك يمين:**
  - تشغيل / إيقاف / إعادة تشغيل السيرفر
  - الإعدادات (تعديل البيانات ومفاتيح API)
  - المراقب (يعيد تشغيل السيرفر لو وقع)
  - خروج

### التحديث التلقائي
النسخة دي **بتتشيك على GitHub كل 5 دقائق**. لما يكون في تحديث جديد، بتحمّله وتطبّقه أوتوماتيك. مش محتاج تعمل أي حاجة.

---

## 📋 المتطلبات

| المكوّن | الغرض | مطلوب |
|---------|-------|-------|
| Python 3.10+ | التشغيل الأساسي | ✅ نعم |
| Flask | سيرفر الويب | ✅ نعم (بيتسطب أوتوماتيك) |
| aria2c | تحميل سريع | ✅ نعم (بيتسطب أوتوماتيك) |
| TMDB API key | بيانات الأفلام/المسلسلات | ⚡ اختياري |
| OMDb API key | التقييمات ومعلومات إضافية | ⚡ اختياري |

---

## License
MIT License - Free to use and modify.
