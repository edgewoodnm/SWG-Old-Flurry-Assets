# Old Flurry Halloween content and compatibility — v1.0.30

Use the existing launcher's **Old Flurry Assets** update. Fully close the game before installing, then reopen it. This is the complete cumulative client package; no manual Halloween hotfix is required afterward.

Includes all 5,234 supplied, activated Halloween client resources: Spooky Tusken and Spooky Exar Kun instances, new gear and schematics, five glowing wing colors, halo, vehicles and vendor assets. Yoda's two instance routes and both returns to Mos Eisley Shuttleport A were tested live on the matching server.

Repairs the wing appearance-equip crash across 400 meshes. The server owner confirmed green wings equip without crashing after restart. All 2,037 supplied skeletal meshes pass the structural checks used for this fix. New wearable rows follow stock species block/hide rules; Nightbrother rows use the supplied male Zabrak fits. 576 native species eligibility checks passed. Individual outfit/species visual checks remain ongoing. Enable Show Helmet to display the halo.

TRE-only asset payloads: all earlier v1.0.28 resources remain included. The 890 legacy loose resources are now packed into the new TREs, so the ZIP ships no loose asset files. The existing swgsource_3.0.tre is retained byte-for-byte. Three new registered TRE archives keep the package within the unchanged launcher limits: 5 ZIP entries, under 100 MiB per file, under 500 MiB extracted. client.cfg retains its normal includes and adds the archives after user.cfg so older manual Halloween and Hoth overlays cannot mask the repaired resources. login.cfg, user.cfg, player profiles and executables are not replaced.

Hollow Mother's boss/arena base packages and Gothic Moon furniture model part were not supplied; those incomplete encounters/assets remain excluded. This package does not claim those missing pieces are playable.

For an existing manual installation, use this cumulative launcher update instead of combining older hotfix ZIPs. If the client is open, exit it completely before installing. See VALIDATION-v1.0.30.json and PACKAGE-DIFF-v1.0.30.json for verification details.

