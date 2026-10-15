# finland-outdoor-tak-data

Ready-to-use TAK data for Finnish national parks and regions: shelters, campfire sites, towers, toilets and hiking routes as CoT data packages, KMZ overlays with auto-refreshing KML network links and GPX routes for **ATAK** (WinTAK and iTAK not tested yet). GeoPDF national park maps are coming once publication permission has been granted.

> **Status:** pilot. The data is published and updated weekly; the share pages show when it was last checked. Tested with ATAK 5.8 and TAK Aware; iTAK and WinTAK are not tested yet.

## What's available

| Content | Format | Where |
|---|---|---|
| All areas as auto-refreshing layers | KML network link | `links/all_en.kml`, `links/all_fi.kml` |
| National parks / regions only | KML network link | `links/kansallispuistot_*.kml`, `links/maakunnat_*.kml` |
| One area (41 national parks, 19 regions) | KMZ, TAK data package, GPX | `<lang>/<category>/<area>/` |
| Icon set for the markers | ATAK iconset | `iconset/lipas2tak_iconset.zip` |
| QR codes and "open in ATAK" buttons for every area | web pages (en / fi) | [share/en](https://street3r.github.io/finland-outdoor-tak-data/share/en/), [share/fi](https://street3r.github.io/finland-outdoor-tak-data/share/fi/) |
| National park maps *(coming: awaiting publication permission)* | GeoPDF, overlay KMZ | [Releases](../../releases), [maps/](maps/) |

Base URL: **https://street3r.github.io/finland-outdoor-tak-data/** (lists every file).
Finnish and English versions are separate files (`fi` / `en`).

## Quick start (ATAK)

1. Install the icon set once: scan its QR code in [SHARE.md](SHARE.md) ([suomeksi](SHARE.fi.md)), or import `iconset/lipas2tak_iconset.zip`.
2. Open the **All areas** QR code or button on the [share page](https://street3r.github.io/finland-outdoor-tak-data/share/en/): ATAK adds an auto-refreshing layer. (By hand: Import → KML Link with `https://street3r.github.io/finland-outdoor-tak-data/links/all_en.kml`, auto refresh 86400 s.)
3. Switch areas on and off in Overlay Manager → Network Resources.

For navigable routes and #hashtag filtering, use the per-area **data packages** instead of KML. Details: [docs/atak-quick-start.md](docs/atak-quick-start.md) · QR codes for every area: [share page](https://street3r.github.io/finland-outdoor-tak-data/share/en/) ([suomeksi](https://street3r.github.io/finland-outdoor-tak-data/share/fi/)).

## How this repository works

| Branch / place | Content | Updated by |
|---|---|---|
| `main` | this page, docs, map catalogue, overlays, QR codes for the start links | hand |
| [`data`](../../tree/data) | generated layers, packages and share pages, served via GitHub Pages | weekly bot; holds only the latest version |
| [Releases](../../releases) | GeoPDF maps (large files; coming, awaiting publication permission) | hand, one release per map edition |

The data is generated from [Lipas](https://lipas.fi) and [OpenStreetMap](https://www.openstreetmap.org) by [python-lipas2tak-tool](https://github.com/Street3r/python-lipas2tak-tool) and published by [docker-lipas-integration](https://github.com/Street3r/docker-lipas-integration).

## Licence

Generated data: [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/) — *Lipas – University of Jyväskylä (CC BY 4.0); © OpenStreetMap contributors (ODbL 1.0); Statistics Finland (CC BY 4.0)*. Maps, docs and tools have their own terms: see [LICENSING.md](LICENSING.md).

The data is provided as is. Always check current information from the site operator before relying on it in the field.
