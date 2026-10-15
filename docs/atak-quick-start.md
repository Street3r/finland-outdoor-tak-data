# ATAK quick start

> **Suomeksi lyhyesti:** asenna kuvakesarja kerran, lisää päivittyvä taso jakosivun QR-koodilla tai painikkeella tai tuo alueen datapaketti. QR-koodit: [jakosivu](https://street3r.github.io/finland-outdoor-tak-data/share/fi/) ja [SHARE.fi.md](../SHARE.fi.md).

Base URL: `https://street3r.github.io/finland-outdoor-tak-data/`

## 1. Icon set (once)

Import `iconset/lipas2tak_iconset.zip` (Import Manager, or scan the QR code in [SHARE.md](../SHARE.md)). Without it the markers show as default icons. A new version of the icon set replaces the old one and updates markers already on the map.

## 2. Choose how to load the data

| Option | Best for | Routes | #hashtag filter | Updates |
|---|---|---|---|---|
| **KML network link** | overview, many areas | lines | no | automatic |
| **Data package** (`.zip`) | navigation in one area | navigable ATAK routes with named waypoints | yes | re-import |
| **GPX** (`_gpx.zip`) | routes only | converted to ATAK routes on import | – | re-import |
| **GeoPDF** | offline base map | – | – | per map edition |

Named routes are navigable ATAK routes; a loop route has one start point ("lähtö ja paluu" / "start and finish"). Unnamed path networks (many connected paths without route names, e.g. Isojärvi) are drawn lines named "<site> · 4.6 km", with the network's total length in the remarks. Long routes are split at region borders, so each region package has its own section.

### KML network link

Easiest: open the **auto-refreshing layer** QR code or button on the share page (the `_link.zip` package). ATAK adds the link to Overlay Manager → Network Resources and refreshes it daily. Opening the `.kml` file itself would only import a one-off copy.

By hand (or in other apps):

1. Import → **KML Link**.
2. Name: e.g. `Finland outdoors`. URL: `…/links/all_en.kml` (or `all_fi.kml`, `kansallispuistot_en.kml`, `maakunnat_en.kml`).
3. Auto refresh on, interval `86400` (the data changes weekly).
4. Overlay Manager → **Network Resources**: download, then switch areas on and off. Switch on the whole link to show every area, or open it and pick single areas (e.g. Nuuksio National Park). ATAK only downloads the areas that are switched on. National parks are on by default, regions off. Regions contain the parks too, so switching on both a park and its region shows the park features twice, in exactly the same places; this is harmless. Each region must be switched on separately.

A single area works the same way with its `.kmz` URL, e.g. `…/en/kansallispuistot/nuuksio/nuuksio_en.kmz`.

### Data package

Import `…/<lang>/<category>/<area>/<area>_<lang>.zip` via Import Manager, a QR code, or TAK Server. The package name ends with the date of its latest change, e.g. `Nuuksion kansallispuisto (fi) 2026-10-21`.

- The package stays in **Data Packages**, so its contents can be hidden or removed together.
- A new version has a new package UID, so ATAK imports it and updates the existing markers and routes (no duplicates). Importing the same version again is skipped. Finnish and English packages of an area share the same items: importing the other language switches the texts.
- The old version stays in **Data Packages** after a new one is imported. Delete it if you no longer need it; the date in the package name tells the versions apart.
- Sites removed from the data stay on the device until you delete the old package: in Data Packages, delete the old version together with its contents, then import the new one.

Filter with hashtags in the search: `#laavu`, `#nuotiopaikka`, `#nuuksio`, `#uusimaa` …

### QR codes and links

`tak://com.atakmap.app/import?url=<url>` opens a file directly in ATAK (ATAK asks for confirmation). The [share pages](https://street3r.github.io/finland-outdoor-tak-data/share/en/) have a QR code and an "open in ATAK" button for every area, one page per category and language; [SHARE.md](../SHARE.md) has the start links. iTAK and WinTAK: use the plain https link.

## WinTAK and Google Earth

Open the `.kml` file (network link) or the `.kmz`.

## Known limitations

- Many Metsähallitus sites and main trails are missing from Lipas; OpenStreetMap fills some gaps.
- Refreshing layers come from the `_link.zip` packages; importing a `.kml`/`.kmz` file directly creates a one-off copy.
- Tested with ATAK 5.8 and TAK Aware. iTAK and WinTAK have not been tested yet.
