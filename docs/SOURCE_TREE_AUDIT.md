# Source Tree Audit

Generated from the local IPTV Manager source tree on 2026-04-29. This public docs repo does not contain the private development source, so this file records the inspected tree and the role of each relevant file group.

## High-Level Tree

| Path | Role |
|---|---|
| `series_manager_web.py` | Flask/Cheroot entry point and static/remote compatibility routes |
| `web/` | Web package: app helpers, recurring tasks, auth, diagnostics, routes, Plex tracking |
| `web/routes/` | Blueprint route modules for dashboard, series, settings, system, live, discovery, trash, repair, updates, remote, PWA |
| `admin/routes/` | Admin-only database/export/publish surfaces |
| `db/` | SQLite schema, migrations, config store, media, decisions, downloads, trash, search, tracking, integrity |
| `sync/` | Provider fetch, metadata enrichment, covers, IMDb watchlist, episode schedules, staged sync pipeline |
| `downloader/` | aria2c integration, queue building, limits, metadata tagging, integrity cooperation, phased downloader flow |
| `static/js/modules/features/` | Modular dashboard frontend features |
| `static/js/settings/` | Modular Settings frontend features |
| `templates/partials/settings/` | Settings templates split into focused partials |
| `web/plex_tracking/` | Plex data source, sync, store, and reclaim safety helpers |

## Frontend And Settings Files

| File | Role |
|---|---|
| `static/js/modules/features/actors.js` | Actor search, actor photo, and actor media surfaces |
| `static/js/modules/features/bandwidth.js` | Bandwidth charts and history UI |
| `static/js/modules/features/calendar.js` | Activity calendar and agenda |
| `static/js/modules/features/calendar_agenda.js` | Activity calendar and agenda |
| `static/js/modules/features/card_hover_bg.js` | Card hover background/media effects |
| `static/js/modules/features/card_lazy_fallback.js` | Lazy image fallback handling |
| `static/js/modules/features/card_scroll.js` | Card scroll behavior |
| `static/js/modules/features/cards.js` | Dashboard card rendering helpers |
| `static/js/modules/features/category_manage.js` | IPTV category add/remove controls |
| `static/js/modules/features/continue_watching.js` | Continue Watching UI |
| `static/js/modules/features/dash_render_dl.js` | Download status card rendering |
| `static/js/modules/features/dash_render_sync.js` | Sync status card rendering |
| `static/js/modules/features/data_fetch.js` | Dashboard API fetch layer |
| `static/js/modules/features/decisions.js` | Accept/reject/watch decision actions |
| `static/js/modules/features/dl_view.js` | Download view interactions |
| `static/js/modules/features/empty_state_watchdog.js` | Empty-state protection |
| `static/js/modules/features/fb_live.js` | Live TV dashboard integration |
| `static/js/modules/features/filter_breakdown.js` | Country/genre/year breakdown charts |
| `static/js/modules/features/filters_ui.js` | Dashboard filters and dropdowns |
| `static/js/modules/features/flex_close.js` | Flex detail close behavior |
| `static/js/modules/features/flex_gallery.js` | TMDB/gallery image handling |
| `static/js/modules/features/flex_muscles.js` | Rich hover/detail behavior |
| `static/js/modules/features/flex_trailer.js` | Trailer loading/playback |
| `static/js/modules/features/gone_items.js` | Gone inbox UI |
| `static/js/modules/features/grid_view.js` | Grid/list layout controls |
| `static/js/modules/features/group_modal.js` | Variant group modal |
| `static/js/modules/features/holidays_check.js` | Holiday theme calculation and activation |
| `static/js/modules/features/holidays_christian_easter.js` | Holiday theme calculation and activation |
| `static/js/modules/features/holidays_christian_saints.js` | Holiday theme calculation and activation |
| `static/js/modules/features/holidays_core.js` | Holiday theme calculation and activation |
| `static/js/modules/features/holidays_islamic.js` | Holiday theme calculation and activation |
| `static/js/modules/features/holidays_misc.js` | Holiday theme calculation and activation |
| `static/js/modules/features/holidays_national.js` | Holiday theme calculation and activation |
| `static/js/modules/features/holidays_ramadan.js` | Holiday theme calculation and activation |
| `static/js/modules/features/init.js` | Dashboard initialization |
| `static/js/modules/features/integrity.js` | Integrity banner/list UI |
| `static/js/modules/features/integrity_actions.js` | Integrity banner/list UI |
| `static/js/modules/features/logs_fetch.js` | Log polling/fetching |
| `static/js/modules/features/logs_render.js` | Log rendering |
| `static/js/modules/features/match.js` | Manual match UI |
| `static/js/modules/features/match_actions.js` | Manual match UI |
| `static/js/modules/features/plex_tracking.js` | Plex tracking dashboard panel |
| `static/js/modules/features/push.js` | Web push subscription UI |
| `static/js/modules/features/remote_cmd.js` | Remote command controls |
| `static/js/modules/features/render_content.js` | Main dashboard content rendering |
| `static/js/modules/features/render_trash.js` | Trash rendering |
| `static/js/modules/features/search_commit.js` | Search, suggestions, preview, recents, and commit behavior |
| `static/js/modules/features/search_dropdown.js` | Search, suggestions, preview, recents, and commit behavior |
| `static/js/modules/features/search_inline.js` | Search, suggestions, preview, recents, and commit behavior |
| `static/js/modules/features/search_iptv.js` | Search, suggestions, preview, recents, and commit behavior |
| `static/js/modules/features/search_preview.js` | Search, suggestions, preview, recents, and commit behavior |
| `static/js/modules/features/search_recents.js` | Search, suggestions, preview, recents, and commit behavior |
| `static/js/modules/features/section_ctrl_browse.js` | Section browse/modal controls |
| `static/js/modules/features/section_ctrl_modal.js` | Section browse/modal controls |
| `static/js/modules/features/series_local_counts.js` | Local/online/future episode counts |
| `static/js/modules/features/social_watch.js` | Social Watch feed and badges |
| `static/js/modules/features/ssh_state.js` | Admin terminal state/session/actions |
| `static/js/modules/features/ssh_terminal_actions.js` | Admin terminal state/session/actions |
| `static/js/modules/features/ssh_terminal_open.js` | Admin terminal state/session/actions |
| `static/js/modules/features/ssh_terminal_session.js` | Admin terminal state/session/actions |
| `static/js/modules/features/stats_panel.js` | System statistics panel |
| `static/js/modules/features/sync_section.js` | Section sync trigger |
| `static/js/modules/features/sync_view.js` | Sync view rendering |
| `static/js/modules/features/system_actions.js` | Manual system actions |
| `static/js/modules/features/tabs.js` | Section/status tab behavior |
| `static/js/modules/features/telemetry_card.js` | Connected device cards, history, panel, and device state |
| `static/js/modules/features/telemetry_device.js` | Connected device cards, history, panel, and device state |
| `static/js/modules/features/telemetry_history.js` | Connected device cards, history, panel, and device state |
| `static/js/modules/features/telemetry_panel.js` | Connected device cards, history, panel, and device state |
| `static/js/modules/features/theme.js` | Theme switching |
| `static/js/modules/features/typewriter.js` | Small text animation helper |
| `static/js/modules/features/unlinked.js` | Unlinked-media UI |
| `static/js/settings/backups.js` | Settings page JavaScript module |
| `static/js/settings/browse.js` | Settings page JavaScript module |
| `static/js/settings/core.js` | Settings page JavaScript module |
| `static/js/settings/database.js` | Settings page JavaScript module |
| `static/js/settings/filters.js` | Settings page JavaScript module |
| `static/js/settings/general.js` | Settings page JavaScript module |
| `static/js/settings/iptv_resolver.js` | Settings page JavaScript module |
| `static/js/settings/keywords.js` | Settings page JavaScript module |
| `static/js/settings/maintenance.js` | Settings page JavaScript module |
| `static/js/settings/plex.js` | Settings page JavaScript module |
| `static/js/settings/publish.js` | Settings page JavaScript module |
| `static/js/settings/themes_browser.js` | Theme switching |
| `templates/partials/settings/backups_panel.html` | Settings page partial template |
| `templates/partials/settings/browse_panel.html` | Settings page partial template |
| `templates/partials/settings/database_panel.html` | Settings page partial template |
| `templates/partials/settings/exclusions_panel.html` | Settings page partial template |
| `templates/partials/settings/filters_panel.html` | Settings page partial template |
| `templates/partials/settings/general/api_keys.html` | Settings page partial template |
| `templates/partials/settings/general/download_limits.html` | Settings page partial template |
| `templates/partials/settings/general/download_settings.html` | Settings page partial template |
| `templates/partials/settings/general/iptv_connection.html` | Settings page partial template |
| `templates/partials/settings/general/series_stale.html` | Settings page partial template |
| `templates/partials/settings/general/theme_mode.html` | Theme switching |
| `templates/partials/settings/general_panel.html` | Settings page partial template |
| `templates/partials/settings/head_inline_styles.html` | Settings page partial template |
| `templates/partials/settings/imdb_help_popup.html` | Settings page partial template |
| `templates/partials/settings/keywords_panel.html` | Settings page partial template |
| `templates/partials/settings/maintenance_panel.html` | Settings page partial template |
| `templates/partials/settings/plex_panel.html` | Settings page partial template |
| `templates/partials/settings/publish_panel.html` | Settings page partial template |
| `templates/partials/settings/remote_panel.html` | Settings page partial template |
| `templates/partials/settings/tabs_row.html` | Section/status tab behavior |
| `templates/partials/settings/theme_inline_script.html` | Theme switching |
| `templates/partials/settings/themes_panel.html` | Theme switching |

## Route Files

| File | Role |
|---|---|
| `web/routes/__init__.py` | Project source file inspected for documentation scope |
| `web/routes/_remote_tokens.py` | Project source file inspected for documentation scope |
| `web/routes/actors.py` | Actor search, actor photo, and actor media surfaces |
| `web/routes/backups.py` | Project source file inspected for documentation scope |
| `web/routes/discovery/__init__.py` | Disk discovery route module |
| `web/routes/discovery/count.py` | Disk discovery route module |
| `web/routes/discovery/episodes.py` | Disk discovery route module |
| `web/routes/discovery/helpers.py` | Disk discovery route module |
| `web/routes/discovery/ignore.py` | Disk discovery route module |
| `web/routes/discovery/link.py` | Disk discovery route module |
| `web/routes/discovery/merge.py` | Disk discovery route module |
| `web/routes/discovery/scan.py` | Disk discovery route module |
| `web/routes/discovery/search.py` | Search, suggestions, preview, recents, and commit behavior |
| `web/routes/live.py` | Project source file inspected for documentation scope |
| `web/routes/micky.py` | Project source file inspected for documentation scope |
| `web/routes/plex_tracking.py` | Plex tracking dashboard panel |
| `web/routes/pwa.py` | Project source file inspected for documentation scope |
| `web/routes/remote.py` | Project source file inspected for documentation scope |
| `web/routes/repair/__init__.py` | Admin repair and terminal route module |
| `web/routes/repair/health.py` | Admin repair and terminal route module |
| `web/routes/repair/repair_cmds.py` | Admin repair and terminal route module |
| `web/routes/repair/ssh_core.py` | Admin terminal state/session/actions |
| `web/routes/repair/terminal.py` | Admin repair and terminal route module |
| `web/routes/search_page.py` | Search, suggestions, preview, recents, and commit behavior |
| `web/routes/series/__init__.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/accept.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/batch_reenrich.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/group.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/list.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/local_counts.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/match.py` | Manual match UI |
| `web/routes/series/nav_state.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/playback.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/playback_cache.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/playback_prepare.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/playback_stream.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/playback_tier.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/reject.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/track.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/untrack.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/variants.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/watch.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/series/watch_payload.py` | Series/dashboard API route module for listing, decisions, playback, match, variants, watch, or local counts |
| `web/routes/settings/__init__.py` | Settings page/API route module |
| `web/routes/settings/public.py` | Settings page/API route module |
| `web/routes/settings/section_config.py` | Settings page/API route module |
| `web/routes/social.py` | Project source file inspected for documentation scope |
| `web/routes/social_badge.py` | Project source file inspected for documentation scope |
| `web/routes/system/__init__.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/bandwidth.py` | Bandwidth charts and history UI |
| `web/routes/system/cover_repair.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/dashboard.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/disk_scan.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/download_stats.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/gone_items.py` | Gone inbox UI |
| `web/routes/system/heartbeat.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/holidays.py` | Holiday theme calculation and activation |
| `web/routes/system/integrity.py` | Integrity banner/list UI |
| `web/routes/system/integrity_control.py` | Integrity banner/list UI |
| `web/routes/system/iptv_stats.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/iptv_test.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/kill.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/logs.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/maintenance.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/plex.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/shutdown.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/snapshot.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/stats.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/sync_control.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/telemetry_alias.py` | Connected device cards, history, panel, and device state |
| `web/routes/system/telemetry_cmd.py` | Connected device cards, history, panel, and device state |
| `web/routes/system/telemetry_common.py` | Connected device cards, history, panel, and device state |
| `web/routes/system/telemetry_devices.py` | Connected device cards, history, panel, and device state |
| `web/routes/system/telemetry_history.py` | Connected device cards, history, panel, and device state |
| `web/routes/system/telemetry_remote.py` | Connected device cards, history, panel, and device state |
| `web/routes/system/telemetry_tunnel.py` | Connected device cards, history, panel, and device state |
| `web/routes/system/themes.py` | Theme switching |
| `web/routes/system/tmdb.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/tmdb_prefetch.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/trailers.py` | System API route module for logs, stats, telemetry, themes, integrity, sync, kill, Plex, TMDB, or maintenance |
| `web/routes/system/unlinked.py` | Unlinked-media UI |
| `web/routes/trash/__init__.py` | Trash/search/cover recovery route module |
| `web/routes/trash/bin.py` | Trash/search/cover recovery route module |
| `web/routes/trash/covers.py` | Trash/search/cover recovery route module |
| `web/routes/trash/iptv_search.py` | Trash/search/cover recovery route module |
| `web/routes/trash/search.py` | Search, suggestions, preview, recents, and commit behavior |
| `web/routes/update.py` | Project source file inspected for documentation scope |
| `web/routes/vpn.py` | Project source file inspected for documentation scope |
| `admin/routes/__init__.py` | Admin-only database, export, or publish route module |
| `admin/routes/_test_fixture_do_not_ship.py` | Admin-only database, export, or publish route module |
| `admin/routes/database_ops.py` | Admin-only database, export, or publish route module |
| `admin/routes/export.py` | Admin-only database, export, or publish route module |
| `admin/routes/export_support.py` | Admin-only database, export, or publish route module |
| `admin/routes/export_windows.py` | Admin-only database, export, or publish route module |
| `admin/routes/publish.py` | Admin-only database, export, or publish route module |
| `admin/routes/publish_channels.py` | Admin-only database, export, or publish route module |
| `admin/routes/publish_release_notes.py` | Admin-only database, export, or publish route module |
| `admin/routes/publish_runtime.py` | Admin-only database, export, or publish route module |
| `admin/routes/publish_support.py` | Admin-only database, export, or publish route module |

## DB Sync Downloader Plex Files

| File | Role |
|---|---|
| `db/__init__.py` | SQLite schema, migration, query, or persistence helper |
| `db/_columns.py` | SQLite schema, migration, query, or persistence helper |
| `db/_core.py` | SQLite schema, migration, query, or persistence helper |
| `db/_migrations.py` | SQLite schema, migration, query, or persistence helper |
| `db/_migrations_additive.py` | SQLite schema, migration, query, or persistence helper |
| `db/_migrations_disk.py` | SQLite schema, migration, query, or persistence helper |
| `db/_migrations_v1.py` | SQLite schema, migration, query, or persistence helper |
| `db/_row_helpers.py` | SQLite schema, migration, query, or persistence helper |
| `db/_safety.py` | SQLite schema, migration, query, or persistence helper |
| `db/_schema_audit.py` | SQLite schema, migration, query, or persistence helper |
| `db/_schema_sql.py` | SQLite schema, migration, query, or persistence helper |
| `db/cache.py` | SQLite schema, migration, query, or persistence helper |
| `db/config_store.py` | SQLite schema, migration, query, or persistence helper |
| `db/decisions.py` | Accept/reject/watch decision actions |
| `db/disk.py` | SQLite schema, migration, query, or persistence helper |
| `db/download_runtime.py` | SQLite schema, migration, query, or persistence helper |
| `db/downloads.py` | SQLite schema, migration, query, or persistence helper |
| `db/episode_catalog.py` | SQLite schema, migration, query, or persistence helper |
| `db/episode_schedule.py` | SQLite schema, migration, query, or persistence helper |
| `db/integrity.py` | Integrity banner/list UI |
| `db/logs.py` | SQLite schema, migration, query, or persistence helper |
| `db/media.py` | SQLite schema, migration, query, or persistence helper |
| `db/mediafiles.py` | SQLite schema, migration, query, or persistence helper |
| `db/micky.py` | SQLite schema, migration, query, or persistence helper |
| `db/push.py` | Web push subscription UI |
| `db/queries_counts.py` | SQLite schema, migration, query, or persistence helper |
| `db/queries_filters.py` | SQLite schema, migration, query, or persistence helper |
| `db/queries_misc.py` | SQLite schema, migration, query, or persistence helper |
| `db/queries_paginated.py` | SQLite schema, migration, query, or persistence helper |
| `db/recovery.py` | SQLite schema, migration, query, or persistence helper |
| `db/search.py` | Search, suggestions, preview, recents, and commit behavior |
| `db/sections.py` | SQLite schema, migration, query, or persistence helper |
| `db/settings.py` | SQLite schema, migration, query, or persistence helper |
| `db/tracker.py` | SQLite schema, migration, query, or persistence helper |
| `db/trash.py` | SQLite schema, migration, query, or persistence helper |
| `db/watch_history.py` | SQLite schema, migration, query, or persistence helper |
| `db/watchdog.py` | SQLite schema, migration, query, or persistence helper |
| `sync/__init__.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/_api_shape.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/catalog_snapshot.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/context.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/covers.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/episode_schedule.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/imdb_watchlist.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/iptv_bootstrap.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/iptv_runtime.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/naming.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/omdb.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/omdb_format.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/pipeline.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/rescan.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/__init__.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage1_config.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage2_prefilter.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage4_repair.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage5_watchdog.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage5b_watched.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage5c_override.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage5d_xstate.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage5e_bulk.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage6_enrich.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage6_section_loop.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage_heal.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage_maint.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage_preaccept.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage_purge.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/stages/stage_summary.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `sync/watchdog.py` | Sync pipeline, IPTV runtime, metadata, naming, covers, or stage helper |
| `downloader/__init__.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/__init__.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/aria2.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/download_results.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/downloads.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/duplicates.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/filename.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/metadata.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/runtime.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/core/sections.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/integrity/__init__.py` | Integrity banner/list UI |
| `downloader/integrity/consistency.py` | Integrity banner/list UI |
| `downloader/integrity/ffprobe.py` | Integrity banner/list UI |
| `downloader/integrity/scan_ops.py` | Integrity banner/list UI |
| `downloader/integrity/size_check.py` | Integrity banner/list UI |
| `downloader/integrity/tag_files.py` | Integrity banner/list UI |
| `downloader/integrity/tag_link_helpers.py` | Integrity banner/list UI |
| `downloader/main/__init__.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/phase_a/__init__.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/phase_a/drain.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/phase_b/__init__.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/phase_b/downloads.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/queue/__init__.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/queue/build.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/queue/cooldown.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/queue/limits.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/queue/movies.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `downloader/main/queue/series.py` | Downloader queue, aria2c, limits, metadata, integrity, or phase helper |
| `web/plex_tracking/__init__.py` | Plex tracking dashboard panel |
| `web/plex_tracking/datasource.py` | Plex tracking dashboard panel |
| `web/plex_tracking/reclaim.py` | Plex tracking dashboard panel |
| `web/plex_tracking/store.py` | Plex tracking dashboard panel |
| `web/plex_tracking/sync.py` | Plex tracking dashboard panel |
