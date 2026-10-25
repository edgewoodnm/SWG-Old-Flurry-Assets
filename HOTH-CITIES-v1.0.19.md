# Hoth Player Cities and Wildlife — v1.0.19 QA

Update through the launcher, then fully close and reopen the client.

Adds standalone Hoth city hall, cloning facility, bank, garage, shuttleport, three gardens and five homes. Cold gray/blue materials cover interiors and exteriors; original Tatooine assets remain unchanged. Native portals, floors, footprints and civic behavior are retained. These deeds are restricted to Hoth, with player construction in the northern half; southern settlements, travel hubs and the battlefield remain protected.

The Hoth Colonial Deed Quartermaster is a noncombat, invulnerable snowtrooper in the Stronghold control room. Deeds cost 25,000–150,000 credits. The character builder also offers a Hoth City and Housing Pack.

Server companion changes add five native GCW regions including the existing battlefield, plus a stock-style wilderness scoring fallback, city faction/region-defender support, ordinary wildlife sites, a separate Unkajo encounter and cold-weather faction patrols. Region control and player-city declarations affect patrol allegiance; active combat is not forcibly reset. Existing travel routes are preserved.

This is a cumulative root-layout client package. Server scripts, executables, configuration and backups are not included. City placement, shuttle/cloning progression and final building appearance still require player gameplay QA. The material finish does not add new roof-snow geometry.

## Municipal service hotfix - October 25, 2026

The QA server now includes the missing exact-template registrations for the Hoth civic buildings. These are server-side fixes; the cumulative v1.0.19 client ZIP and its checksum are unchanged.

- [x] City Hall and Small House placement confirmed in game by the developer tester.
- [x] Existing FROZEN FLURRY city map registration repaired and confirmed in game.
- [x] Existing player shuttle initialized with its ticket terminal, shuttle, and ticket collector; shuttle/map fix confirmed in game. Native city travel destination is registered.
- [x] Cloning facility donor entries added for droid placement and respawn. Native checks confirm the cloning terminal, clone droid, and an interior cloning-lab respawn location.
- [x] Garage native vehicle repair trigger verified active. Bank terminals loaded successfully in player testing.
- [x] Existing southern travel hubs remain safe; all six Hoth GCW region lookups pass.

### Tester checklist

- [ ] Update to v1.0.19 through the launcher and fully reopen the client if not already updated.
- [ ] Place Hoth homes in the northern construction area (north coordinate 0 or greater), outside protected regions. Stock city skills, rank, zoning and lot requirements still apply; City Hall requires the native Politician placement skill.
- [ ] Register the city, refresh the planetary map, and verify its city and civic service entries.
- [ ] Purchase a ticket and complete a round trip using the player city shuttle and another Hoth travel point.
- [ ] Verify the player city cloning facility appears as an eligible clone destination and respawns inside its cloning lab after death. This gameplay test is still pending.
- [ ] Bring a repairable vehicle into the garage service area and verify the normal repair interaction and credit charge. This gameplay test is still pending.

No server files, private configuration or recovery backups need to be installed on tester PCs. No additional client download is required for this server hotfix if v1.0.19 is already installed.
