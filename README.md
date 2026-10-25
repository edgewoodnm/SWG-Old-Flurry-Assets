Hoth municipal service hotfix deployed October 25: city map registration, player shuttle setup, and cloning dependencies corrected on the QA server. Use client **v1.0.19**; see the [updated tester checklist](HOTH-CITIES-v1.0.19.md#municipal-service-hotfix---october-25-2026).

Latest QA update: **v1.0.19 — Hoth player cities and wildlife**. Update through the launcher and fully restart the client. See [patch notes](HOTH-CITIES-v1.0.19.md).

# SWG-Old-Flurry-Assets
Custom client asset updates for SWG Old Flurry

The launcher reads `manifest.json` to download the cumulative, versioned client ZIP from GitHub Releases. The manifest records the exact byte size and SHA-256 checksum. Asset directories are stored at the ZIP root.

## v1.0.15 â€” Hoth Imperial Stronghold QA

Cumulative launcher update with Hoth map/ticket UI, planet/travel tables, buildout, terrain, Imperial Stronghold snow/rock exterior and collision, and red Imperial screens. Close SWG, update to **1.0.15**, then restart the client. Existing v1.0.13 content remains included; only its object-template registry is extended with all prior registrations retained.

Testers need this client package and the matching QA server. No developer configuration, server scripts or backups should be copied to tester PCs. Check ticket purchases, Hoth/Mos Eisley round trips, ship-terminal selection/launch/travel, doorways and collision. Native checks passed; in-game QA is still required.

See [exact package delta](PACKAGE-DIFF-v1.0.15.json) and [recovery instructions](ROLLBACK-v1.0.15.md).

## v1.0.13 â€” Imperial Guild Hall lighting/materials QA

Updates the standalone guild hall with smooth glossy white interior materials, near-black exterior sections, clean red banners, corrected texture opacity, brighter native room lighting and two main-hall ceiling fill lights. Latest lighting/banner behavior still needs in-game QA. No decorating slots or triangles added; non-light POB data preserved.

Cumulative package: 731 v1.0.12 files unchanged, 13 guild hall files updated, six textures added. Existing background, music, flight labels and unrelated assets are unchanged. Close the client before updating. The Structure Management Terminal repair is a separate server deployment, not part of this client ZIP.

See [exact package delta](PACKAGE-DIFF-v1.0.13.json) and [manual/Git recovery](ROLLBACK-v1.0.13.md). Modified assets must be restored from the previous package, not simply deleted; the launcher has no rollback button.

## v1.0.12 â€” Imperial March login music QA

Replaces the shared login/character selection title music with the Imperial March, configured to repeat indefinitely with zero configured loop delay. The track is approximately 3 minutes 7 seconds. The v1.0.11 Dark Side background and all other previous assets are unchanged.

The cumulative ZIP preserves all 742 v1.0.11 files byte-for-byte and adds `sound/music_main_title.snd` and `music/old_flurry_imperial_march.mp3`. The new sound template overrides the stock title cue; no original TRE, executable, user configuration or server files are changed. Only the Imperial March is shipped; the earlier short local test clip is excluded. Audio source: [Internet Archive item tvtunes_12997](https://archive.org/details/tvtunes_12997). The MP3 contains only audio, with attached cover art and metadata removed.

Close the game before updating through the launcher. QA should check playback on both login and character selection, volume and the transition after about 3:07, and that the front-end music stops when entering the world. The cue and resource lookup were verified and the local client reached login; audible transitions require human QA. A local `old_flurry_music_files` overlay can mask the launcher assets and must be disabled to test the public package independently.

See [Git reversal and fresh-client recovery instructions](ROLLBACK-v1.0.12.md). If the update breaks a tester's client, wait for a higher-version correction, then install a fresh base client and update through the launcher.

## v1.0.11 â€” Dark Side background QA

Adds the custom SWG OLD FLURRY fortress artwork behind the front-end screens, including login and character selection. The character, selection menu, buttons, and particle assets retain their existing behavior. Both registered station/Jedi backgrounds use the new art, with neutral color and a corrected crop.

This cumulative QA prerelease preserves all 740 v1.0.10 files byte-for-byte and adds only `ui/ui_backdrop_default.inc` and `texture/ui_background_old_flurry.dds`. No executable, configuration, server, or new TRE files are included. The two added assets are also tracked in Git. Close the client before applying the launcher update.

The live client displayed the art and full logo at login; the server owner confirmed the character selection result works perfectly. QA should check login, character selection, character rotation, character creation/back navigation, and return from the world, including color, logo position, and scaling at different aspect ratios. Existing higher-priority manual UI overrides can mask this patch.

If this QA release breaks a tester's client, the recovery plan is a fresh base client followed by the corrected package through the launcher. Wait for a correction before reinstalling: the current launcher package would otherwise install the same background again. See [QA and Git recovery instructions](ROLLBACK-v1.0.11.md). The launcher has no rollback button.

## v1.0.10 â€” Atmospheric flight QA

Adds only `string/en/atmo_trial.stf` for atmospheric Launch/Return labels. All 739 v1.0.9 files remain byte-identical. No HUD/UI files are included. Flight itself runs on the separately updated server; supported testing is owned fighters on Tatooine, with current time/range/altitude limits and normal PvP rules.

The server owner reports flight, HUD, controls, return, non-GM visibility, firing and PvP working. This remains an experimental QA prerelease. Close the client before updating. See [manual removal and recovery instructions](ROLLBACK-v1.0.10.md): the launcher has no rollback button, and installing an older ZIP does not necessarily remove newly added files.

## v1.0.9

- Standalone Imperial Guild Hall with a near-black exterior, crimson Imperial banners, coordinated interiors, and a fixed red Imperial insignia.
- Shared building/deed templates, localized names and merged template registrations; original generic guild hall preserved.
- Cumulative package retains all v1.0.8 assets and preserves existing strings and registrations.

The matching server deployment offers Imperial Guild Hall Deed at the Mos Eisley Darth Vader vendor for 500,000 credits and configures this hall for 3,000 items. Those server features require a separate deployment. Close the client fully before updating. In-game placement and runtime tests are pending; this release is marked as a prerelease.

## v1.0.8

- M-68 Landspeeder r8 client assets and mount mappings.
- Four Imperial tables and the Imperial Dark Throne, with revised sizing and a fixed red Imperial insignia.
- Readable display names for 14 previously unlocalized item registrations.
- Existing v1.0.7 assets, table entries, localized strings, and template registrations preserved.

Close the game client fully before updating. This package contains client assets only; server item registration and vendor configuration are deployed separately. The latest furniture revision remains available for in-game testing as a prerelease.



Latest Hoth battlefield QA: v1.0.16 adds shallow snow breastworks, forward-camp labels and outpost wall footings. Fully close the client before updating; matching server deployment and gameplay QA are required.
