# Changelog - Malachite Beast Unlocker + GPU Governor

## v1.7.0 (versionCode 170)

### New
- Bundled Mediatek Mali GPU Governor v2.12.5 (Seyud, Tools-cx-app, GPL-3.0) in a single zip.
- GPU mode is now tied to each profile: Battery = powersave, Balanced = balance, Gaming / Esport 90 = performance, Esport 120 = fast (editable via `gpu_*` lines in `beast/profiles.conf`).
- Per-app profiles also set that app's GPU mode in the governor's `games.toml`.
- Tuned governor config (`beast/gov_tuned.toml`) applied on first install: lower margins, faster ramp-up, short hold on ramp-down. Old config is kept as `config.toml.bak_malachite`.
- BGMI (`com.pubg.imobile`) and CODM added to the game list; game entries default to `performance`.
- GPU Governor panel inside the WebUI (frequency table, voltages, games, logs).
- Animated WebUI background (`webroot/bg.gif`, replaceable).

### Changed
- Governor WebUI moved to `webroot/gpu/` with module-id paths fixed.
- Governor's volume-key menu is now `script/gov_menu.sh`.
- Governor no longer renames `module.prop` or points updates at its own server.

### Fixed
- `profiles.conf` is now read from `beast/` (v1.6.0 looked in the wrong folder).
- Governor running-state check now uses `log/governor.pid`.

### Notes
- Thermal protection is not disabled; no thermal or touch nodes are written.
- Do not install alongside the standalone Mediatek Mali GPU Governor module.
