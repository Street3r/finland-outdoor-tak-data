# ATAK quick start

> **Suomeksi lyhyesti:** asenna kuvakesarja kerran, lisää KML-linkki käsin (Import → KML Link, kopioi osoite jakosivulta) tai tuo alueen datapaketti. QR-koodit: [jakosivu](https://street3r.github.io/finland-outdoor-tak-data/share/fi/) ja [SHARE.fi.md](../SHARE.fi.md).

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

### KML network link

A refreshing link can only be added by hand: opening the `.kml` through a QR code or an "open in ATAK" link imports a one-off copy. The share pages have a copy button for each URL.

1. Import → **KML Link**.
2. Name: e.g. `Finland outdoors`. URL: `…/links/all_en.kml` (or `all_fi.kml`, `kansallispuistot_en.kml`, `maakunnat_en.kml`).
3. Auto refresh on, interval `86400` (the data changes weekly).
4. Overlay Manager → **Network Resources**: download, then switch areas on and off. National parks are on by default, regions off.

A single area works the same way with its `.kmz` URL, e.g. `…/en/kansallispuistot/nuuksio/nuuksio_en.kmz`.

### Data package

Import `…/<lang>/<category>/<area>/<area>_<lang>.zip` via Import Manager, a QR code, or TAK Server. The package name ends with the date of its latest change, e.g. `Nuuksion kansallispuisto (fi) 2026-10-21`.

- The package stays in **Data Packages**, so its contents can be hidden or removed together.
- A new version has a new package UID, so ATAK imports it and updates the existing markers and routes (no duplicates). Importing the same version again is skipped. Finnish and English packages of an area share the same items: importing the other language switches the texts.
- Sites removed from the data stay on the device until you delete the old package: in Data Packages, delete the old version together with its contents, then import the new one.

Filter with hashtags in the search: `#laavu`, `#nuotiopaikka`, `#nuuksio`, `#uusimaa` …

### QR codes and links

`tak://com.atakmap.app/import?url=<url>` opens a file directly in ATAK (ATAK asks for confirmation). The [share pages](https://street3r.github.io/finland-outdoor-tak-data/share/en/) have a QR code and an "open in ATAK" button for every area, one page per category and language; [SHARE.md](../SHARE.md) has the start links. iTAK and WinTAK: use the plain https link.

## WinTAK and Google Earth

Open the `.kml` file (network link) or the `.kmz`.

## Known limitations

- Many Metsähallitus sites and main trails are missing from Lipas; OpenStreetMap fills some gaps.
- Network links have to be added by hand (Import → KML Link); a QR import creates a one-off copy.
- To be confirmed: whether ATAK fetches areas that are switched off.
