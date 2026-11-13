# WNDR

*Presented by Chambers Creations, LLC*

Chill, calm places to work from a laptop or have a private conversation across **Dallas, Fort Worth, and Austin, Texas**, plus a toggleable layer of **podcast recording spaces** (free library studios and low-cost paid studios).

**Live map:** https://mrchambers-wolf.github.io/wndr/

- Single-file web app (`index.html`): Leaflet + OpenStreetMap tiles, mobile-first.
- Overlays: work spots, podcast spaces, chill-zone density, city boundaries, 5-mile free/paid studio reach rings, library branches (OSM).
- Filters: city, type, free/paid, outdoor seating, search, and "near me".

## How to use
Tap the **?** button in the app for the full guide. In short:
- **City chips** jump to Dallas, Fort Worth or Austin; **search** covers names, areas, vibes and rates; **filters** set type, free/paid and outdoor seating.
- **Near me** uses your location and sorts spots by distance.
- **Bottom panel**: swipe up/down or tap the handle; switch Work and Podcast tabs.
- **Tap a pin** for details and one-tap Directions, Call, Email and Website.
- **Layers** (top right): work spots (teal); podcast spaces (filled purple = free, purple ring = paid); chill zones (amber glow where spots cluster); city boundaries; 5-mile rings around free (green) and paid (amber, dashed) studios; library branches (OpenStreetMap).
- **Add to Home screen** from Chrome's ⋮ menu (Android) or Safari's Share menu (iPhone).
- Hours and rates change: **call ahead** to confirm.

## Adding a spot
Edit the `WORK` or `PODS` arrays near the top of `index.html` (one object per line), then commit. Leave unknown fields as `""`.

Spot details and links were checked Nov 12, 2026; call ahead to confirm hours and studio rates.
Map data © OpenStreetMap contributors.
