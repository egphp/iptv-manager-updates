# Last Month Changelog

Generated from the development source repository on 2026-04-29 for commits since 2026-03-29. This is a public documentation inventory of work completed during the last month; it lists commit subjects only, not runtime values.

## Thematic Summary

| Theme | Work Captured |
|---|---|
| Plex tracking and reclaim | Plex Connect settings, home user watch activity, watch-state sync, safe reclaim decisions, future episode blocking |
| Local playback and VOD | Tiered playback, older ffmpeg progress support, transcode preparation progress, cache guardrails, Safari/iOS playback fixes |
| Disk discovery and identity | Manual link/merge, folder identity, disk path state by device, duplicate repair, path drift fixes, Arabic/noisy filename matching |
| Gone inbox and trash | User-driven provider-missing review, swap/trash/ignore, trash restore fixes, restore metadata protection |
| Integrity and downloader | Partial resume, smart restart, queue limits, global queue, aria2c retries, tagger safeguards, stalled process control |
| Settings and filters | Section filters, exclusions, stale detection, download limits, settings split into partials, database browser improvements |
| Connected devices and remote ops | Telemetry, aliases, disconnected devices, mobile device panels, update history, relay/repair workflows |
| Publish/update/runtime | GitHub release packages, managed Python/runtime, toolchain updates, package manifests, mirror upload hardening |
| UI and frontend structure | Dashboard/template decomposition, modular JS, mobile layout passes, hover cards, Flex detail, logs, stats, calendar |
| Themes and PWA | Egyptian holiday themes, Coptic/national/seasonal themes, PWA icons/service worker, certificate install flow |
| Search/social/live | FTS autocomplete, Social Watch, push events, Live TV playback, live logs, category exclusions |

## Commit Inventory By Date

### 2026-04-29

| Commit | Subject |
|---|---|
| `bf6b5470` | chore: bump version to 3.5.599 |
| `02fa4d03` | docs: add Plex tracking workflow memory |
| `74339ac2` | feat: add Plex tracking and safe disk discovery |
| `7ae33767` | chore: bump version to 3.5.598 |
| `47fac7d7` | fix(vod): parse legacy ffmpeg progress |
| `f08f65a2` | chore: bump version to 3.5.597 |
| `e242c2d2` | fix(vod): support older ffmpeg progress |
| `192f126b` | chore: bump version to 3.5.596 |
| `578b50da` | fix(vod): show transcode prepare progress |
| `24748dd4` | chore: bump version to 3.5.595 |
| `b4f80810` | fix(vod): prepare legacy local transcodes |
| `5744849c` | fix(update): preflight python dependencies |
| `11dcb5fd` | fix(vod): avoid startup crash without psutil |
| `79fb67b0` | Bump app version to 3.5.594 |
| `16437395` | feat(vod): unlock seeking after transcode cache |
| `b938c527` | feat(vod): tier local playback safely |
| `e721c12d` | chore(runtime): add psutil for playback guards |
| `cf16ad12` | Bump app version to 3.5.593 |
| `c8e74333` | Persist remote dashboard login session values |
| `131034dd` | Bump app version to 3.5.592 |
| `f0b2174b` | Make static gzip generation deterministic |
| `24024761` | Bump app version to 3.5.591 |
| `c769116f` | Add managed runtime and toolchain updates |
| `a8b96a03` | Fix discovered duplicate disk identity repair |
| `0a7251a5` | Bump app version to 3.5.590 |
| `4f2d7591` | Show Plex home user watch activity |
| `891b593e` | Reduce log polling CPU load |
| `9e9d4840` | Fix numbered sequence disk matching loops |

### 2026-04-28

| Commit | Subject |
|---|---|
| `2728049e` | Bump app version to 3.5.589 |
| `fd734804` | Show Continue Watching episode and last opened time |
| `0b0f1075` | Bump app version to 3.5.588 |
| `2c82f59a` | Hide zero sub-tabs and speed count badges |
| `b85c5d72` | Bump app version to 3.5.587 |
| `787b8c61` | Fix skip-enrich sections and matcher UX |
| `aa691b7f` | Save client DB recovery memory |
| `a8cd3e5c` | Bump app version to 3.5.586 |
| `92effcee` | Fix DB recovery and matcher filter regressions |
| `56cb8bac` | Bump app version to 3.5.584 |
| `3c060f93` | Make Plex Connect available to all devices |
| `61bda8e1` | Bump app version to 3.5.583 |
| `f50fb9a9` | Remove hardcoded IPTV resolver domains |
| `872f9c17` | Add Plex Connect settings |
| `710b1011` | Add IPTV domain resolver button |
| `640b8b4f` | Fix match path identity and cover repair |
| `ba320574` | Identity Drift Hardening: stable folder + manual match + cover hash + per-season dismiss |
| `efdfd769` | Bump version to 3.5.581 |
| `9cc7afe2` | Hide merged discovered variants from matcher |

### 2026-04-27

| Commit | Subject |
|---|---|
| `96717e7b` | Bump version to 3.5.580 |
| `04a5712b` | Fix social metadata hydration and matcher disk merges |
| `f6a008c3` | Bump version to 3.5.579 |
| `a1d46441` | Repair automatic disk media linking |
| `e723754f` | Bump version to 3.5.578 |
| `d3f28261` | Repair empty cartoon section path |
| `9e8c5e3b` | Bump version to 3.5.577 |
| `5bd71832` | Skip integrity remote checks for local disk links |
| `65c4cee2` | Repair disk reconcile for existing PPETO media |
| `1d5777d8` | Update Codex memory for 3.5.575 |
| `273731c5` | Bump version to 3.5.575 |
| `99f3b130` | Fix mobile card grids and push deep links |
| `8af97e54` | Bump version to 3.5.574 |
| `898f3313` | Fix automatic series queue waiting states |
| `8b138faf` | Bump version to 3.5.573 |
| `97ac30b5` | Replace legacy 8888 dashboard references |
| `fce80024` | Fix series badge refresh and stale aria2 cleanup |
| `ef72df7b` | Improve series download and publish update flow |

### 2026-04-26

| Commit | Subject |
|---|---|
| `a3f220af` | Save session memory notes |
| `163fd37e` | Bump app version after publish |
| `a5baa886` | Fix settings tab owner actions |
| `63f63a22` | Bump app version after publish |
| `16bb59b3` | Fix settings owner access field visibility |
| `a260638f` | Fix client settings access field handling |
| `920142c3` | Harden downloader bootstrap fallback |
| `4ae7d994` | Bootstrap-once IPTV API policy + call counter (v3.5.565) |
| `6b3e7bfc` | Fix downloader lock path + idle-but-alive placeholder (v3.5.563) |
| `8bb2782b` | Logs overlay tracks script-running, not just active-downloading (v3.5.562) |
| `dd89febd` | Full Accept-grid reorder by latest episode download (v3.5.561) |
| `495b1da5` | Per-section latest-downloaded scope (v3.5.560) |
| `473d74e0` | Daily catalog refresh + Latest-DL series leads Accept grid (v3.5.559) |
| `7f2e99a6` | VOD episode catalog auto-poll (v3.5.558) |
| `0ab89ff5` | Episode catalog cache + Refresh button (v3.5.557) |
| `ee68c098` | Local-first episodes + ج7 tombstone + Latest-DL highlight (v3.5.556) |
| `65022fca` | Series: cache fallback for /api/watch/episodes + light-theme badge (v3.5.554) |
| `f575b372` | Series badge: split LOCAL + ONLINE counts (v3.5.552) |
| `124d2f9a` | Series: bare-number/E-only fallback + LOCAL/TOTAL badge (v3.5.550) |
| `b3ea7f04` | Social: persistent dedup for badge + push (v3.5.548) |
| `58e22b05` | Unlinked: auto-link sibling files when one is manually linked (v3.5.547) |
| `f009e7bf` | Disk walk: don't overwrite existing sibling locations (v3.5.547) |
| `71a7b1b8` | Scanner: add .rmvb / .wmv / .mov / etc; drop .ts (subtitle) (v3.5.547) |
| `5598b1ed` | Disk walk: claim files for already-seen media (v3.5.547) |
| `d2436efc` | Disk walk: pin sibling variants to shared folder (v3.5.547) |
| `82f953f2` | Social push: persistent suppression via social_pushed table (v3.5.547) |
| `0b227d99` | Disk walk: transaction-based persistence + Arabic match (Bug M, v3.5.547) |
| `9edade5a` | Disk-walk reconcile + folder-aware episode key (Bug L, v3.5.546) |
| `4831ac63` | Reconcile orphan claims + dashboard visibility (Bug K2, v3.5.544) |
| `746b5246` | Bump APP_VERSION to v3.5.543 |
| `418dab90` | Auto-recover claim from existing mkv tags (Bug K, v3.5.542) |
| `301e826c` | Bump APP_VERSION to v3.5.541 |
| `f2fcc358` | 9-bug fix batch: drain races, zombie integrity, trash JSON, VOD kill, matcher (v3.5.540) |
| `fc1a0350` | Bump APP_VERSION to v3.5.538 |
| `be3ab4f1` | Dedupe tagger runs per cron tick + early lock check (v3.5.537) |
| `adb3f88e` | Tagger fast-skip + ghost-season cleanup + API cache (v3.5.535) |
| `9155cc48` | Bump APP_VERSION to v3.5.533 |
| `7011dede` | System Logs auto-refresh no longer flashes (v3.5.532) |
| `0251ced9` | Bump APP_VERSION to v3.5.531 |
| `552a8563` | Fix System Logs auto-refresh wiring (v3.5.530) |
| `2667fd1b` | Nested-folder matching + ghost-series prevention (v3.5.529) |
| `14070bd7` | Bump APP_VERSION to v3.5.528 |
| `bbfa52fb` | Discover-before-gate + modal UX overhaul (v3.5.527) |
| `59648f91` | Block dl/integrity on unlinked + warning banner + push (v3.5.525) |
| `1c8611a6` | Manual linking popup for unmatchable disk files (v3.5.524) |
| `fa58c0a9` | Phase A drain: verify pct on rc=0 + reopen stuck resumed (v3.5.520) |
| `cbb2368c` | Keep series mediafiles at 'accepted' after episode complete (v3.5.518) |
| `083d6baf` | Stop infinite re-tag of MKV files mkvpropedit refuses (v3.5.516) |
| `e11b2b63` | Fix silent skip of Accepted series + kill IPTV cache + live logs (v3.5.514) |
| `61bdb913` | Manual download: bypass cache + clear guard (v3.5.512) |

### 2026-04-25

| Commit | Subject |
|---|---|
| `a4502880` | Document push-notification rules in CLAUDE.md |
| `566e8169` | Push notifications: download-complete + Social new-content (v3.5.510) |
| `10f91ef2` | Persistent sessions + VAPID auto-gen + push consolidation (v3.5.509) |
| `d531925a` | Push notifications: session value refresh + new-eps for excluded series (v3.5.508) |
| `8656e3a3` | Bump APP_VERSION to v3.5.507 |
| `7cd14346` | Extend remote login session to 30 days |
| `04ca3286` | Document Social Watch two-tier allowlist (v3.5.506) |
| `47713ef3` | Social Watch: stale-cutoff fallback + split social.py (v3.5.505) |
| `cd52fbe3` | Social Watch: gate feed on Connected Devices allowlist (v3.5.503) |
| `68773da8` | Rebuild bundled .gz assets for v3.5.502 |
| `0eaaeaa0` | Drop HTTP heartbeat self-kill from tunnel Phase 2 loop (v3.5.502) |
| `64700c73` | Bump APP_VERSION to v3.5.501 — TCP-only tunnel healthcheck |
| `2bc3016d` | Fix accepted card rendering and tunnel health checks |

### 2026-04-24

| Commit | Subject |
|---|---|
| `a5fc0bc0` | Rebuild bundled .gz assets + APP_VERSION for v3.5.500 |
| `0ec939a7` | Allow manual /api/check-update for authenticated remote sessions |
| `4d303197` | Rebuild bundled .gz assets + bump APP_VERSION for v3.5.499 |
| `c7471ca7` | Social: drop overzealous orphan-self subset + fix _not_mine rename |
| `73d61665` | Social feed: purge stale self-hash twins + duplicate-identity devices |
| `55701b0c` | Tag reject decisions with actor (device + host + IP) for audit trail |
| `1c9d7836` | stage_purge: silently drop pending media gone from IPTV |
| `697678af` | Revert debug trace in remote-login after root cause fixed |
| `be59484f` | Debug: add trace logs to remote-login path |
| `7dfcdff2` | Debug: log remote-login entry to trace 302-no-cookie on external POST |
| `fe36a4c7` | Fix WS SSL verify failure on self-signed :8765 relay cert |
| `b38737a5` | Harden _diag_id stability + auto-merge twin device entries |
| `55734b5b` | Fix: self-heal WS cmd_private marker + stabilise _diag_id + honest repair terminal fallback |
| `e872ce23` | Restore accepted visibility for downloaded items |
| `4ede5370` | Fix downloader sync and refresh bundled assets |
| `63831b97` | Advisor P1-P3 follow-ups: close remaining audit gaps |
| `f88b3dac` | Test-driven follow-ups from comprehensive API test sweep |
| `26c511d7` | Advisor revisions: honest labels on hardening |
| `7fcf63f5` | Audit fixes Wave C: hardening + defensive guards |
| `28d737b3` | Audit fixes: 10 concrete bugs from 2026-04-24 audit |
| `bada8b64` | Audit re-pass: tighten severity on areas 1, 5, 7, 9 |
| `b9a22e95` | Add comprehensive Arabic audit report 2026-04-24 |
| `bffaadaa` | Subfolder fallback collision guard + audit-friendly log |
| `7abb36b7` | Fix 3 bugs: subfolder Space Cleanup, OMDb tmdb_id storm, tag log |
| `c9c1dd9f` | Add missing System Logs tabs: Covers, Web, System |
| `1430f464` | Fix matcher-revert loop + clarify unmatched-tag log |
| `49496da5` | Wave 0 bugfixes: .ts files, child sort, null JSON body, admin cache |
| `1cf2cd76` | Wave 0 follow-up: fingerprint reader + admin auth gate |
| `03e2487e` | Wave 0: file fingerprint column + rename-drift anchor |
| `d6bd5d3a` | Fix rename-drift silent re-download bug |
| `2ddfbff0` | Bump app version to 3.5.485 |
| `be45578e` | Dynamic OS icons + duplicate device fix + mobile CSS cascade fixes |

### 2026-04-23

| Commit | Subject |
|---|---|
| `d606ff35` | Bump app version to 3.5.483 |
| `7bc630b4` | TBridge Mac-only tunnel + remote perf pass + duplicate-device fix |
| `90a6e9c6` | Bump app version to 3.5.480 |
| `4d7f753d` | Fix telemetry latestVer: semver max across versions, not first key |
| `4ac04ad6` | Mobile UI polish pass + downloader path identity |
| `25c06405` | Bump app version to 3.5.478 |
| `2aaf339d` | Generalize mobile holiday decorations |
| `cc6e79f4` | Fix trash restore and mobile holiday layout |

### 2026-04-22

| Commit | Subject |
|---|---|
| `cc7a5440` | fix: rollback failed publish releases |
| `9d4dcbd2` | fix: stream publish mirror uploads |
| `f56ae846` | fix: dedupe publish assets |
| `7f503377` | fix: harden publish pipeline |
| `2e58f568` | feat: speed up remote dashboard paging |
| `0ecd6eae` | Bump version to 3.5.473 |
| `03459eed` | Fix excluded-new tab query |
| `54699c96` | Fix client episode catch-up and update permissions |
| `dfea9079` | Refresh generated gzip assets |
| `e1367d0e` | Sync APP_VERSION to v3.5.471 |
| `b91d400f` | Ship current IPTV Manager fixes |

### 2026-04-21

| Commit | Subject |
|---|---|
| `2e383e55` | Refactor dashboard and settings assets, harden discovery merges |
| `54f7b859` | refactor(downloader): split main queue orchestration |
| `fe519f05` | refactor(downloader): split integrity package flows |
| `d8ab9655` | refactor(web): extract app bootstrap runtime helpers |
| `3b4fe460` | refactor(sync): extract update and omdb formatting helpers |
| `dee130cb` | refactor(admin): split publish route helpers |
| `21d65a8e` | refactor(admin): split export route payload builders |
| `2b13499d` | refactor(sync): extract IPTV runtime helpers |
| `389f5cd8` | refactor(web): extract recurring background tasks |
| `9ec57988` | fix: harden local update and telemetry private marker surfaces |
| `68f8b1ca` | chore: bump app version to 3.5.466 |
| `19607b68` | fix: harden linked media ownership across downloader flows |
| `76c2fdf0` | fix: scope integrity scan to downloader-managed media |
| `97662f3f` | fix: respect download limits during integrity drain |
| `2170e407` | fix: repair linked series typing and nested local episodes |
| `e1f008d6` | fix: honor linked series episodes on disk |
| `0f54f60e` | chore: publish current IPTV manager updates |
| `b47e9e2f` | Stabilize tunnel health, static caching, and runtime cleanup |
| `5470704a` | fix: remove paused runtime drift and normalize speed display |
| `4bb8de8d` | fix: keep disk-only links out of gone inbox |
| `824ee11f` | fix: harden shared matcher snapshot apply |
| `c961a211` | fix: wait for graceful process exit in kill truth |
| `01067608` | fix: harden discovery and kill truth for recovery wave |
| `18bcaeb5` | fix: publish versions must advance past latest public tag |
| `ce2a51e0` | fix: repair partial discovery path state backfill |
| `a5b32325` | test: cover native setup and runtime snapshot contracts |
| `894421f8` | fix: stabilize runtime logs and kill-all dashboard state |
| `9c4be07e` | fix: harden matcher cross-section merges |
| `e51e3ad5` | fix: preserve download speed badge casing |
| `61509fa7` | fix: apply published nginx runtime updates on clients |
| `d2a8a5c1` | fix: render cooldown-only downloads as a paused card |
| `cfdec602` | feat: add downloader runtime state and shared iptv snapshots |

### 2026-04-20

| Commit | Subject |
|---|---|
| `1de6558d` | fix: add run-scoped iptv snapshot and cooldown visibility |
| `9277ac8f` | fix: route remaining iptv lookups through shared gate |
| `4ff62bf5` | fix: make tunnel server authoritative end-to-end |
| `23f4c798` | fix: scope disk discovery path state by device |
| `e9fbda4b` | docs: add neighborhood verification protocol |
| `02d89703` | fix: align disk discovery badge with real scan state |
| `5e791f6f` | fix: route remaining iptv metadata flows through shared gate |
| `08048761` | fix: serialize shared iptv metadata requests |
| `aaf041aa` | fix: harden client release export and admin update boundaries |
| `a7fcf948` | fix: harden disk discovery path and matching contracts |
| `3d846167` | fix: unify publish and direct-update package manifests |
| `7b1eac59` | chore: checkpoint current workspace before audit waves |
| `4bc537d0` | fix(tagger): skip corrupted Matroska files so they don't loop every downloader run |
| `152f46d7` | fix: disk discovery picks non-sample feature file + remux-copy fast path + stand-alone DB audit tool |
| `6f87f4ad` | chore: tick APP_VERSION so remote devices re-extract with the new _shared_matches allowlist |
| `59fcc1cb` | chore: sync APP_VERSION to published 3.5.452 |
| `f7d43efd` | feat(matcher-share): admin matcher cache ships in every auto-update zip and auto-fills empty rows on remote devices |
| `6614a258` | chore: sync APP_VERSION to published 3.5.451 |
| `1bdce3be` | fix: MKV tagger skips non-matroska .mkv files + AVI/Xvid online playback via ffmpeg transcode |
| `65736ee3` | chore: sync APP_VERSION to published 3.5.450 |
| `1c186887` | fix: disk-discovery de-duplication, gone-inbox discovered_* skip, nginx errors propagation, richer merge confirm, broader cheroot ssl silencing |
| `7e59da68` | chore: sync APP_VERSION to published 3.5.449 |
| `27eb81e0` | fix(disk-merge): hard-validate path before accepting + downloader skips disk-linked accepted items |
| `1ce65886` | fix(disk-discovery): show absolute path in scan card + clearer merge toast |
| `b62c924e` | chore: sync APP_VERSION to published 3.5.448 |
| `4fd2b302` | fix(disk-discovery): scan TTL cache, ignore persistence, card path badge + cheroot ssl EOF silencing + vod path contrast |
| `1050b621` | feat(gone-inbox): replace silent auto-swap + silent delete with user-driven Gone inbox |
| `76572320` | chore: sync APP_VERSION to published 3.5.446 |
| `ae2ad530` | feat(safeguards): 5 structural safeguards + throttle/EBADF fixes |
| `d0b3f04e` | docs: CLAUDE.md + memory updates after 2026-04-20 marathon session |
| `9665b720` | feat(covers): hover-triggered upgrade + SW bypass for ?t= reloads + sync ring-buffer hooks + console tracing |
| `c1bc8188` | feat(covers): auto-reload UI when background cover upgrade writes new bytes |
| `fa428da5` | fix(covers): in-place reload after upgrade — no page refresh, no jitter |
| `b757228d` | feat: card-hover cinematic split + nginx upstream pool + 502 page + cache tweaks |
| `8023c20d` | feat: card-hover background (LAN) + /api/dashboard/snapshot (remote) + TMDB prefetch at accept |
| `b0dc1d12` | perf(remote): cache /mthumb/ + /covers/ 7d (was 1h + none), slower disk-scan poll |
| `86b3daae` | chore(version): sync APP_VERSION to published 3.5.439 |
| `3cc7907a` | fix(series/variants): show chosen ✓ for all decisions regardless of reason + unshadow builtin list + comprehensive endpoint tests |
| `e50d2b46` | chore(version): sync APP_VERSION to published 3.5.437 |
| `0fc96a4e` | perf(remote): is_remote gated lazy-vendor + tmdb-img immutable + deferred update-check |
| `24f22ff9` | chore(version): sync APP_VERSION to published 3.5.435 |
| `b23f119e` | fix(remote+routes): cache headers, holiday CSS, integrity Kill All, _OMDB+_tmdb_cache state, pre-update DB backup |
| `19c77265` | fix(settings/db): show all 41 tables (revert filter) + add meta for 8 internals |
| `d7959571` | chore(version): sync APP_VERSION to published 3.5.432 |
| `8d27c2cf` | feat(settings/db): hide SQLite/FTS internals + add 13 missing table meta |
| `e4dd785c` | chore(static): regenerated .gz cache after Wave 8 split |
| `c791e194` | chore(version): sync APP_VERSION to published 3.5.430 (Wave 8) |
| `a02a747a` | refactor: Wave 8 — split 4 remaining route files into sub-packages |
| `c67ed40a` | chore(static): regenerated .gz cache after Wave 3 module split |
| `c46a7d79` | chore(version): sync APP_VERSION to published 3.5.428 (full glob ZIP) |
| `3053e9a3` | fix(publish): glob patterns recursive — Wave 3/9/10/11 sub-packages were missing from ZIP |
| `01e8e883` | chore(version): sync APP_VERSION to published 3.5.426 |
| `0b0e920a` | refactor: decomposition Waves 3+5+6+7+9+10+11 + recovery + db hardening |
| `c71f4ee8` | fix(emergency): publish glob must recurse into templates/partials/** |

### 2026-04-19

| Commit | Subject |
|---|---|
| `cd773b0a` | fix(emergency): make admin import soft — admin/ missing on clients (PPETO crash-loop fix) |
| `77deb849` | refactor(admin): wave 4 — physical admin isolation under admin/routes/ |
| `11b6cf5a` | refactor(templates): wave 2d — settings.html decomposition into 17 partials + 6 general sub-partials |
| `7e9cb7ea` | refactor(templates): wave 2c — extract 14 remaining dashboard overlays + FAB partials |
| `64394f21` | refactor(templates): wave 2b — extract logs / section-tabs / sub-tabs / content partials |
| `62f251f4` | refactor(templates): wave 2a — extract integrity-banner partial (proof of concept for Wave 2) |
| `8a4d3b50` | refactor(html): wave 1.5 — migrate all 5 routes from str.replace() to Flask render_template() |
| `0f6e6837` | refactor(css): wave-1a — extract base.css (root vars + light-theme overrides) |
| `45cc177e` | infra(wave-0): pre-commit LOC ceilings + admin/ isolation skeleton + extraction harness |
| `4d3e0256` | fix(downloader): write filename/file_size/downloaded_at/status='downloaded' on success (Phase R0) |
| `ae0465fe` | feat(db): decision-audit triggers + tests (Phases 2-4 of Immutable User State) |
| `041a4b58` | refactor(sync): kill chosen-swap auto-mutation + legacy undo migration |
| `d5e4bfdb` | chore: bump APP_VERSION to 3.5.411 + regenerated artifacts |
| `35ede12f` | fix: DLC section label wrong for Arabic titles + restore 37 lost user rejects |
| `125cba2d` | chore: bump APP_VERSION to 3.5.409 + regenerated artifacts |
| `57fa7b52` | feat(tunnel): auto-deploy 4-layer hardening on every device (Linux/Mac/Win); skip admin |
| `72cb57e8` | skill: remote-device-ws — canonical WS comms + repair terminal key rotation recipe |
| `94a98691` | docs: session log 2026-04-19 — Phase A/B/D complete; Phase C roadmap |
| `d5af089f` | test: first pytest harness (Phase D wave 1) |
| `63a913a1` | chore: bump APP_VERSION to 3.5.407 + regenerated artifacts |
| `b033df69` | chore: untrack accidentally committed db.sqlite3 |
| `92089d59` | feat: per-item DLC section + bad-stream cooldown + richer logs + missing indexes |
| `f4edc686` | chore: bump APP_VERSION to 3.5.405 + regenerated artifacts |
| `e660aef3` | feat: bulk IPTV fetch + honest cover upgrade + live-category display + user-decision preservation |

### 2026-04-18

| Commit | Subject |
|---|---|
| `e7dcf015` | feat(sync): deep enrichment fix — TMDB details + OMDb retry + visible manual-match |
| `61707ee0` | chore: regenerated gz bundles + v3.5.390 artifacts |
| `6446178e` | chore(vpn): remove orphan JS helpers now that acquire/release are gone |
| `b23f76b7` | refactor(vpn): admin-only watchdog + drop auto-acquire/release |
| `cb5b92eb` | feat(vpn): auto-pause sync/download during VPN + script self-exit guard |
| `33f6eda3` | feat(vpn): state-aware, ref-counted VPN lifecycle for tunnel ports |
| `338b105c` | fix: 0-byte loop + banner + breakdown + flicker + VPN SCP wrap |
| `91c869dc` | feat(logs): per-source retention + writers for Tunnel/Telemetry/Terminal + 10 silent features |
| `33a68284` | feat(auto-update): requirements.txt single source of truth + pip install on update |
| `99b67bd7` | fix(setup-macos): add selenium to pip install list |
| `83ed7a67` | fix(sync): silence PIL bomb warning + graceful selenium-missing + macOS chromedriver |
| `970d583f` | fix(tunnel): UnboundLocalError on health check — module-level os import |
| `1a2b136c` | feat(integrity+cron+trash): scope scanner to visible-truncation, unified cron, trash-only deletes |
| `0db22bb0` | feat(terminal): Arabic rendering + RTL toggle + zero-lag typing (v3.5.379) |
| `0232a3c5` | fix(integrity): Kill All stops drain, Phase A restarts on slow, tri-state ffprobe, exclusivity gate (v3.5.378) |
| `8edb79e4` | fix(repair): remember each device's repair terminal user, stop guessing |
| `31e1550b` | fix(repair): repair terminal session reuse + use external tunnel port |
| `8318c205` | feat(mirror): include sha256 in latest.tag + client verifies + retries 3x |
| `471d2c24` | feat(publish): tv-eg.com mirror fallback for auto-update |
| `84b7edc7` | feat(integrity): detect+repair pipeline + inline banner + boot cleanup (v3.5.373) |

### 2026-04-17

| Commit | Subject |
|---|---|
| `b6a59602` | chore: regenerate compressed static assets + ignore mkcert rootCA |
| `9739a782` | chore: bump local APP_VERSION to 3.5.371 to match published tag |
| `daa4ce9c` | fix(telemetry): accurate Mac RAM usage in Connected Devices |
| `f08fc33b` | fix(telemetry): cap heartbeat backoff at 5min instead of 24h |
| `3779ca46` | feat(repair terminal-terminal): pro overhaul — adaptive polling, WebGL, 24 presets, 5 themes |
| `53654374` | chore: bump local APP_VERSION to 3.5.369 to match published tag |
| `b72d5e86` | security: defense-in-depth after public-repo session value leak + update-button fix (v3.5.368) |
| `7b3816eb` | chore: bump local APP_VERSION to 3.5.365 to match published tag |
| `f0a87029` | feat(search+pwa+ssl): unified pipeline, Arabic search, iOS PWA fixes (v3.5.364) |
| `2527e7a3` | fix(card): unified card click — opens detail modal from any zone |
| `342bdf1e` | feat(search): Stage 4 — trending, continue-watching, actor known-for |
| `eeb5248a` | feat(search): Stage 3 — split-pane preview rail (desktop ≥1280px) |
| `79ca892f` | feat(search): Stage 2 — rich recents + ⌘K shortcuts + per-item dismiss |
| `6f5d4201` | fix(security): /api/remote-login — same hardening as /api/remote/auth |
| `cf69645e` | fix(security): remote login — hash/constant-time/rate-limit/cookies (7 fixes) |
| `99e7b05f` | feat(search): section escape on search + desktop dropdown redesign |
| `9148e429` | fix(mobile): prevent iOS zoom + larger touch targets in search dropdown |

### 2026-04-16

| Commit | Subject |
|---|---|
| `c4b74b12` | chore: bump APP_VERSION → 3.5.348 (rich search + IPTV cache + UI polish) |
| `51a28f5f` | feat(search): rich FTS5 + IPTV cache + professional dropdown UI |
| `a91f7292` | chore: bump APP_VERSION → 3.5.347 (batch writes + batch IMDb lookup) |
| `857c4e3b` | fix(perf): Phase 6 B028/B107 batch writes + B066 batch IMDb lookup + B052 log |
| `006cd448` | chore: bump APP_VERSION → 3.5.346 (DRY + Stage 5b parallelization) |
| `240e9c1d` | fix(dry+perf+polish): Phase 7-8 + B021/B022 parallelize Stage 5b |
| `4a661880` | chore: bump APP_VERSION → 3.5.345 (Phase 4-7 audit fixes) |
| `2f1c1fbd` | fix(perf+dry): Phase 6 throttle + Phase 7 dedupe (B035/B070-B071/B114) |
| `5a47cf68` | fix(filter): Phase 5 substring false positives (B031/B032/B055/B108) |
| `03e50cb7` | fix(pool): Phase 4 B010 — conn.close() → release_connection() |
| `e799fa6d` | chore: bump APP_VERSION → 3.5.344 (audit fixes release) |
| `71d84c5c` | fix(audit): Phase 1.5 regression + Phase 2 integrity |
| `3ef64c76` | fix(security): Phase 1.5 — close critical auth holes found during Phase 1 verification |
| `41f89c67` | fix(sync): B023 POSIX fallback — use pgrep tree, never killpg |
| `5119b546` | docs(audit): Phase 2 audit findings — 118 new bugs (B115-B232) |
| `87928e9f` | docs(audit): Phase 1 audit findings + fix plan |
| `d28e518f` | fix(security): Phase 1 — web/auth + auto-update hardening (B001,B111,B097,B098,B103) |
| `0d587a5d` | fix(security): Phase 1 — downloader aria2c PID isolation (B086) |
| `a78af02c` | fix(security): Phase 1 — sync group hardening (B053, B023) |
| `dd8534cc` | fix: Remote Access auto-fetch tunnel info from server for client devices (v3.5.343) |
| `6a44485b` | feat: auto-maintenance, HD covers, trailer reliability, performance caching (v3.5.342) |
| `68602b73` | feat: auto-download on paste — URL pasted in micky input triggers download |
| `576786a4` | fix: remove hardcoded /media paths + fix _log undefined in tunnel |
| `a2bc11f6` | chore: session 2026-04-16 — tunnel system, PTY fix, restart automation, search fallback |
| `2bebb51d` | fix: currentSearch → searchQuery, grid 4-col desktop + gap 40px |
| `9ccc8cbc` | feat: clear search on section switch + IPTV API fallback when no local results |
| `f74e2e18` | fix: disk discovery re-appearing items — substring matching for tracked names |
| `37ef1401` | feat: remote card sizing — cap to mthumb 300x450, responsive grid |
| `deca3ea4` | fix: health check includes RDP/VNC ports in status |
| `64baaf75` | feat: 4-port tunnel blocks (HTTPS/repair terminal/RDP/VNC) + full port status UI |
| `9860b07c` | fix: repair terminal repair try multiple usernames (root/mac-user/ppeto) |
| `565799ee` | feat: auto-provision repair terminal tunnel — zero manual setup |
| `9256668f` | chore: bump version to v3.5.336 — PTY Ubuntu fix |
| `8b938c4f` | fix: PTY terminal permission denied on Ubuntu — 3-layer fallback |

### 2026-04-15

| Commit | Subject |
|---|---|
| `8ae2b07a` | chore: bump version to v3.5.335 — repair terminal repair system |
| `789e27d9` | feat: Fix button + repair terminal terminal UI + device alert banner |
| `520ba072` | feat: repair terminal repair key setup + repair terminald in all platform scripts |
| `aa06b44b` | feat: auto-fetch admin repair terminal pubkey + paramiko during auto-update |
| `3e711371` | feat: repair terminal repair module — terminal bridge, quick commands, health check |
| `cfba2e61` | feat: dual-port tunnel registry + repair terminal fallback for cmd_send |
| `cb9b0d5e` | feat: forward port 22 (repair terminal) + 3389 (RDP) alongside 443 in tunnel |
| `ff4a4a99` | feat: PHP endpoints for admin repair terminal key registration and distribution |
| `fd92bb5b` | docs: repair terminal tunnel repair system implementation plan — 9 tasks |
| `3d1dc9f8` | docs: fix spec per advisor review — key bootstrap, HTTP polling, repair.py |
| `8e7d10e7` | docs: repair terminal port 22 tunnel + device repair system design spec |
| `dd48dc52` | chore: update check interval 5min → 2min |
| `56fe7121` | fix: stop re-enrichment loop for items where OMDb has no data |
| `47ebd1a7` | feat: auto-install yt-dlp on update + matcher regression fix |
| `06f53138` | fix: matcher auto-search regression + gz updates + version sync v3.5.330 |
| `c531e596` | chore: bump version to v3.5.329 |
| `46ad040a` | feat: sync enrichment fix, trailer cookie auth + yt-dlp fallback, TMDB image reliability |
| `8d720662` | fix: use mthumb (300x450) on remote to match 4-col card size exactly |
| `be8da886` | chore: bump version to v3.5.326 |
| `ea91bf50` | feat: Mac native, HTTP/2 tunnel, cover quality upgrade, 3-col grid |
| `0fba95cf` | chore: bump version to v3.5.324 |
| `67116b67` | feat: auto-configure nginx HTTP/2 on Ubuntu native — zero manual steps |
| `11aa2e55` | chore: bump version to v3.5.322 |
| `009d068f` | feat: nginx HTTP/2 frontend — faster image loading over tunnel |
| `528781c0` | perf: medium thumbnails + remote-only PAGE_SIZE for tunnel speed |
| `816f13e8` | fix: show real CPU load in Connected Devices device cards |
| `5f5b3aee` | feat: Disk Discovery batched scan — 3 items at a time with live progress |
| `1ebbc5ba` | fix: trailer fail marker (no spam retries), prevent duplicate calls |
| `6924a8b0` | feat: add Tunnel, Social, Telemetry, Terminal tabs to System Logs + Connected Devices |
| `60b2a3b1` | fix: telemetry ping every 60s (was 1h), add cpu_load to device data |
| `90677370` | fix: Remote tab tunnel URL lookup from correct config_store key (tunnel_ports not telemetry_devices) |
| `82d34692` | feat: Remote tab tunnel URL from device registry, JPG/WebP counts, 60s device refresh |
| `fab0e1b3` | feat: Remote Access IPs, episode local/online badges, Cover Management in Maintenance |
| `16e765b4` | fix: PTY terminal uses pty.fork(), search bar compact+expand on focus |
| `6e476d97` | feat: xterm.js interactive terminal — real PTY shell on any device |
| `5e3e01c8` | fix: terminal commands sent directly to backend — no more hardcoded builtins list |
| `00de45e4` | feat: show file path as visible text under VOD player title bar |
| `1eaad619` | feat: expanded remote terminal — 14 new commands for full device management |

### 2026-04-14

| Commit | Subject |
|---|---|
| `a23aacb7` | fix: sync backfills category names in DB — no more numeric-only Source labels |
| `f3b1e5af` | fix: Disk Discovery must NOT override start_episode — user-only choice from Dashboard |
| `310a1e4a` | fix: prevent duplicate series downloads on path change, VOD file info, DB browser 401 handling |
| `67718897` | feat: Service Worker caching for remote access speed |
| `3ae97373` | fix: trailer fail marker (no spam retries), prevent duplicate calls |
| `7938db40` | fix: IMDb rating priority, update both rating columns, trailer logging |
| `6a3ca352` | fix: sync image download before response — no more broken images |
| `ba713d5f` | fix: always-update IMDb data, card click→flex, tmdb-img 204 fallback |
| `401eaf9e` | feat: IMDb GraphQL enrichment, local trailer cache, gallery click→poster |
| `9e71e381` | fix: IMDb trailer scraper — GraphQL + videoembed bypass WAF |
| `2e965c5e` | feat: auto-tunnel provisioning system — allocate, setup, start, auto-restart |
| `70fbbd05` | refactor: replace all legacy endpoint references with tv-eg.com |
| `6d983b1c` | fix: WebP q95, static TMDB images, cast names, social blur, render debounce |
| `b53bc858` | feat: actors DB, TMDB cast enrichment, local image proxy, eliminate theme duplicates |
| `58b3fe97` | feat: per-client access field + URL in Settings Remote Access section |
| `8759218f` | chore: sync APP_VERSION to 3.5.292 |
| `429adc42` | feat: settings remote access section + WebP button + login device name |
| `58963e58` | fix: social covers download via sync's download_cover (HTTP, not HTTPS) |
| `d0e42b49` | feat: WebP covers + fix social feed hang + cache headers |
| `cca08e1c` | fix: session persistence (stable private marker_key) + double /covers/ path bug |
| `0294197f` | fix: remove command whitelist — any command runs as shell fallback |
| `c2d9fa92` | feat: per-device access field change from Connected Devices + Mac-me tunnel link |
| `93e46a5a` | feat: remote access gate, local cover download, tunnel links, low-quality remote covers |
| `5202a5d5` | fix: strip :80 port from HTTPS-converted cover URLs |
| `d52a3372` | fix: social feed covers blocked by mixed content — force HTTP→HTTPS |
| `939bae00` | fix: social feed IPTV access field lookup — support nested settings.iptv.domain |
| `e6256149` | fix: terminal cmd split — "sh ls -la" now correctly splits into cmd=sh args=[ls,-la] |
| `29ccf909` | feat: real terminal via WS — unrestricted shell, no PHP polling |
| `48418f0d` | fix: holiday theme timezone bug — toISOString() returns UTC, not local |
| `f9f0e70a` | fix: holiday theme stuck after midnight — 3-layer cleanup |
| `7089daa1` | fix: holiday theme auto-revert after midnight + cross-platform pip install |
| `2a0fbe70` | fix: cross-platform websockets auto-install (Ubuntu PEP 668 compat) |

### 2026-04-13

| Commit | Subject |
|---|---|
| `7e7f25ce` | fix: WebSocket stability — remove manual ping, fix auto-install return bug, add provision endpoint |
| `23e33505` | feat: auto-install websockets library if missing |
| `fcfd8832` | feat: WebSocket client — live connection to relay server |
| `bc543fef` | feat: WebSocket relay server + device card button layout fix |
| `d1299aa3` | fix: hide Update button on admin device (Docker doesn't auto-update) |
| `5b7201b5` | feat: sync device aliases to PHP server for cross-device Social Watch names |
| `29c440b1` | fix: add server PHP files to repo + panel.php ghost device filter |
| `64c9fd3e` | fix: IPTV API response parsing — merge info + movie_data for VOD |
| `bece315c` | feat: Remote Command Relay UI in Connected Devices |
| `9e829a24` | fix: social cover resolution — local path prefix + full URL fallback |
| `8563bcb3` | security: remove IPTV_ADMIN env var fallback, filter ghost devices |
| `a53c87aa` | security: admin session value auth replaces IPTV_ADMIN env var, social cover fix, publish images |
| `32f36768` | feat: remote provisioning — admin drops config on PHP, device picks it up |
| `e321b36a` | feat: show 🔗 Relay badge on Connected Devices if cmd_private marker configured |
| `e74a0dbc` | fix: reports were dead code after return — now all 11 sources actually sent |
| `7eb94eae` | fix: restore Logs button to header — non-admin devices need log access |
| `3038b372` | feat: Remote Command Relay — secure admin-to-device execution via PHP |
| `66e78917` | feat: telemetry sends all 11 log sources (was sync+download only) |
| `467815bb` | fix: actor profile shows director filmography + flex stays open on actor click |
| `a724e190` | feat: Social Watch polish — IPTV category name, no blur, no opacity, rename |
| `9945d26c` | feat: Social Watch hero cards — 486px/43vh poster, arrow flip, local covers, section name |
| `3337386f` | fix: Social Watch uses cover_local first (never external URLs) |
| `45a6718c` | fix: social sender tolerates non-numeric iptv_ids (discovered items) |
| `39dbc639` | fix: social_loop logs errors instead of silent pass — critical for remote debugging |
| `4b927ccb` | fix: include social_report in telemetry payload (was collected but not sent) |
| `34f9e8dc` | diag: include social logs in telemetry reports for remote debugging |
| `1fbe4103` | diag: add social report diagnostic logging for remote device debugging |
| `d577b9ed` | fix: Social Watch sender uses iptv_id (not media_id) — cross-device consistent |
| `57401f9a` | fix: Social Watch PHP backward compat — handle old format objects + skip invalid ids |
| `14f532f4` | feat: Reports → Connected Devices — local device shows 16 log tabs |
| `23dc1b1e` | feat: Social Watch v2 — slim protocol (iptv_ids only, local resolution) |
| `b3495b59` | chore: session save — Social Watch architecture + Reports plan + cover fix |
| `940bc4ca` | fix: matcher year display, social cover fallback (omdb→cover_url→local) |
| `c1862549` | feat: Social Watch device aliases, library badges, matcher year, log cleanup |
| `a4cc7166` | fix: auto-prune logs >10 days, stale lock cleanup, tab renames, LEFT JOIN social |
| `c87d98f0` | fix: social report works without imdb_id, stale lock cleanup, Rich rename |
| `f3f54295` | chore: sync APP_VERSION to 3.5.224 |
| `c404eb91` | fix: Social Watch cards navigate to section, remove monthly, responsive FABs |
| `3573d2cc` | chore: sync APP_VERSION to 3.5.223 |
| `6b0aee6a` | fix: Social Watch 7-bug overhaul + pipeline guard hook |
| `21104746` | fix: social report diagnostic logging — logs accepted count when 0 items found |
| `76930f83` | fix: social report LEFT JOIN sections — fixes devices with NULL section_id |
| `24f4d9d9` | fix: download card clears when download is not active (was stuck on last download) |
| `0366c6db` | fix: remove body::before background from sham-nessim + social report error logging |
| `a13d8c87` | fix: sham-nessim banner — 207px width, no background, no blur, full opacity |
| `354c0d6d` | fix: sham-nessim banner — show images at full natural height |
| `943cfc64` | fix: remove center text from sham-nessim banner — photos only |
| `4a8bdbed` | feat: Sham el-Nessim banner — left/right feseekh photos + centered Arabic/English text |
| `84cb3fa7` | feat: Sham el-Nessim feseekh banner — real IMG elements with crossfade, desktop only, 1200px centered |
| `73bc36c1` | fix: sham-nessim feseekh banner crossfade + delete test social data |
| `bd74d074` | fix: Social Watch — hide own data, sham-nessim feseekh banner, clean empty state |
| `df5c80ba` | fix: Social Watch — remove (you) tag, hide Monthly Stats, clean test data |
| `90d75240` | feat: Social Watch device-grouped UI with featured poster + horizontal slider |
| `55e46ff6` | feat: Social Watch device grouping, episode dates, no-poster, social fix |
| `ceddfe95` | feat: S-Watchlist — series tracker panel with watch progress |

### 2026-04-12

| Commit | Subject |
|---|---|
| `637ead32` | chore: sync local version to 3.5.205 + dashboard CSS slider fix |
| `5c5a2f02` | fix: publish version double-increment + category_id 100% backfill |
| `e7289886` | fix: publish auto-restart — server now restarts after publish to apply new version |
| `dde7642e` | feat: complete holiday theme overhaul — 28 themes with SVG art, photos, birthday events |
| `1ca4d9e7` | feat: auto-restart sync/download after Live TV stops + startup trigger |
| `196b54eb` | feat: Social Watch — persistent badge checkpoint + wiggle animation |
| `48623034` | feat: Social Watch — 10min sync, clickable items, themed JS field fixes |
| `91b8092c` | feat: smart Update button + folder picker root-jumping + Social Watch text |
| `8c66b266` | fix: Social Watch PHP backend + correct endpoint URLs for LiteSpeed |
| `cf3c5c3a` | fix: Social Watch — 11 bugs fixed + enabled by default + Ubuntu browse-dirs |
| `3af0d462` | fix: Ubuntu native — rootCA path + browser cert auto-trust |

### 2026-04-11

| Commit | Subject |
|---|---|
| `b332bdb9` | fix: glob root_dir requires Python 3.10+ — use absolute paths for 3.8 compat |
| `59400266` | fix: enable auto-update on Mac/native — cert presence is not admin indicator |
| `282cc3c3` | fix: pin urllib3<2 on macOS with LibreSSL to suppress SSL warnings |
| `3dc9c298` | fix: setup-macos.sh — lower Python min to 3.8, fix venv path in plist |
| `0a834166` | fix: add future annotations for Python 3.9 compat on macOS native |
| `e23d19ea` | fix: skip DB migration v3 on fresh installs — tables don't exist yet |
| `c30c9df0` | docs: update Obsidian integration — new folders, hooks, obsidian-session skill |
| `0ad1ad77` | fix: restore Second Account section in root settings.html |
| `928d6c74` | fix: bandwidth panel uses local date instead of UTC — prevents off-by-one at midnight |
| `219cf075` | feat: holiday themes — 2 new saints + 6 enhanced themes, all professional & distinctive |
| `b651e873` | fix: holiday themes — Holy Saturday joyful redesign + Easter stronger cross |
| `85269c1c` | feat: Connected Devices — delete, alias, disconnected section + auto-cleanup |
| `305f94cf` | fix: Social Watch FAB desktop-only — hidden on mobile (≤640px) |

### 2026-04-10

| Commit | Subject |
|---|---|
| `98a61451` | fix: final 6-bug graduation cleanup |
| `ca4b3e76` | fix: excluded_new 5-bug fix — complete end-to-end repair |
| `5257b713` | fix: excluded_new count query now matches paginated query conditions |
| `f14fb5d2` | fix: _safe() guard eliminates all undefined/null in UI + cast photos in Flex Detail |
| `bb69b93b` | fix: excluded_rich/excluded_new tabs disappeared in paginated mode |
| `e5dc0ed7` | fix: social watch exclude self + sync auto-enrich missing fields |
| `d3efd620` | feat: Flex Detail overlay shows director, cast, plot, RT, runtime, rated, awards |
| `8f4eac09` | feat: Social Watch + search tabs + undefined fixes |
| `e6745527` | feat: card enrichment (RT/runtime/rated/awards/plot/director), actor search+profile, holiday fixes |
| `35e69dad` | perf: 12-issue performance audit — connection pool, N+1, thumbnails, disk check |
| `931d709b` | fix: 9-agent review — PEP 668 venv for macOS, tzdata for Docker, Alpine iproute2, if/then bug |
| `3a9290ca` | chore: sync version to v3.5.163 |
| `1536b001` | feat: cross-platform native installers — macOS, Ubuntu, Linux + 12 critical fixes |
| `667c2d27` | fix: prevent update loop on Windows — version-based comparison for LAN strategy |
| `cbf332ed` | fix: stale holiday cache no longer blocks theme activation |
| `53550b66` | feat: auto-pin version after publish — no manual pin step needed |
| `45e86e54` | chore: sync version to v3.5.160 |
| `8f8c998d` | fix: sync hash computation across all 3 auto-update entry points |
| `23eec089` | fix: Windows clients now receive theme files via auto-update |

### 2026-04-09

| Commit | Subject |
|---|---|
| `87ad948f` | chore: sync version to v3.5.156 (fix publish auto-increment drift) |
| `c84cd2ea` | chore: sync version to v3.5.155 |
| `ad2bfc07` | feat: multi-strategy Windows auto-update with 4 fallback methods |
| `a96e67a8` | chore: sync version to v3.5.153 |
| `c2d0cffc` | feat: FTS5 autocomplete search — instant suggestions, keyboard nav, recent searches |

### 2026-04-08

| Commit | Subject |
|---|---|
| `f34f8339` | fix: theme preview now shows full holiday experience (panels + decorations) |
| `4af77aac` | feat: holiday side panels with real photos + theme preview fix |
| `61b9c45e` | feat: holiday side panels — emoji + name on left/right sides (desktop) |
| `2387c057` | feat: 12 new Coptic Christian holiday themes — total 24 holidays |
| `f996e007` | polish: complete shadow + glass + watch button overrides for all 14 themes |
| `92836b93` | fix: Windows auto-update + polish all holiday theme CSS variables |
| `863968ad` | feat: unique dedicated decorations for all 12 holiday themes |
| `92d6c109` | feat: telemetry delta logs, full timestamps, version update history |

### 2026-04-07

| Commit | Subject |
|---|---|
| `98502252` | feat: green notify dot for Excluded-but-New sections, waterfall tab auto-switch |
| `0822767d` | feat: global download queue, unlimited aria2c retries, cross-section parallelism |
| `2314b38a` | feat: parallel file downloads, DL-NOW persistence, 3-min section delay fix |
| `957df176` | feat: dual-account download, log auto-refresh, exponential backoff, access field safety |

### 2026-04-06

| Commit | Subject |
|---|---|
| `7601015b` | fix: remove dark progress overlay from sync card slides — images now vivid |
| `655bc0b0` | feat: sync card Swiper slides match download card poster style |
| `2019c3a1` | feat: show status messages inside download card (.dlc-msg) |
| `2dec1c4c` | fix: remove download status line entirely — visual card only |
| `4d7aa6f1` | fix: download card — restore visual card, status line only when active |
| `eedb9742` | feat: comprehensive sync/download log rendering — full data on every step |
| `eb57e97a` | feat: IMDb ID search, global search navigation fix, progress bar % on bar, group audit fixes |
| `cb5d0f39` | fix: dl-sec always visible via DB query + mobile CSS tweaks |
| `7bdfe79d` | chore: bump version to 3.5.149 |
| `7683138f` | feat: download dashboard card — poster, section, episode, progress bar + sync swiper autoplay fix |

### 2026-04-05

| Commit | Subject |
|---|---|
| `f676c17f` | feat: sync visual dashboard — donut chart, Swiper poster slider, category names, project map |
| `abe9d287` | feat: calendar downloads, telemetry reports, adaptive logs, disconnected badge, push chat bubble |

### 2026-04-04

| Commit | Subject |
|---|---|
| `d9fbb0c1` | feat: telemetry history tracking, CPU detection, panel redesign |
| `945d962a` | feat: integrity resume — download incomplete files with live progress |
| `25a81669` | fix: instant kill — eliminate 2-7s UI delay after Kill All / Stop Download |
| `a948f36d` | feat: configurable speed threshold slider for smart restart |
| `fc1d9ebb` | feat: Windows auto-update fix, telemetry panel redesign, download improvements |
| `35f9d64f` | fix: mobile UI polish — log header gradient, badge sizes, text cleanup |
| `79543792` | feat: telemetry v2 — CPU model, full operational logs, badge auto-refresh |
| `51801d3e` | feat: device telemetry system — anonymous diagnostics, admin panel, PHP backend |
| `dd95fc3c` | feat: mobile calendar redesign — compact grid + inline agenda, light theme logo filter |
| `5ca8c183` | feat: IMDb Matcher overhaul — batch re-enrich, cleanup words, DB schema v3, search fixes |
| `418f7118` | chore: sync version 3.5.125 |
| `b4b6b8fe` | fix: mobile CSS cleanup — remove .app padding, scrollbar width, log overflow hidden, modal overflow-x, fulllog fade hints |
| `695d3b80` | chore: sync version 3.5.124 |
| `12d0b0f2` | fix: responsive breakpoints standardized, mobile layout fixes, versions modal chosen logic (v3.5.123) |

### 2026-04-03

| Commit | Subject |
|---|---|
| `5c0da88c` | chore: sync version 3.5.122, update deploy sequence (stop+start not kill 1) |
| `138ebc9c` | fix: remove theme toggle button from header (theme via Settings only) |
| `b21ea34d` | fix: restore theme toggle button in header (was removed by mistake) |
| `ba731fe3` | fix: imdb_id UNIQUE crash + Windows 1-min auto-update + remove theme button |
| `00659bfc` | feat: SSL cert includes LAN IPs + /install-ca serves .crt for Windows/Mac |
| `fab8bfa0` | fix: Disk Discovery complete rewrite — 23 bugs fixed from audit |
| `fb17a7c0` | fix: Disk Discovery — movie folder path, auto-refresh, auto-search OMDb |
| `3a69112e` | fix: link-external — status accepted (not downloaded), OMDb enrichment |
| `eff656aa` | fix: link-external — wrong column names, missing fields, broken movie_mapping |
| `ae26f6f4` | fix: link-external column name — added_date → added_at |
| `639abdb1` | fix: Disk Discovery — remove OMDb from scan, add Link button for external results |
| `d2cd035e` | fix: Disk Discovery — 8 bugs fixed, lightweight count endpoint |
| `940c550a` | fix: Flex Muscles still disabled on Windows 10 — use any-hover media query |
| `5ccf1290` | fix: Disk Discovery OMDb search dead — API key read from wrong level |
| `040450ef` | fix: Flex Muscles disabled on Windows 10 PCs — false touch detection |
| `97c5199d` | fix: Windows trash path — use section/.trash instead of drive root |
| `f8b5a073` | fix: scheduled tasks 261-char limit — use wrapper .bat files |
| `5721ae2a` | fix: batch ) escaping — unescaped parentheses inside if/for blocks crashed CMD |
| `bf3fb5e4` | fix: UAC elevation path escaping — trailing \ broke PowerShell \" |
| `229436aa` | fix: setup-windows.bat — 34 bugs fixed (UAC crash, MS Store Python, PATH destruction) |
| `04dccb68` | feat: golden accent styling for dark/light mode + Process Control in Maintenance |
| `f3b44ea9` | fix: universal safe-area padding for all overlays (iPhone Dynamic Island) |
| `d3b3d2ae` | feat: الأسطورة — social media video download + gallery system |
| `1938e119` | feat: 3D inset depth effect on section-info-bar, tabs-row, sub-tabs-row |
| `25903a79` | fix: Kill All ETag cache bug — button stayed visible after kill |
| `7c3f16bf` | fix: Kill All instant response, clear feedback, UI reset |
| `59d1ddb0` | feat: highest quality posters everywhere, IMDb badge inline, calendar tabs |

### 2026-04-02

| Commit | Subject |
|---|---|
| `bbdd2851` | chore: sync APP_VERSION to 3.5.87 after publish |
| `860da7cc` | feat: iOS player fix, ffmpeg cleanup, poster upgrade to disk, cover cache revalidation |
| `446a5aa5` | chore: sync APP_VERSION to 3.5.86 after publish |
| `195f4da8` | feat: Flex Muscles — trailer preload, gallery flip, poster upgrade |
| `5924e6bc` | chore: sync APP_VERSION to 3.5.85 after publish |
| `8af7c91a` | feat: Flex Muscles — loading spinner, TMDB image gallery, better trailer UX |
| `e44e196f` | chore: sync APP_VERSION to 3.5.84 after publish |
| `e521ba5e` | fix: Flex Muscles — 80vh poster, Ken Burns animation, working IMDb trailers |
| `6c941848` | chore: sync APP_VERSION to 3.5.83 after publish |
| `a2f90e31` | feat: direct IMDb trailer playback — MP4 from imdb-video.media-imdb.com |
| `e0dfada6` | chore: sync APP_VERSION to 3.5.82 after publish |
| `52e2377c` | fix: download limits not enforced — load_settings_as_dict merged both sources |
| `aeed2dd3` | chore: sync APP_VERSION to 3.5.81 after publish |
| `8f7e6579` | feat: Flex Muscles — desktop hover 4s → shake → fullscreen detail + trailer |
| `ddef8846` | chore: sync APP_VERSION to 3.5.80 after publish |
| `fbc1352e` | fix: Matcher cross-section merge (Rule 4), conn pool, SERIES_STALE_DAYS type |
| `3b3be4c3` | feat: smart kill notification + per-file download limits |
| `6d45032a` | chore: sync APP_VERSION to 3.5.79 after publish |
| `9f041d51` | fix: per-file download limit enforcement + auto-switch to accepted tab + status dot |
| `6c29043b` | feat: Settings overhaul — collapsible sections, download limits, stale DB, themes preview |
| `4696040c` | chore: sync APP_VERSION to 3.5.78 after publish |
| `a399d24f` | feat: System Logs views, Disk Discovery, 12-bug data integrity audit |

### 2026-04-01

| Commit | Subject |
|---|---|
| `3f7c216b` | chore: sync APP_VERSION to 3.5.70 after publish |
| `1e1a14e8` | feat: Dismiss button on Continue Watching cards + delete progress API |
| `13a0bc75` | feat: Activity Calendar v2 — glassmorphism, animations, detail popup |
| `c2dffaed` | feat: Activity Calendar — daily view of all watch, accept, reject, live activity |
| `3417c6cb` | feat: Watch History tab in System Logs — shows all VOD playback activity |
| `17774e31` | fix: Trash tab empty when opened via direct URL hash (#1/trash) |
| `f67eb662` | chore: sync APP_VERSION to 3.5.69 after publish |
| `19c7bc8a` | fix: iOS resume via HLS START tag + aggressive repaint after player close |
| `7c7839f6` | fix: iOS seeking — on-demand HLS segment generation for instant seek |
| `1428a1f5` | fix: iOS — probe duration priority, white cards repaint, safe area padding |
| `6382b2c6` | fix: iOS duration — probe duration takes priority over video.duration |
| `4654fed9` | fix: iOS resume — set video.src before onloadedmetadata, store HLS duration |
| `69556a51` | fix: iOS VOD — pre-generated VOD playlist with full duration from ffprobe |
| `17abcf47` | fix: iOS VOD — HLS remux instead of fMP4 (full duration + seeking on Safari) |
| `877199f3` | fix: iOS fMP4 duration — probe real duration via ffprobe, fallback for Infinity |
| `affb8569` | fix: iOS VOD playback — use canPlayType detection + fMP4 remux fallback |
| `106477b6` | fix: Safari/iOS VOD — request .mp4 instead of .mkv, remove fMP4 remux |
| `b12aaee1` | fix: VOD playback on Safari/iOS — auto-remux MKV to fMP4 |
| `99a536d9` | chore: sync APP_VERSION to 3.5.68 after publish |
| `6efee62f` | feat: Continue Watching button shows count badge and hides when empty |
| `41596d94` | fix: Hide completed series (90%+) from Continue Watching |
| `7b58f2ee` | feat: Continue Watching — resume movies and series from where you left off |
| `37e920e1` | chore: sync APP_VERSION to 3.5.67 after publish |
| `65fc8cf5` | fix: Stop spamming 'PROCESSES KILLED' log when no processes are running |
| `2ad1a573` | fix: 7 audit fixes — rate limiter bypass, URL encoding, subprocess safety, O(1) rebuild |
| `edaf60a9` | fix: Complete player.js rewrite — all race conditions and save bugs fixed |
| `08b1247f` | fix: Series resume picks most recent episode, not highest position |
| `ce3447b0` | fix: Critical race condition — episode/media IDs set after await, not before |
| `85218c91` | fix: Episode active highlight with proper CSS across all themes |
| `f153a465` | fix: Critical watch progress DB bug — NULL episode_id caused infinite duplicates |
| `6ad8b65d` | feat: Episode watch indicators + resume fix for corrupted progress data |
| `27c8cfd0` | feat: Live TV instant load + last channel memory + VOD resume fix + cache busting |

### 2026-03-31

| Commit | Subject |
|---|---|
| `c118a215` | feat: Year filter + Live TV fullscreen resilience + mobile header fix |
| `6879d02c` | fix: remove Live TV mini log bar — logs only in Full System Logs popup |
| `6a08deaa` | feat: Live TV loading indicator + error tracking |
| `9ccd0446` | perf: Live channels cache invalidated on sync + excluded sort bottom |
| `156083ff` | fix: Live TV is standalone section tab in Filter Breakdown, not sub-tab |
| `08e972ae` | feat: Live TV Filter Breakdown + category exclusion system |
| `c1c0886d` | feat: Live TV stats chart + cleanup + mobile button |
| `d29f0310` | fix: Live TV heartbeat reliability + device logging |
| `e9cf4b1e` | feat: Live tab in Full Logs + scroll fix + sync NOT NULL fix |
| `cadaf337` | feat: Live TV logs in System Logs + sync NOT NULL fix + scroll fix |
| `5eec03a1` | feat: LIVE button v2 — solid red badge with ripple broadcast animation |
| `d0df98cb` | feat: LIVE button — premium animated design with gradient text and glow pulse |
| `94208153` | fix: Live TV — second browser can no longer kill first session |
| `14b04c02` | fix: Live TV session lock + iOS PiP + stale lock cleanup |
| `7d2d403d` | fix: Live TV iPhone zoom — disable user-scalable while overlay open |
| `385f994f` | fix: Live TV iPhone — video fit, fullscreen, session timeout |
| `3754ded6` | fix: Live TV iPhone — safe-area-inset-top for Dynamic Island + hide sidebar scroll when playing |
| `5b0a3ba4` | fix: Live TV mobile — no scroll, video centered, 100dvh |
| `b63315cc` | feat: Live TV mobile UX — fullscreen player with back button |
| `44e95372` | fix: Live TV — reject second browser + restore iOS HLS support |
| `b83e91cc` | fix: Live TV buffer 8s ahead — liveBufferLatencyMinRemain=8 |
| `748e1f56` | fix: Live TV channel switch — destroy old player fully before new one |
| `a88c9099` | fix: Live TV startup stall — wait for canplay before play() |
| `d5436594` | feat: Live TV — browse and stream IPTV channels in browser |
| `8ff30866` | perf: remaining audit fixes — filters, trash, cover repair |
| `4948aa8b` | feat: IMDb watchlist reason overrides other exclusion reasons |
| `734b38a7` | fix: Trash dynamic update + codebase audit fixes (7 issues) |
| `cd349815` | fix: Settings page theme matches Dashboard — unified backgrounds |
| `120d67e5` | fix: Excluded-but-New tracks rejected IMDb-watched items correctly |
| `79ed4f7e` | perf: audit Excluded-but-New feature — cache + remove redundant loads |
| `44dd6927` | fix: Download Log hidden on mobile — logs container too short |
| `ec19eefe` | fix: downloader lock file path — dashboard now detects active downloads |
| `f6ce5049` | perf: engineering judgment fixes batch 6 — sync-critical issues |

### 2026-03-30

| Commit | Subject |
|---|---|
| `a70125f1` | perf: engineering judgment fixes batch 5 — final safe fixes |
| `4e0774cf` | fix: restore SELECT 1 connection validation — Issue 30 broke DB connections |
| `4fb974ed` | perf: engineering judgment fixes batch 4 — 7 more issues |
| `cda70ddf` | perf: engineering judgment fixes batch 3 — 8 more issues resolved |
| `f86d25de` | fix: Add Section UX + engineering judgment fixes batch 2 |
| `084dfaf7` | perf: engineering judgment audit — fix 7 critical/high issues |
| `fb636d59` | fix: Windows 10 compatibility — direct download fallbacks, no winget dependency |
| `9cd7e8ff` | fix: Windows native uses port 443 + iptv.local hosts entry |
| `68368187` | feat: native Windows 10/11 installer — no Docker required |
| `faca5b17` | chore: add agents config, database, and skills lock |
| `683ca84c` | fix: auto-discover publish files + log styling + obsidian sync dedup |
| `80cdb29e` | chore: bump version to 3.5.28 |
| `95b3acc9` | feat: holiday theme visuals — 12 Egyptian holidays with foreground decorations, particles, and animations |
| `156671e0` | feat: responsive fixes + Egyptian holiday theme system (12 themes, colors only — visuals pending) |

### 2026-03-29

| Commit | Subject |
|---|---|
| `053b61a2` | docs: SKILL.md v3.5.31 — 6 new traps (trash restore flow, toast, variant loss, timestamps) |
| `26876896` | fix: trash restore — 5 bugs (toast undefined, variant lost, vague errors, double-click, wrong timestamp) |
| `059c76a1` | feat: Obsidian hooks rewritten — direct filesystem sync, no MCP dependency |
| `7595ab5d` | docs: SKILL.md v3.5.30 + 5 new traps, session-log hook captures git state |
| `599cf0d7` | fix: integrity review, watched_del guard, stale tracker cleanup, lock safety |
