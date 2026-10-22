# v1.0.11 QA and recovery

## What changed

Added paths, relative to the launcher's installed asset directory:

- `ui/ui_backdrop_default.inc`
- `texture/ui_background_old_flurry.dds`

Modified previous assets: none. Removed assets: none. All 740 v1.0.10 files are byte-identical. `PACKAGE-DIFF-v1.0.11.json` records the package size/checksum and exact delta.

Both station/Jedi image widgets reference the custom art. Their crop rectangles are updated, palette bindings removed, and color/tint set to white. Original widget visibility, backdrop registrations, legacy particle hooks, character/menu layout, and particle appearance assets are preserved. The star-like speckles in the old station image were baked into its DDS; no global particle modification was needed. This is a shared front-end background, not a planet/zone loading-screen replacement.

## Tester installation and checks

1. Close all game-client instances and apply the normal launcher update.
2. Confirm the red/black fortress and full SWG OLD FLURRY logo at login and character selection.
3. Check the character, selection rows, buttons, tooltips, and rotation still work.
4. Check character creation/back navigation and returning from the world.
5. Report resolution/aspect ratio, cropping, incorrect cyan coloring, missing texture, or startup errors. Include a screenshot where possible.

Local login rendering was directly verified; the owner confirmed the character selection result works perfectly. This is not exhaustive QA coverage. A separately installed manual background or another higher-priority UI override can mask the launcher version. No local configurations or account data are shipped in this release.

## Agreed tester recovery: fresh client and corrected launcher package

If this release breaks a tester's client, wait for the owner to publish a corrected package. Then close the client, preserve any wanted screenshots/settings, remove the affected client installation, extract a fresh base client, and apply the correction through the launcher. Do not carry custom override folders from the broken installation into the fresh copy.

Do not reinstall and immediately update while v1.0.11 is still the active manifest: that would apply the same release again. The launcher has no rollback button. An older ZIP over an existing installation may leave newly added files behind, and a launcher may reject a lower version.

## Maintainer: manually reverse the publication through Git

From a clean checkout of the public repository, inspect the release commit, then create a normal revert commit:

```sh
git fetch origin --tags
git switch main
git pull --ff-only
git show --stat v1.0.11
git revert v1.0.11
```

The tag identifies the background publication commit. Reverting it removes the two tracked background assets and restores the preceding manifest/documentation in Git. Do not force-push, reset public history, or move the published tag.

**Do not push the reverted, lower-version manifest as the final launcher correction.** Complete a higher-version recovery publication first:

1. Download the retained `SWG-Old-Flurry-Assets-v1.0.10.zip` from the v1.0.10 release.
2. Verify its SHA-256 is `0DE0FED344016E94E5C708913FBFF9A3480CA72A2BF2214AF7B4A9163F989C56` and its size is 29,429,544 bytes.
3. For a full background rollback with no later releases to preserve, reuse those verified ZIP bytes under a NEW versioned package name. Choose an unused version greater than every deployed version (for example v1.0.12 if v1.0.11 is still the newest). If later changes have shipped, preserve them while removing only this background delta.
4. Publish a correction release with that package, exact byte size and SHA-256, and fresh-client recovery instructions. Retain the old release/tag for audit.
5. Change `manifest.json` to the correction's higher version and new release URL; commit and push the correction after its downloadable asset exists. Test the public URL and checksum.
6. Tell affected QA testers the correction is available and have them perform the fresh-client workflow above.

The example v1.0.12 is reserved only by publication, not by this document. Git revert affects repository history and the launcher pointer; it does not uninstall assets from testers' disks or delete an existing GitHub Release. Fresh installation is the agreed way to clear the bad files before the corrected launcher update.

## Optional exact-file removal for maintainers

With the client closed, remove only the two paths listed at the top from the installed patch directory, or restore any custom versions backed up before the update. Do not delete the entire `ui` or `texture` directory. A separate local `old_flurry_background_files` installation must be disabled separately; reverting the public repository does not remove that manual overlay. Until the manifest is corrected, another launcher update can restore the release files.

No server rollback is required for this background-only change.
