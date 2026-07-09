# Geocaching.hu Planner

A single-page map that compares two [geocaching.hu](https://geocaching.hu) users' finds, to help plan a caching trip together.

**Live map:** https://hann.io/geocaching-hu-planner/

## What it does

Enter two geocaching.hu usernames and the map shows every active cache in Hungary, color-coded by who's found it:

- 🔴 only user 1
- 🔵 only user 2
- 🟢 neither
- ⚪ both (hidden by default)

Each group can be toggled independently. For multi-caches, the individual stage points can be shown as smaller dots and connected with a dashed line, so you can see the layout of a multi at a glance without opening it. A few reference overlays are also available: hiking/cycling/MTB trails ([Waymarked Trails](https://waymarkedtrails.org)), protected natural areas ([OKIR](https://web.okir.hu/hu/tart/index/234/Interaktiv_termeszetvedelmi_terkep)), and forest protection status ([NÉBIH](https://erdoterkep.nebih.gov.hu/)).

The current usernames are reflected in the URL (`?user1=...&user2=...`), so a search can be bookmarked or shared directly.

## Usage

Just open `index.html` (locally or via the live map above) - no build step, no server required. It's a single self-contained HTML file that talks directly to the public [geocaching.hu API](https://api.geocaching.hu) from the browser.

## Tech

- [Leaflet](https://leafletjs.com/) for markers, popups and the layer control
- [MapLibre GL JS](https://maplibre.org/) for the vector basemap ([OpenFreeMap](https://openfreemap.org)'s "Liberty" style), bridged into Leaflet via [maplibre-gl-leaflet](https://github.com/maplibre/maplibre-gl-leaflet) for smooth (non-stepped) zooming
- No build tooling, no dependencies beyond what's loaded from CDN in `index.html`

## License

MIT - see [LICENSE](LICENSE).
