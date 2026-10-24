# v1.0.16 recovery

Only terrain/hoth.trn and string/en/hoth_region_names.stf differ from v1.0.15. Keep client terrain synchronized with the matching server terrain. For a controlled rollback, close clients, restore both files from the verified v1.0.15 cumulative package, restore the matching server deployment backup, and follow the five-minute server restart warnings. Prefer publishing a corrected higher-version cumulative package for ordinary launcher recovery. Do not lower manifest versions or remove previous assets.
