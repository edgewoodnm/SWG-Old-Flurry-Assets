IMPORTANT: wing equip crash repaired. See WING-CRASH-HOTFIX.txt.

Old Flurry Halloween integration backup

Client resource overlay for the matching private server integration.
This backup branch does not change the live launcher manifest.

Verified: 36 server item creations, 11 Clone Commando schematic requirements,
24 Halloween purchases with exact Moon Coin deductions and insufficient-funds checks.
Yoda spawn position and facing verified on the running server.
Both Yoda entries and both stock shuttleport exits passed live with Nattas.
Loading labels: Adventure Worlds and Ancient Dungeons (client restart required).

Install the halloween_event_files folder into the client root. Add a SharedFile
searchPath at the next unused priority, retaining existing search paths.
The local installation uses searchPath_00_18=halloween_event_files and
maxSearchPriority=18. Use the matching server release; do not mix versions.

Excluded incomplete packages: Hollow Mother arena and boss base packages
were not supplied; Gothic Moon furniture models were not supplied.
Unsafe destructive wing color-swap script is excluded; five colors are separate items.

