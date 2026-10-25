# Hoth wildlife missions and municipal services - v1.0.20 QA

Update through the launcher and fully reopen the client. This cumulative client package adds readable Hoth Wampa, Tauntaun, den and shelter mission target names. All previous client resources are retained.

The companion QA server now includes native Hoth General destroy missions and Scout hunting contracts using Wampas and Tauntauns, plus 64 additional fixed wilderness encounter sites. Wildlife groups activate near players, respawn on timers, and exclude city, hub and battlefield areas. The additional grid is limited to 96 live creatures, with idle cleanup. Existing fixed encounters and faction patrols remain. Unkajo is excluded from these ordinary missions and new wildlife groups; a custom heroic is planned separately.

Native temporary mission-data tests passed 8/8 hunting and 8/8 destroy generation. These tests assigned no player missions. Full acceptance, objective completion and reward QA remain pending. This update does not claim new delivery, artisan, entertainer, bounty or recon content for Hoth.

Also includes the deployed server fixes for Hoth city map registration, player shuttle terminal/collector/service setup and cloning droid/respawn configuration. Player testing confirmed City Hall/home placement and shuttle/map operation. Native checks confirm garage repair trigger, cloning terminal/droid and interior respawn. Death/clone and vehicle repair gameplay testing remain pending.

## QA checklist

- [ ] Update the client to v1.0.20, then fully reopen it.
- [ ] Open General and Scout mayor terminals on Hoth; accept a native destroy/hunt mission.
- [ ] Confirm readable mission names, correct waypoint/objective, kill credit, completion and credit reward.
- [ ] Explore outside player cities for Wampa groups and Tauntaun herds; check natural scale, combat, loot and respawn.
- [ ] Confirm wildlife remains outside city and protected travel areas.
- [ ] Verify player-city shuttle ticket round trip, cloning after death and garage vehicle repair.

No server scripts, executables, backups or private configuration are included. Existing city ranks, mayor skills, treasury costs, lots, zoning and travel routes are preserved. No server restart was required for the deployed table/script fixes.
