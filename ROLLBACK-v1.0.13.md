# v1.0.13 QA and recovery

The launcher has no rollback button. Close SWG before changing files. Wait for the owner to publish a corrected higher-version release before reinstalling a fresh base client and updating through the launcher. Preserve wanted screenshots/settings separately, not old override folders.

## Exact package delta

Restore these modified files from the verified v1.0.12 package; do not delete them:

- `appearance/imperial_guild_hall.pob`
- `shader/imperial_gh_all_banner_assoc_a_asb13.sht`
- `shader/imperial_gh_all_concrete_a_fallback_a2d13.sht`
- `shader/imperial_gh_all_concrete_b_fallback_a2d13.sht`
- `shader/imperial_gh_all_tile_a_adb13.sht`
- `shader/imperial_gh_corellia_underhanga_trim_ads16.sht`
- `shader/imperial_gh_corellia_verticala_trim_ads16.sht`
- `shader/imperial_gh_intr_assoc_marble_white_gloss_ces17.sht`
- `shader/imperial_gh_intr_assoc_marbleblack_gloss_ces17.sht`
- `shader/imperial_gh_intr_assoc_stucco_fallback_c2d13.sht`
- `shader/imperial_gh_intr_assoc_wall_gloss_ces17.sht`
- `shader/imperial_gh_intr_commerce_wall_a_cd8.sht`
- `texture/imperial_gh_all_banner_assoc_a_asb13.dds`

Remove only these newly added files when reversing this update:

- `texture/imperial_gh_r2_banner_spec.dds`
- `texture/imperial_gh_r2_black_spec.dds`
- `texture/imperial_gh_r2_exterior_black.dds`
- `texture/imperial_gh_r2_porcelain_white.dds`
- `texture/imperial_gh_r2_white_spec.dds`
- `texture/imperial_gh_r3_banner_flat_normal.dds`

Use paths relative to the launcher's asset installation directory. If a manual overlay holds the same paths, restore/disable those copies too. Do not remove entire appearance, shader, texture or UI folders. Current v1.0.13 updates can reinstall these files until the maintainer switches to a corrected release.

## Maintainer reversal

From a clean checkout, fetch origin/tags and inspect `git show --stat v1.0.13`. A normal `git revert v1.0.13` reverses tracked delta/metadata, but does not remove installed tester files or rebuild the release ZIP. Do not force-push, move tags, or push a downgraded manifest as the finished fix.

Publish an unused higher-version cumulative correction from the verified v1.0.12 baseline, preserving later unrelated changes if any, and switch manifest.json only after that asset is available. Baseline v1.0.12: 33,664,750 bytes, SHA-256 813A246B723C73C7DE7C24CD0B8265731A886BA1FC3C2737D5B917DF24DF8C83. The existing v1.0.12 release is retained. An older manifest can be ignored and an overlay extraction can leave added files behind.

The server terminal repair is separate; reversing this client package does not require deleting persistent management terminals or changing the VM database. Use the private server deployment backup only if that independent repair must be reverted.
