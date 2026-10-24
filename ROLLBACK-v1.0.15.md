# v1.0.15 QA recovery

Close the game client first. The exact added and modified paths are recorded in [PACKAGE-DIFF-v1.0.15.json](PACKAGE-DIFF-v1.0.15.json).

The only overwritten previous asset is `misc/object_template_crc_string_table.iff`. To reverse this client update manually, restore its exact v1.0.13 bytes and remove only the 135 paths in the delta's `added` list. Do not delete whole asset directories. Do not remove other custom object registrations or server objects. Manual test overlays can mask the launcher files and must be handled separately.

The v1.0.13 baseline ZIP is 33,061,625 bytes; SHA-256 B6DDEFB1371D0099A3072BE24467741021C3288A0702139D97D7D43132CA1A06. Existing v1.0.13 assets are otherwise byte-identical in v1.0.15.

For launcher-only testers, use a clean supported base client and a maintainer-published corrected higher-version cumulative package. Do not expect an older ZIP overlay or a downgraded manifest to remove added files. A correction must preserve unrelated later changes and switch the manifest only after its downloadable asset exists and its checksum is verified. Reverting Git metadata alone does not repair tester installations.

Server collision, buildout and terminal/NPC scripts are deployed separately. A client rollback does not roll back the server; coordinate any server rollback using private deployment backups. No private backup or server configuration is included in this repository or release.
