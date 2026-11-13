# WNDR

**WNDR = Wi-Fi · Nooks · Drinks · Recording**

*Presented by Chambers Creations, LLC*

Calm places to work from a laptop or have a private conversation, plus a toggleable layer of **podcast recording spaces** (free library studios first, then low-cost paid studios), in the places Wes travels:

| Region | Work spots | Podcast spaces |
|---|---|---|
| Dallas, TX | 14 | 9 (6 free, 3 paid) |
| Fort Worth, TX | 12 | 3 (paid) |
| Austin, TX | 15 | 3 (1 free, 2 paid) |
| Oklahoma City, OK | 10 | 2 (1 free, 1 paid) |
| Edmond, OK | 5 | none found |
| Guthrie, OK | 2 | none found |
| Tupelo, MS | 3 | none found |
| San Diego, CA | 12 | 5 (2 free, 3 paid) |
| Northern NM: Santa Fe | 10 | none mappable (see notes in app) |
| Northern NM: Taos | 5 | 1 (paid) |
| Northern NM: Red River | 3 | none found |
| Northern NM: Angel Fire | 3 | none found |

**Live map:** https://mrchambers-wolf.github.io/wndr/

## How to use
Tap the **?** button in the app for the full guide. In short:
- **Region chips** scroll sideways: Dallas, Fort Worth, Austin, OKC, Edmond, Guthrie, Tupelo, Northern NM (all four NM towns), Santa Fe, Taos, Red River, Angel Fire, San Diego and All. Spots load only when you tap a chip or pan the map into a region, so the app stays fast. Zoomed out, bubbles show each region and its spot count.
- WNDR opens on **Dallas**, or on your nearest region if you've already allowed location. **Near me** jumps to the nearest region and sorts by distance.
- **Search** covers names, areas, vibe notes, rates and your own notes, across all regions. **Filters** set type, free/paid and outdoor seating.
- **Tap a pin or row** for details with **Google Maps, Waze and Apple Maps** navigation buttons (exact coordinates; spots with an approximate pin search by name and address instead), plus Call, Email and Website.
- **♥ Favorites** on every row and details page; the **Saved** tab lists them along with any spot you've noted.
- **My note** on each details page is private, saves as you type, shows in the list and is searchable.
- **Share spot** uses your phone's share menu (or copies a link) with a deep link like `…/wndr/#spot=sf6` that opens the map on that spot with details open. You can choose to include your note.
- **Export / Import** (Saved tab) saves favorites and notes as a JSON file and merges one back in.
- Favorites and notes are stored only in your browser (localStorage). There are no accounts, no backend and no public notes.
- **Add to Home screen** from Chrome's ⋮ menu (Android) or Safari's Share menu (iPhone).
- Hours and rates change: **call ahead** to confirm.

Region links: `#dallas`, `#fort-worth`, `#austin`, `#okc`, `#edmond`, `#guthrie`, `#tupelo`, `#northern-nm`, `#santa-fe`, `#taos`, `#red-river`, `#angel-fire`, `#san-diego`, `#all`. Add `?help` to open the guide.

## Files
- `index.html`: the app (Leaflet + OpenStreetMap tiles, mobile-first, no build step).
- `data/index.json`: a small index of each region's center, bounds, counts and spot ids (used for deep links and the zoomed-out bubbles).
- `data/<region>.json`: that region's work spots, podcast spaces, OSM library branches and city boundaries.

The app loads data with `fetch`, so open it from a web server (GitHub Pages, or `python3 -m http.server`); it won't work by double-clicking the file.

## Adding a spot
Add one object to the `work` or `pods` array in the region's `data/<region>.json`, add its id to that region's `ids` list in `data/index.json`, and update `counts`. Use a real geocode (US Census geocoder or OpenStreetMap). Leave unknown fields as `""`; never guess hours, rates or phone numbers. Optional `navq` (a name + address string) makes the navigation buttons search instead of using coordinates.

Spot details and links were checked Nov 12, 2026 (DFW, Austin) and Nov 13, 2026 (new regions); call ahead to confirm hours and studio rates.
Map data © OpenStreetMap contributors. Coordinates from the US Census Geocoder and OpenStreetMap.
