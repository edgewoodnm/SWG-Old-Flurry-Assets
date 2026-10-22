# v1.0.12 music QA and recovery

## Package delta

Added at the ZIP root:

- `sound/music_main_title.snd`
- `music/old_flurry_imperial_march.mp3`

All 742 v1.0.11 files are byte-for-byte unchanged. The sound template replaces the stock shared front-end cue through the normal asset override mechanism; it is newly added to this cumulative package. The earlier short WAV test clip, local configuration, backups, account data, executables, and server files are not included.

## QA

Close SWG before the launcher update. Listen at login and character selection. Let the approximately 3:07 track finish to test the actual repeat, checking for silence/clicks and appropriate volume. Enter the world and verify front-end music stops normally; return to character selection and check it resumes. Zero configured loop delay does not guarantee a perceptually gapless MP3 transition.

The local MP3 decoded successfully, its cue specifies one sample and infinite looping, both assets resolved through the client configuration, and SWG reached login. The user requested publication after local testing; audible transitions and broader compatibility are left for human QA. Another higher-priority sound override, including the owner's separate `old_flurry_music_files` folder, can mask this public patch.

## Tester recovery agreed by the owner

Wait until the owner publishes a corrected package. Close the game, preserve wanted local settings/screenshots, replace the affected installation with a fresh base client, and apply the corrected release through the launcher. Do not copy old custom override folders into the fresh installation. Updating while v1.0.12 is still active will reinstall this music.

## Maintainer Git reversal

From a clean checkout:

```sh
git fetch origin --tags
git switch main
git pull --ff-only
git show --stat v1.0.12
git revert v1.0.12
```

This creates a normal reversal commit, removes the two tracked music files and restores preceding metadata. Do not force-push or move tags. Git revert does not remove files already installed on testers' disks or delete the existing release.

Before pushing the final correction manifest, publish an unused higher-version recovery release (for example v1.0.13 if v1.0.12 remains newest). To restore v1.0.11 behavior, reuse the verified v1.0.11 ZIP under the correction's versioned filename and record its exact size/hash and URL. The v1.0.11 baseline is 30,834,167 bytes with SHA-256 `BB9697E0B5AF4251B4AB5DE65D3E5300936776B3CC2EF04FA01164B18A275664`. If later changes have shipped, preserve them while removing only this music delta. Update `manifest.json` to the higher version and publish fresh-client recovery instructions before telling testers to reinstall.

An older manifest can be ignored by a launcher that requires increasing versions, and extracting an older ZIP over the existing client may leave these added files behind. Retain previous releases for recovery. No server rollback is required.

For maintainers who prefer exact-file removal, close SWG and remove only the two paths listed above from the installed patch, restoring any prior custom loose versions from backup. Do not remove entire sound/music folders. Disable any separate manual music overlay as well. The active launcher update can restore the files until a correction is published.
