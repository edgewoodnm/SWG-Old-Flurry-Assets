# Old Flurry launcher-compatible Hoth package — v1.0.21 QA

Fixes “ZIP contains too many entries” without changing the launcher. The existing launcher permits 1,000 entries; v1.0.20 contained 1,428. This cumulative package contains 891 ZIP entries. All 1,428 prior client resources are retained: 538 Hoth city resources move into the already-registered swgsource_3.0.tre, while 890 resources remain loose.

The SWG Source 3.0 stock TRE contains 26,513 entries. All stock file payloads and their original offsets remain unchanged; the merged archive adds 538 resources. No stock resource is replaced inside the archive. The resulting TRE is 47,629,104 bytes, below the launcher's 100 MiB per-file limit. No configuration files or launcher/server executables are included. No server restart is needed.

Close SWG, press Old Flurry Assets in the existing launcher, approve the installation, then reopen SWG. Use the normal SWG Source 3.0 base client. The launcher retains backups of replaced files, including the TRE. Do not delete older loose assets: this package intentionally preserves their current versions. Developer overlays can mask public resources and should be excluded from QA verification.

## QA checklist

- [ ] Existing unchanged launcher downloads and installs without the ZIP entry error.
- [ ] Hoth map, travel, player-city buildings/deeds, shuttle and mission names load correctly.
- [ ] Older guild hall, furniture, music and other custom assets still work.

The separate snow-roof/park art work is not included in this packaging-only correction. No resource-spawn changes are included.
