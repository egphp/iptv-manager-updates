# API Endpoint Inventory

Generated from the IPTV Manager source tree on 2026-04-29. Routes are grouped by blueprint/module and include admin-only routes because they are part of the application surface.

**Total route decorators:** 299

| Group | Count |
|---|---:|
| `web/routes/system` | 87 |
| `web/routes/series` | 63 |
| `web/routes/pwa.py` | 19 |
| `web/routes/trash` | 19 |
| `web/routes/settings` | 16 |
| `web/routes/live.py` | 14 |
| `web/routes/plex_tracking.py` | 12 |
| `web/routes/repair` | 12 |
| `web/routes/discovery` | 10 |
| `admin/routes` | 8 |
| `web/routes/micky.py` | 8 |
| `web/routes/remote.py` | 7 |
| `web/routes/backups.py` | 6 |
| `web/routes/update.py` | 6 |
| `series_manager_web.py` | 4 |
| `web/routes/actors.py` | 3 |
| `web/routes/social_badge.py` | 2 |
| `web/routes/search_page.py` | 1 |
| `web/routes/social.py` | 1 |
| `web/routes/vpn.py` | 1 |

## admin/routes

| Methods | Route | Source |
|---|---|---|
| `POST` | `/api/db/maintenance` | `admin/routes/database_ops.py:232` |
| `POST` | `/api/db/query` | `admin/routes/database_ops.py:137` |
| `POST` | `/api/db/row/delete` | `admin/routes/database_ops.py:184` |
| `GET` | `/api/db/table/<table_name>` | `admin/routes/database_ops.py:68` |
| `GET` | `/api/db/tables` | `admin/routes/database_ops.py:42` |
| `GET` | `/api/export` | `admin/routes/export.py:28` |
| `GET` | `/api/github-update-status` | `admin/routes/publish.py:606` |
| `POST` | `/api/publish-update` | `admin/routes/publish.py:62` |

## series_manager_web.py

| Methods | Route | Source |
|---|---|---|
| `POST` | `/api/remote-login` | `series_manager_web.py:232` |
| `GET` | `/static/<path:filename>` | `series_manager_web.py:41` |
| `GET` | `/tmdb-img/<filename>` | `series_manager_web.py:93` |
| `GET` | `/trailers/<filename>` | `series_manager_web.py:106` |

## web/routes/actors.py

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/actors/<name>/media` | `web/routes/actors.py:167` |
| `GET` | `/api/actors/<name>/photo` | `web/routes/actors.py:205` |
| `GET` | `/api/actors/search` | `web/routes/actors.py:78` |

## web/routes/backups.py

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/backups` | `web/routes/backups.py:18` |
| `POST` | `/api/backups/create` | `web/routes/backups.py:52` |
| `POST` | `/api/backups/delete` | `web/routes/backups.py:118` |
| `GET` | `/api/backups/download/<backup_name>` | `web/routes/backups.py:141` |
| `POST` | `/api/backups/restore` | `web/routes/backups.py:69` |
| `POST` | `/api/backups/upload` | `web/routes/backups.py:153` |

## web/routes/discovery

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/disk/count` | `web/routes/discovery/count.py:17` |
| `GET` | `/api/disk/episodes` | `web/routes/discovery/episodes.py:16` |
| `POST` | `/api/disk/ignore` | `web/routes/discovery/ignore.py:111` |
| `DELETE` | `/api/disk/ignore/<int:ignore_id>` | `web/routes/discovery/ignore.py:134` |
| `GET` | `/api/disk/ignores` | `web/routes/discovery/ignore.py:127` |
| `POST` | `/api/disk/link-external` | `web/routes/discovery/link.py:15` |
| `POST` | `/api/disk/merge` | `web/routes/discovery/merge.py:38` |
| `GET` | `/api/disk/scan` | `web/routes/discovery/scan.py:92` |
| `GET` | `/api/disk/scan/progress` | `web/routes/discovery/scan.py:132` |
| `POST` | `/api/disk/search` | `web/routes/discovery/search.py:26` |

## web/routes/live.py

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/live/all-categories` | `web/routes/live.py:383` |
| `GET` | `/api/live/channels` | `web/routes/live.py:143` |
| `GET` | `/api/live/chunk/<stream_id>/<int:seq>` | `web/routes/live.py:227` |
| `GET` | `/api/live/daily-stats` | `web/routes/live.py:437` |
| `POST` | `/api/live/exclude-category` | `web/routes/live.py:405` |
| `GET` | `/api/live/excluded-categories` | `web/routes/live.py:398` |
| `POST` | `/api/live/heartbeat` | `web/routes/live.py:348` |
| `GET` | `/api/live/live.m3u8/<stream_id>` | `web/routes/live.py:202` |
| `POST` | `/api/live/log-error` | `web/routes/live.py:426` |
| `GET` | `/api/live/play/<stream_id>` | `web/routes/live.py:250` |
| `POST` | `/api/live/refresh` | `web/routes/live.py:160` |
| `POST` | `/api/live/start` | `web/routes/live.py:292` |
| `GET` | `/api/live/status` | `web/routes/live.py:452` |
| `POST` | `/api/live/stop` | `web/routes/live.py:364` |

## web/routes/micky.py

| Methods | Route | Source |
|---|---|---|
| `DELETE` | `/api/micky/<int:row_id>` | `web/routes/micky.py:333` |
| `POST` | `/api/micky/clear` | `web/routes/micky.py:438` |
| `GET` | `/api/micky/count` | `web/routes/micky.py:317` |
| `POST` | `/api/micky/download` | `web/routes/micky.py:269` |
| `GET` | `/api/micky/list` | `web/routes/micky.py:308` |
| `GET` | `/api/micky/play/<int:row_id>` | `web/routes/micky.py:365` |
| `GET` | `/api/micky/status/<int:row_id>` | `web/routes/micky.py:324` |
| `GET` | `/api/micky/thumb/<int:row_id>` | `web/routes/micky.py:419` |

## web/routes/plex_tracking.py

| Methods | Route | Source |
|---|---|---|
| `POST` | `/api/plex/tracking/home/assign` | `web/routes/plex_tracking.py:111` |
| `GET` | `/api/plex/tracking/home/discovery` | `web/routes/plex_tracking.py:106` |
| `GET` | `/api/plex/tracking/items` | `web/routes/plex_tracking.py:60` |
| `GET` | `/api/plex/tracking/items/<path:media_iptv_id>/detail` | `web/routes/plex_tracking.py:81` |
| `POST` | `/api/plex/tracking/items/<path:media_iptv_id>/reclaim/<action>` | `web/routes/plex_tracking.py:87` |
| `GET` | `/api/plex/tracking/sections` | `web/routes/plex_tracking.py:76` |
| `GET` | `/api/plex/tracking/sync/status` | `web/routes/plex_tracking.py:101` |
| `POST` | `/api/plex/tracking/sync/trigger` | `web/routes/plex_tracking.py:96` |
| `GET` | `/api/plex/tracking/users` | `web/routes/plex_tracking.py:25` |
| `POST` | `/api/plex/tracking/users/<int:user_id>/nickname` | `web/routes/plex_tracking.py:38` |
| `POST` | `/api/plex/tracking/users/<int:user_id>/sections/<int:section_id>/interest` | `web/routes/plex_tracking.py:47` |
| `POST` | `/api/plex/tracking/users/<int:user_id>/track` | `web/routes/plex_tracking.py:30` |

## web/routes/pwa.py

| Methods | Route | Source |
|---|---|---|
| `POST` | `/api/push/subscribe` | `web/routes/pwa.py:291` |
| `POST` | `/api/push/test` | `web/routes/pwa.py:313` |
| `POST` | `/api/push/unsubscribe` | `web/routes/pwa.py:303` |
| `GET` | `/api/push/vapid-key` | `web/routes/pwa.py:286` |
| `POST` | `/api/restart-server` | `web/routes/pwa.py:269` |
| `GET` | `/apple-touch-icon-precomposed.png` | `web/routes/pwa.py:247` |
| `GET` | `/apple-touch-icon.png` | `web/routes/pwa.py:242` |
| `GET` | `/covers/<path:filename>` | `web/routes/pwa.py:22` |
| `GET` | `/favicon-16.png` | `web/routes/pwa.py:261` |
| `GET` | `/favicon-32.png` | `web/routes/pwa.py:257` |
| `GET` | `/favicon.ico` | `web/routes/pwa.py:253` |
| `GET` | `/install-ca` | `web/routes/pwa.py:147` |
| `GET` | `/logo.png` | `web/routes/pwa.py:265` |
| `GET` | `/manifest.json` | `web/routes/pwa.py:204` |
| `GET` | `/mthumb/<path:filename>` | `web/routes/pwa.py:54` |
| `GET` | `/pwa-icon-192.png` | `web/routes/pwa.py:234` |
| `GET` | `/pwa-icon-512.png` | `web/routes/pwa.py:238` |
| `GET` | `/sw.js` | `web/routes/pwa.py:221` |
| `GET` | `/thumbs/<path:filename>` | `web/routes/pwa.py:105` |

## web/routes/remote.py

| Methods | Route | Source |
|---|---|---|
| `OPTIONS` | `/api/remote/<path:subpath>` | `web/routes/remote.py:296` |
| `POST` | `/api/remote/auth` | `web/routes/remote.py:315` |
| `POST` | `/api/remote/decide` | `web/routes/remote.py:452` |
| `POST` | `/api/remote/download` | `web/routes/remote.py:486` |
| `POST` | `/api/remote/logout` | `web/routes/remote.py:370` |
| `GET` | `/api/remote/pending` | `web/routes/remote.py:384` |
| `GET` | `/remote` | `web/routes/remote.py:308` |

## web/routes/repair

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/device-alerts` | `web/routes/repair/health.py:377` |
| `GET` | `/api/device-health` | `web/routes/repair/health.py:242` |
| `POST` | `/api/device-port-check` | `web/routes/repair/health.py:277` |
| `GET` | `/api/device-port-status` | `web/routes/repair/health.py:252` |
| `POST` | `/api/device-repair` | `web/routes/repair/repair_cmds.py:23` |
| `POST` | `/api/ssh-terminal/close` | `web/routes/repair/terminal.py:146` |
| `POST` | `/api/ssh-terminal/input` | `web/routes/repair/terminal.py:102` |
| `POST` | `/api/ssh-terminal/open` | `web/routes/repair/terminal.py:15` |
| `GET` | `/api/ssh-terminal/preset/list` | `web/routes/repair/repair_cmds.py:118` |
| `POST` | `/api/ssh-terminal/read` | `web/routes/repair/terminal.py:68` |
| `POST` | `/api/ssh-terminal/resize` | `web/routes/repair/terminal.py:124` |
| `GET` | `/api/tunnel-sync` | `web/routes/repair/health.py:386` |

## web/routes/search_page.py

| Methods | Route | Source |
|---|---|---|
| `GET` | `/search` | `web/routes/search_page.py:9` |

## web/routes/series

| Methods | Route | Source |
|---|---|---|
| `GET` | `/` | `web/routes/series/list.py:30` |
| `GET` | `/api/browse-path` | `web/routes/series/list.py:300` |
| `GET` | `/api/calendar` | `web/routes/series/list.py:421` |
| `GET` | `/api/categories` | `web/routes/series/variants.py:401` |
| `GET` | `/api/category-names` | `web/routes/series/variants.py:393` |
| `GET, POST` | `/api/dashboard/nav-state` | `web/routes/series/nav_state.py:48` |
| `GET` | `/api/mode` | `web/routes/series/list.py:399` |
| `POST` | `/api/mode` | `web/routes/series/list.py:407` |
| `POST` | `/api/save-screenshot` | `web/routes/series/list.py:281` |
| `POST` | `/api/sections` | `web/routes/series/variants.py:201` |
| `POST` | `/api/sections/<section_id>/add_category` | `web/routes/series/variants.py:237` |
| `POST` | `/api/sections/<section_id>/delete` | `web/routes/series/variants.py:307` |
| `GET` | `/api/sections/<section_id>/delete_info` | `web/routes/series/variants.py:282` |
| `POST` | `/api/sections/<section_id>/remove_category` | `web/routes/series/variants.py:261` |
| `POST` | `/api/sections/<section_id>/toggle` | `web/routes/series/variants.py:177` |
| `POST` | `/api/sections/<section_id>/update` | `web/routes/series/variants.py:328` |
| `GET` | `/api/series` | `web/routes/series/list.py:61` |
| `POST` | `/api/series/<iptv_id>/confirm-match` | `web/routes/series/match.py:330` |
| `POST` | `/api/series/<iptv_id>/search-match` | `web/routes/series/match.py:175` |
| `POST` | `/api/series/<iptv_id>/skip-match` | `web/routes/series/match.py:687` |
| `POST` | `/api/series/<iptv_id>/undo-match` | `web/routes/series/match.py:664` |
| `POST` | `/api/series/<series_id>/accept` | `web/routes/series/accept.py:20` |
| `POST` | `/api/series/<series_id>/dismiss-season/<int:season>` | `web/routes/series/untrack.py:70` |
| `GET` | `/api/series/<series_id>/episodes` | `web/routes/series/list.py:244` |
| `POST` | `/api/series/<series_id>/reject` | `web/routes/series/reject.py:59` |
| `POST` | `/api/series/<series_id>/reject_group` | `web/routes/series/group.py:20` |
| `GET` | `/api/series/<series_id>/siblings` | `web/routes/series/variants.py:12` |
| `POST` | `/api/series/<series_id>/undismiss-season/<int:season>` | `web/routes/series/untrack.py:97` |
| `POST` | `/api/series/<series_id>/untrack` | `web/routes/series/untrack.py:20` |
| `POST` | `/api/series/<series_id>/watched_removed` | `web/routes/series/untrack.py:118` |
| `POST` | `/api/series/batch-reenrich` | `web/routes/series/batch_reenrich.py:65` |
| `GET` | `/api/series/hash` | `web/routes/series/list.py:236` |
| `GET` | `/api/series/latest-downloaded` | `web/routes/series/local_counts.py:215` |
| `GET` | `/api/series/latest-downloaded-order` | `web/routes/series/local_counts.py:256` |
| `GET` | `/api/series/local-counts` | `web/routes/series/local_counts.py:131` |
| `POST` | `/api/series/reject_all_pending/<section_id>` | `web/routes/series/reject.py:255` |
| `GET` | `/api/series/unmatched` | `web/routes/series/batch_reenrich.py:247` |
| `GET` | `/api/settings/cleanup-words` | `web/routes/series/list.py:378` |
| `POST` | `/api/settings/cleanup-words` | `web/routes/series/list.py:387` |
| `GET` | `/api/watch/continue` | `web/routes/series/track.py:197` |
| `GET` | `/api/watch/episodes/<series_id>` | `web/routes/series/watch.py:764` |
| `POST` | `/api/watch/episodes/<series_id>/refresh` | `web/routes/series/watch.py:898` |
| `GET` | `/api/watch/history` | `web/routes/series/track.py:482` |
| `GET` | `/api/watch/local` | `web/routes/series/watch.py:522` |
| `POST` | `/api/watch/log/end` | `web/routes/series/track.py:472` |
| `GET` | `/api/watch/log/history` | `web/routes/series/track.py:490` |
| `POST` | `/api/watch/log/start` | `web/routes/series/track.py:458` |
| `GET` | `/api/watch/probe` | `web/routes/series/watch.py:278` |
| `GET` | `/api/watch/progress` | `web/routes/series/track.py:58` |
| `POST` | `/api/watch/progress` | `web/routes/series/track.py:69` |
| `GET` | `/api/watch/progress/all` | `web/routes/series/track.py:86` |
| `POST` | `/api/watch/progress/delete` | `web/routes/series/track.py:205` |
| `GET` | `/api/watch/proxy/<path:stream_path>` | `web/routes/series/watch.py:345` |
| `GET` | `/api/watch/remux/<path:stream_path>` | `web/routes/series/watch.py:424` |
| `GET` | `/api/watch/stream-url` | `web/routes/series/watch.py:147` |
| `GET` | `/api/watch/stream/<session_id>/<path:filename>` | `web/routes/series/track.py:346` |
| `POST` | `/api/watch/stream/start` | `web/routes/series/track.py:218` |
| `POST` | `/api/watch/stream/stop` | `web/routes/series/track.py:323` |
| `GET` | `/api/watch/transcode` | `web/routes/series/watch.py:541` |
| `POST` | `/api/watch/transcode/cancel` | `web/routes/series/watch.py:573` |
| `POST` | `/api/watch/transcode/prepare` | `web/routes/series/watch.py:554` |
| `GET` | `/api/watch/transcode/status` | `web/routes/series/watch.py:586` |
| `GET` | `/help` | `web/routes/series/list.py:365` |

## web/routes/settings

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/browse-dirs` | `web/routes/settings/public.py:176` |
| `GET` | `/api/browse/<section_id>` | `web/routes/settings/section_config.py:347` |
| `GET` | `/api/known_values` | `web/routes/settings/public.py:310` |
| `GET` | `/api/section_breakdown` | `web/routes/settings/section_config.py:270` |
| `GET` | `/api/settings` | `web/routes/settings/public.py:67` |
| `POST` | `/api/settings` | `web/routes/settings/public.py:76` |
| `POST` | `/api/settings/excluded_countries` | `web/routes/settings/section_config.py:68` |
| `POST` | `/api/settings/excluded_genres` | `web/routes/settings/section_config.py:91` |
| `POST` | `/api/settings/excluded_keywords` | `web/routes/settings/section_config.py:38` |
| `POST` | `/api/settings/excluded_languages` | `web/routes/settings/section_config.py:114` |
| `POST` | `/api/settings/pre_rejected_keywords` | `web/routes/settings/section_config.py:137` |
| `POST` | `/api/settings/section_exclusions` | `web/routes/settings/section_config.py:166` |
| `POST` | `/api/settings/section_filter` | `web/routes/settings/section_config.py:202` |
| `POST` | `/api/settings/stale_sections` | `web/routes/settings/section_config.py:248` |
| `POST` | `/api/upload-csv` | `web/routes/settings/public.py:288` |
| `GET` | `/settings` | `web/routes/settings/public.py:28` |

## web/routes/social.py

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/social/feed` | `web/routes/social.py:85` |

## web/routes/social_badge.py

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/social/badge` | `web/routes/social_badge.py:63` |
| `POST` | `/api/social/badge/reset` | `web/routes/social_badge.py:100` |

## web/routes/system

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/active-holiday` | `web/routes/system/holidays.py:71` |
| `GET` | `/api/auto-maintenance-status` | `web/routes/system/maintenance.py:68` |
| `GET` | `/api/bandwidth` | `web/routes/system/bandwidth.py:18` |
| `GET` | `/api/bandwidth/day` | `web/routes/system/bandwidth.py:79` |
| `GET` | `/api/bandwidth/history` | `web/routes/system/bandwidth.py:66` |
| `POST` | `/api/client-log` | `web/routes/system/dashboard.py:17` |
| `POST` | `/api/covers/repair-missing` | `web/routes/system/cover_repair.py:52` |
| `GET` | `/api/css-compare` | `web/routes/system/themes.py:102` |
| `GET` | `/api/dashboard/snapshot` | `web/routes/system/snapshot.py:112` |
| `GET` | `/api/disk_usage` | `web/routes/system/disk_scan.py:29` |
| `GET` | `/api/download-folders` | `web/routes/system/bandwidth.py:88` |
| `GET` | `/api/download-stats` | `web/routes/system/download_stats.py:18` |
| `GET` | `/api/downloads/view` | `web/routes/system/dashboard.py:161` |
| `POST` | `/api/fingerprint/backfill` | `web/routes/system/maintenance.py:219` |
| `GET` | `/api/fingerprint/status` | `web/routes/system/maintenance.py:243` |
| `GET` | `/api/gone-items` | `web/routes/system/gone_items.py:55` |
| `POST` | `/api/gone-items/action` | `web/routes/system/gone_items.py:165` |
| `GET` | `/api/holiday-image-choices` | `web/routes/system/holidays.py:245` |
| `POST` | `/api/holiday-image-choices` | `web/routes/system/holidays.py:257` |
| `GET` | `/api/holidays/list` | `web/routes/system/holidays.py:77` |
| `GET` | `/api/imdb-trailer/<imdb_id>` | `web/routes/system/trailers.py:19` |
| `POST` | `/api/integrity/action` | `web/routes/system/integrity.py:42` |
| `POST` | `/api/integrity/action-all` | `web/routes/system/integrity_control.py:114` |
| `GET` | `/api/integrity/active` | `web/routes/system/integrity_control.py:53` |
| `GET` | `/api/integrity/issues` | `web/routes/system/integrity.py:20` |
| `GET` | `/api/integrity/progress` | `web/routes/system/integrity_control.py:65` |
| `POST` | `/api/integrity/trigger-resume` | `web/routes/system/integrity_control.py:168` |
| `POST` | `/api/iptv/resolve-domains` | `web/routes/system/iptv_test.py:194` |
| `POST` | `/api/iptv/test` | `web/routes/system/iptv_test.py:157` |
| `GET` | `/api/log` | `web/routes/system/logs.py:871` |
| `GET` | `/api/logs` | `web/routes/system/logs.py:857` |
| `GET` | `/api/logs/full` | `web/routes/system/stats.py:43` |
| `GET` | `/api/my-remote-info` | `web/routes/system/telemetry_remote.py:39` |
| `POST` | `/api/plex/connect` | `web/routes/system/plex.py:418` |
| `POST` | `/api/plex/disconnect` | `web/routes/system/plex.py:446` |
| `GET` | `/api/plex/status` | `web/routes/system/plex.py:395` |
| `GET` | `/api/plex/users` | `web/routes/system/plex.py:402` |
| `GET` | `/api/section-countries` | `web/routes/system/bandwidth.py:38` |
| `GET` | `/api/section-genres` | `web/routes/system/bandwidth.py:24` |
| `GET` | `/api/section-years` | `web/routes/system/bandwidth.py:52` |
| `POST` | `/api/shutdown` | `web/routes/system/shutdown.py:18` |
| `GET` | `/api/stats` | `web/routes/system/stats.py:18` |
| `GET` | `/api/sync/live-stats` | `web/routes/system/heartbeat.py:18` |
| `GET` | `/api/sync/view` | `web/routes/system/dashboard.py:54` |
| `GET` | `/api/sys/docker-push-log` | `web/routes/system/maintenance.py:134` |
| `POST` | `/api/sys/integrity` | `web/routes/system/sync_control.py:42` |
| `GET` | `/api/sys/iptv_stats` | `web/routes/system/iptv_stats.py:6` |
| `POST` | `/api/sys/kill` | `web/routes/system/kill.py:280` |
| `POST` | `/api/sys/refresh-omdb` | `web/routes/system/maintenance.py:36` |
| `GET` | `/api/sys/refresh-omdb-log` | `web/routes/system/maintenance.py:54` |
| `POST` | `/api/sys/start_dl` | `web/routes/system/kill.py:364` |
| `GET` | `/api/sys/status` | `web/routes/system/sync_control.py:107` |
| `POST` | `/api/sys/stop_dl` | `web/routes/system/kill.py:330` |
| `POST` | `/api/sys/sync` | `web/routes/system/sync_control.py:19` |
| `POST` | `/api/sys/sync_section` | `web/routes/system/sync_control.py:62` |
| `GET` | `/api/sys/sync_status` | `web/routes/system/sync_control.py:101` |
| `POST` | `/api/telemetry/cmd/local` | `web/routes/system/telemetry_cmd.py:110` |
| `GET` | `/api/telemetry/cmd/result` | `web/routes/system/telemetry_cmd.py:140` |
| `POST` | `/api/telemetry/cmd/send` | `web/routes/system/telemetry_cmd.py:22` |
| `POST` | `/api/telemetry/device-alias` | `web/routes/system/telemetry_alias.py:14` |
| `DELETE` | `/api/telemetry/device/<device_id>` | `web/routes/system/telemetry_remote.py:145` |
| `GET` | `/api/telemetry/devices` | `web/routes/system/telemetry_devices.py:130` |
| `GET` | `/api/telemetry/history` | `web/routes/system/telemetry_history.py:16` |
| `POST` | `/api/telemetry/provision` | `web/routes/system/telemetry_alias.py:56` |
| `GET` | `/api/telemetry/reports` | `web/routes/system/telemetry_history.py:43` |
| `POST` | `/api/telemetry/set-remote-password` | `web/routes/system/telemetry_remote.py:20` |
| `POST` | `/api/telemetry/tunnel` | `web/routes/system/telemetry_tunnel.py:18` |
| `POST` | `/api/telemetry/tunnel/allocate` | `web/routes/system/telemetry_tunnel.py:50` |
| `POST` | `/api/telemetry/tunnel/authorize` | `web/routes/system/telemetry_tunnel.py:104` |
| `GET` | `/api/telemetry/tunnel/registry` | `web/routes/system/telemetry_tunnel.py:162` |
| `GET` | `/api/theme-preview-full/<theme_name>` | `web/routes/system/themes.py:215` |
| `GET` | `/api/theme-preview/<theme_id>` | `web/routes/system/themes.py:18` |
| `GET` | `/api/themes` | `web/routes/system/themes.py:187` |
| `POST` | `/api/themes/activate` | `web/routes/system/themes.py:199` |
| `GET` | `/api/themes/picker` | `web/routes/system/themes.py:272` |
| `GET` | `/api/tmdb-images/<imdb_id>` | `web/routes/system/tmdb.py:24` |
| `GET` | `/api/tmdb-proxy/<path:tmdb_path>` | `web/routes/system/tmdb.py:41` |
| `GET` | `/api/unlinked` | `web/routes/system/unlinked.py:39` |
| `GET` | `/api/unlinked/candidates` | `web/routes/system/unlinked.py:140` |
| `POST` | `/api/unlinked/ignore` | `web/routes/system/unlinked.py:463` |
| `POST` | `/api/unlinked/link` | `web/routes/system/unlinked.py:177` |
| `POST` | `/api/upgrade-cover` | `web/routes/system/tmdb.py:98` |
| `GET` | `/api/watched/view` | `web/routes/system/dashboard.py:334` |
| `GET` | `/api/watchlist-tracker` | `web/routes/system/holidays.py:104` |
| `POST` | `/api/watchlist-tracker/schedule/queue` | `web/routes/system/holidays.py:230` |
| `GET` | `/static/themes/<theme_name>/css/<path:filename>` | `web/routes/system/themes.py:252` |
| `GET` | `/static/themes/<theme_name>/js/<path:filename>` | `web/routes/system/themes.py:262` |

## web/routes/trash

| Methods | Route | Source |
|---|---|---|
| `POST` | `/api/convert-covers-webp` | `web/routes/trash/covers.py:362` |
| `GET` | `/api/covers/jpg-count` | `web/routes/trash/covers.py:342` |
| `GET` | `/api/covers/recent-upgrades` | `web/routes/trash/covers.py:36` |
| `POST` | `/api/covers/scan` | `web/routes/trash/covers.py:296` |
| `POST` | `/api/repair-covers` | `web/routes/trash/covers.py:62` |
| `GET` | `/api/search` | `web/routes/trash/search.py:52` |
| `GET` | `/api/search/continue-watching` | `web/routes/trash/search.py:198` |
| `GET` | `/api/search/iptv` | `web/routes/trash/iptv_search.py:12` |
| `POST` | `/api/search/iptv/refresh` | `web/routes/trash/iptv_search.py:104` |
| `GET` | `/api/search/iptv/status` | `web/routes/trash/iptv_search.py:92` |
| `GET` | `/api/search/preview/<sid>` | `web/routes/trash/search.py:231` |
| `GET` | `/api/search/suggest` | `web/routes/trash/search.py:12` |
| `GET` | `/api/search/trending` | `web/routes/trash/search.py:163` |
| `GET` | `/api/trash` | `web/routes/trash/bin.py:22` |
| `GET` | `/api/trash/count` | `web/routes/trash/bin.py:15` |
| `POST` | `/api/trash/delete` | `web/routes/trash/bin.py:35` |
| `POST` | `/api/trash/restore` | `web/routes/trash/bin.py:47` |
| `POST` | `/api/upgrade-covers` | `web/routes/trash/covers.py:162` |
| `GET` | `/api/upgrade-covers-log` | `web/routes/trash/covers.py:282` |

## web/routes/update.py

| Methods | Route | Source |
|---|---|---|
| `POST` | `/api/check-update` | `web/routes/update.py:191` |
| `GET` | `/api/heartbeat` | `web/routes/update.py:70` |
| `GET` | `/api/runtime/status` | `web/routes/update.py:77` |
| `GET` | `/api/tools/status` | `web/routes/update.py:83` |
| `GET` | `/api/update-available` | `web/routes/update.py:127` |
| `GET` | `/api/update-package` | `web/routes/update.py:90` |

## web/routes/vpn.py

| Methods | Route | Source |
|---|---|---|
| `GET` | `/api/vpn/status` | `web/routes/vpn.py:16` |
