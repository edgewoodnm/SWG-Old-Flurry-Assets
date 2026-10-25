# Hoth city snow and material finish — v1.0.22 QA

Adds fitted decorative snow blankets to the 13 Hoth city-pack structure families, across all 49 existing exterior detail-level meshes. Roof contours, domes, parapets and raised park beds are retained. Every combined mesh stays below 10,000 triangles; the largest is 6,762.

Hoth doors now use isolated cool gray materials. All existing door style rows, movement speeds, timing, triggers, effects and geometry are preserved. The 7 portal objects retain their exact cell, portal, floor and door transform data. Building collision, floor meshes, hardpoints, object identities, deeds and city-service behavior are unchanged.

The remaining interiors use clean near-neutral white/gray materials with subtle warm highlights rather than desert brown. The large-house interior is deliberately preserved exactly as approved in game. The three parks retain their paths and non-plant decorations; 44 desert plant child decorations are removed from the large and small gardens. The medium garden had none of those plant children.

The owner restarted the client and confirmed: “Looks good and doors work.” That covers the installed visual patch; broader tester checks of each building type, distance transitions and city services are still useful.

## Install

Close SWG, click Old Flurry Assets in the existing launcher, approve installation, then reopen SWG. No launcher update or server restart is required. This cumulative package retains all prior content. The new/updated assets are stored in the already-registered swgsource_3.0.tre, with legacy loose resources preserved for compatibility. No configuration, login details, executables, server scripts or backups are shipped.

ZIP: 891 entries, below the unchanged launcher's 1,000-entry limit. Native SWG extraction and the unchanged launcher installation code were tested. Every exported patch resource is verified against the package's active resource resolution. Each prior archive resource outside this patch remains byte-identical.

## Tester checklist

- [ ] Snow follows roofs at close and distant views without flickering.
- [ ] Exterior doors look gray, open normally and remain walkable.
- [ ] Parks have no desert palms/plants and their paths remain clear.
- [ ] Interiors have no unwanted desert brown; large-house interior remains unchanged.
- [ ] City Hall, bank, cloning, shuttle and garage services continue working.

No resource-spawn, wildlife, GCW, city-rank, placement-rule or server changes are included.
