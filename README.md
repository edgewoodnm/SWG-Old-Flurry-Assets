# SWG-Old-Flurry-Assets
Custom client asset updates for SWG Old Flurry

The launcher reads `manifest.json` to download the cumulative, versioned client ZIP from GitHub Releases. The manifest records the exact byte size and SHA-256 checksum. Asset directories are stored at the ZIP root.

## v1.0.11 — Dark Side background QA

Adds the custom SWG OLD FLURRY fortress artwork behind the front-end screens, including login and character selection. The character, selection menu, buttons, and particle assets retain their existing behavior. Both registered station/Jedi backgrounds use the new art, with neutral color and a corrected crop.

This cumulative QA prerelease preserves all 740 v1.0.10 files byte-for-byte and adds only `ui/ui_backdrop_default.inc` and `texture/ui_background_old_flurry.dds`. No executable, configuration, server, or new TRE files are included. The two added assets are also tracked in Git. Close the client before applying the launcher update.

The live client displayed the art and full logo at login; the server owner confirmed the character selection result works perfectly. QA should check login, character selection, character rotation, character creation/back navigation, and return from the world, including color, logo position, and scaling at different aspect ratios. Existing higher-priority manual UI overrides can mask this patch.

If this QA release breaks a tester's client, the recovery plan is a fresh base client followed by the corrected package through the launcher. Wait for a correction before reinstalling: the current launcher package would otherwise install the same background again. See [QA and Git recovery instructions](ROLLBACK-v1.0.11.md). The launcher has no rollback button.

## v1.0.10 — Atmospheric flight QA

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

