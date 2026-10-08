# finland-outdoor-tak-data

Ready-to-use TAK data for Finnish national parks and regions: shelters, campfire sites, towers, toilets and hiking routes as CoT data packages, KMZ overlays with auto-refreshing KML network links, GPX routes and GeoPDF maps for **ATAK, WinTAK and iTAK**.

> **Status:** early pilot. Download URLs go live once the first weekly update has been published.

## What's available

| Content | Format | Where |
|---|---|---|
| All areas as auto-refreshing layers | KML network link | `links/all_en.kml`, `links/all_fi.kml` |
| National parks / regions only | KML network link | `links/kansallispuistot_*.kml`, `links/maakunnat_*.kml` |
| One area (41 national parks, 19 regions) | KMZ, TAK data package, GPX | `<lang>/<category>/<area>/` |
| Icon set for the markers | ATAK iconset | `iconset/lipas2tak_iconset.zip` |
| National park maps | GeoPDF, overlay KMZ | [Releases](../../releases), [maps/](maps/) |

Base URL: **https://street3r.github.io/finland-outdoor-tak-data/** (lists every file).
Finnish and English versions are separate files (`fi` / `en`).

## Quick start (ATAK)

1. Install the icon set once: scan its QR code in [SHARE.md](SHARE.md), or import `iconset/lipas2tak_iconset.zip`.
2. **Import → KML Link**, paste `https://street3r.github.io/finland-outdoor-tak-data/links/all_en.kml`, turn on auto refresh (86400 s).
3. Switch areas on and off in Overlay Manager → Network Resources.

For navigable routes and #hashtag filtering, use the per-area **data packages** instead of KML. Details: [docs/atak-quick-start.md](docs/atak-quick-start.md) · QR codes for everything: [SHARE.md](SHARE.md).

## How this repository works

| Branch / place | Content | Updated by |
|---|---|---|
| `main` | this page, docs, map catalogue, overlays, QR codes | hand |
| [`data`](../../tree/data) | generated layers and packages, served via GitHub Pages | weekly bot; holds only the latest version |
| [Releases](../../releases) | GeoPDF maps (large files) | hand, one release per map edition |

The data is generated from [Lipas](https://lipas.fi) and [OpenStreetMap](https://www.openstreetmap.org) by [python-lipas2tak-tool](https://github.com/Street3r/python-lipas2tak-tool) and published by [docker-lipas-integration](https://github.com/Street3r/docker-lipas-integration).

## Licence

Generated data: [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/) — *Lipas – University of Jyväskylä (CC BY 4.0); © OpenStreetMap contributors (ODbL 1.0); Statistics Finland (CC BY 4.0)*. Maps, docs and tools have their own terms: see [LICENSE.md](LICENSE.md).

The data is provided as is. Always check current information from the site operator before relying on it in the field.
